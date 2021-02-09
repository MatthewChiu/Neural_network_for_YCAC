# Detecting metric types using a Neural network 

Theory: Music often refers to "meters" such as 3/4, 4/4, 6/8, etc. But, within the same meters, there are stylistic rhythms that create a sense of style. 
For example, while sarabandes and courantes are dance styles in 3/4, they are distinctly different. I refer to these characteristic and recurring patterns as "metric types." <br> <br>

Project: Can we create a model which can correctly identify musical types from one another based on their unique styles? <br> <br>

Procedure: Using a corpus of Bach pieces from the Yale Classical Archives corpus, extract chords as onsets. Since each chord has a different effect on perception, they are weighted by cardinality, duration, and register (see files). These weights are then appended into a time-series grid, and DFTs are calculated on randomized windows of the same length. Using the DFT component magnitudes, a NN model is trained to identify which metric type is which. <br> <br>
