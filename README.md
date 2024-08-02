# Project Description
What are the meaningful changes in the brain with experience, that allows for adaptive behavior? How does the brain create and deploy knowledge? When we look at the coordinated activity across spiking networks of neuronal ensembles, we see a delicate balance of stability and flexibility, as needed for a system that can both learn and remember. In this project, we present a population of simultaneously-recorded neurons from the non-human primate during learning of a complex sequence memory task, and in sleep afterwards. These data are exceptionally rich for exploration, and allow us to address questions such as: 
  1. What behavioral states can we decode from the ensembles,
  2. What is the core representational geometry of the ensembles (what factors are best preserved/differentiated in low-dimensional latent spaces).
  3. How does the geometry constrain the computations and dynamics of the network?
  4. Does ensemble activity drift with time or experience, and if so, how?

Here's an illustration to highlight the collective patterns of activity of [neural ensembles in macaque hippocampus](https://www.youtube.com/watch?v=PVLZRPLcwW4) taken during sleep, that may reflect activation during recent experience. 


# Getting started 

'<a target="_blank" href="https://colab.research.google.com/github/hoffman-lab/Ensemble-Representational-Space/blob/main/manifold_learning.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>'

# Open Research Themes 
1. Experiment on neural manifold creation using different hyperparameters (e.g. n_neighbors or min_dist in UMAP). Different parameters can greatly change the shape of the manifold and thus can affect the ability to decode different behaviors. Afterwards, consider creating a UI to visualize neural manifolds across different hyperparameters. [Here](https://pair-code.github.io/understanding-umap/) is a great example.
2. Parallelize dimensionality reduction across a set of hyperparameters
3. Experiment with which behavioral parameters are most separated in low dimensional space (block type, trial number, time, head position, angular velocity, etc.). Feel free to use the dimensionality reduction methods that are referred to in this notebook, or any other ones that you may be familiar with (e.g. MDS, CEBRA, etc). 
4. See if you can analyze the [structural index](https://github.com/PridaLab/structure_index) within our data. Briefly, this is a method to quantify representational structure in a neural manifold. 
5. You can also try a supervised dimensionality reduction algorithm called [CEBRA](https://cebra.ai/docs/index.html). CEBRA uses neural networks to create a latent space representation of neural data. The supervised contrastive loss function will minimize the distance between ensemble data points that share similar behavioral labels, thereby contrasting data points with dissimilar labels. If neural ensemble data drifts in time even as single unit recording is mechanically stable, then how does scrambling timepoints across cells (creating pseudo-ensemble data points) alter the manifold dimensionality? Is there still drift? You can try comparing the structural index of a CEBRA generated manifold with and without timepoint scrambling. 

# Recommended Tutorials and Demos
## PCA and linear methods
[basic PCA visualization, graphic demo](https://setosa.io/ev/principal-component-analysis/)
## Nonlinear methods
[for tSNE vs UMAP](https://pair-code.github.io/understanding-umap/)


# References
The data come from recordings described [in this paper](https://doi.org/10.1016/j.celrep.2024.114519) (Abbaspoor and Hoffman, Cell Reports, 2024).

The task is described [in this paper](https://www.biorxiv.org/content/10.1101/2023.12.11.571113v1) (Abbaspoor, Rahman, Zinke and Hoffman, bioRxiv, 2023).

# Acknowledgements 
Funding: Whitehall Foundation and NINDS R01 NS127128 to KLH
The lab has some limited openings for postdoctoral fellows. If interested, contact Kari Hoffman (kari.hoffman@vanderbilt.edu) for more info, or:
X: @perpl_lab
M:karihoffman@neuromatch.social
@karihoffman.bsky.social
