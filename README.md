<div align="center">
    <h1>Object Detection in CryoEM Datasets</h1>
</div>

<p align="center">
    <a href="https://mybinder.org/v2/gh/scivision-gallery/cryoEM-object-detection.git/main?labpath=CryoEM%20Example%20-%20Synthetic%20and%20EMPIAR.ipynb">
        <img alt="Binder" src="https://mybinder.org/badge_logo.svg">
    </a>
    <br/>
</p>

<p align="center">
  <img src="https://github.com/scivision-gallery/cryoEM-object-detection/blob/readme-fix/figs/cryoem_detection_example.png?raw=true" 
        alt="Object detection in a synthetic dataset with ODIN" width="60%" align="center">
</p>

<p align="center">
    <em>
    Detection of objects in a synthetic image with ODIN. Bounding boxes: purple - ground truth, yellow - prediction.
    </em>
</p>


## Abstract

Electron Microscopy aims to image particles (e.g., proteins, molecules) on a near atomic resolution. However, with great resolution comes low signal-to-noise ratio. As such, computer vision models need to be trained on noisy datasets in order to detect objects.

![CryoEM pipeline from raw image (left, individual particle highlighted in green) to the molecular structure (right)](https://github.com/scivision-gallery/cryoEM-object-detection/blob/readme-fix/figs/cryoem_objective.png?raw=true)


The structure of the objects being imaged is calculated by averaging hundreds if not thousands of frames of said object in different orientations, rotations and positions. The dataset generated is, consequently, large - usually, the pre-processed images (or with some degree of processing like motion correction) are uploaded onto an online database called EMPIAR.

In this notebook, we use scivision to load memory-friendly synthetic data (AlphabetSoup with a noise filter) and real data from the online database of EM images (EMPIAR), and run them through our pre-trained Object Detection in Images with Noise (odin) model.

## How to run

The notebook is designed to be launched from Binder.
* Click the **Launch Binder** button at the top level of the repository

You may also download the notebook from GitHub to run it locally:
* Open your terminal
* Check your conda install with `conda --version`. If you don't have conda, install it by following these instructions (see [here](https://docs.conda.io/en/latest/miniconda.html))
* Clone the repository, `https://github.com/scivision-gallery/cryoEM-object-detection.git` 
* Move into the cloned repository, `cd cryoEM-object-detection`
* Install the dependencies, `conda env create -f environment.yml`
* Activate the installed environment, `conda activate cryoEM-scivision-py39`
* Launch the jupyter interface of your preference, notebook, `jupyter notebook` or lab `jupyter lab`


## Where are the datasets and model repos?

For **synthetic AlphabetSoup dataset**, refer to: https://github.com/alan-turing-institute/intake-alphabetsoup

For **EMPIAR reader**, refer to: https://github.com/ots22/empiarreader

For **ODIN model**, refer to: https://github.com/alan-turing-institute/odin
