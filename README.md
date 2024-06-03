# Project Description
What are the meaningful changes in the brain with experience, that allows for adaptive behavior? When we look at the coordinated activity across spiking networks of neuronal ensembles, we see a delicate balance of stability and flexibility, as needed for a system that can both learn and remember. In this project, we present a population of simultaneously-recorded neurons from the non-human primate during learning of a complex sequence memory task, and in sleep afterwards. These data are exceptionally rich for exploration, but also to address three fundamental questions: 1. can we decode behavioral states from the ensemble dynamics, 2. what is the core representational geometry of the ensembles (what factors are best preserved/differentiated in low-dimensional spaces, and how does the geometry constrain the computations and dynamics of the network), and finally, 3. Does the ensemble activity drift with time and experience, and if so, how?

Here's an illustration to highlight the collective patterns of activity of [neural ensembles in macaque hippocampus](https://www.youtube.com/watch?v=PVLZRPLcwW4) taken during sleep, that may reflect activation during recent experience. 


# Getting started 

'<a target="_blank" href="https://colab.research.google.com/github/hoffman-lab/Ensemble-Representational-Space/blob/main/manifold_learning.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>'

# Open Research Themes 
1. Experiment on neural manifold creation with using different hyperparameters (e.g. n_neighbors or min_dist in UMAP). Different parameters can greatly change the shape of the manifold and thus can affect the ability to decode different behaviors. Afterwards, consider creating UI to visualize neural manifolds across different hyperparameters. [Here](https://pair-code.github.io/understanding-umap/) is a great example.
2. Parallelize dimensionality reduction across a set of hyperparameters
3. Experiment with which behavioral parameters are most separated in low dimensional space (block type, trial number, time, head position, angular velocity, etc.). Feel free to use the dimensionality reduction methods that are referred to in this notebook, or any other ones that you may be familiar with (e.g. MDS, CEBRA, etc). 
4. See if you can analyze the [structural index](https://github.com/PridaLab/structure_index) within our data. Briefly, this is a method to quantify representational structure in a neural manifold. 
5. We are also interested in a new, supervised dimensionality reduction algorithm called [CEBRA](https://cebra.ai/docs/index.html). CEBRA uses neural networks to create a latent space representation of neural data, minimizing the distance between neural activity points that share similar behavioral labels. We're interested to see if CEBRA is able to create neural manifolds with underlying task-dependent structure even if the behavioral labels are scrambled. For example, if you scramble timepoints across the data, is there still continuous drift? You can try comparing structural index of a CEBRA generated manifold with and without timepoint scrambling. 

# Acknowledgements 
The data come from recordings described [in this paper](https://www.biorxiv.org/content/10.1101/2023.12.06.570369v1) (Abbaspoor and Hoffman, bioRxiv, 2023).

The task is described [in this paper](https://www.biorxiv.org/content/10.1101/2023.12.11.571113v1) (Abbaspoor, Rahman, Zinke and Hoffman, bioRxiv, 2023).

Funding: Whitehall Foundation and NINDS R01 NS127128

The lab has some limited openings for students and postdoctoral fellows. If interested, contact Kari Hoffman (kari.hoffman@vanderbilt.edu) for more info.
