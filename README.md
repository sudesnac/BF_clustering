# BF_clustering

This repository contains codes and data in support of my thesis chapter 2 work "Connectivity based discrete parcellation of the human basal forebrain" 

## Publications

{Link to the thesis once it's ready...}

## Prerequisites

BF roi used is included in the data folder. This roi is created based on the [probabilistic atlas](https://pubmed.ncbi.nlm.nih.gov/18585468/).
All diffusion and functional data used for this study is downloded from [Human Connectome (HCP) project](http://www.humanconnectomeproject.org/).
The structural (diffusion) connectivity matrix is created using this [workflow](https://github.com/sudesnac/diffparc-smk). 
The functional connectivity matrix is created using this [workflow](https://github.com/khanlab/subcorticalparc-smk).
These workflow will create a .npz file containing all subject's connectivity matrices - the files should be placed in the data folder for running the analyses provided in the notebook. 

## Data

Contains the following data file necessary to run the analysis provided in the notebooks.\
**BF roi**: _seed_1p6mm.nii.gz_ - used to construct the connectivity matrices and compute the gradients across BF.\
**BF segmented roi**: _BF_masked_fullB_1p6mm.dseg.nii.gz_ - ch123 and ch4a/ch4p labeled roi used for statistical analysis.\
**HCP-MMP1 annot files**: *{lh,rh}_HCP-MMP1_fsa10.annot* - HCP-MMP1 parcellation annotation files in fsa-10k space for [brainspace](https://brainspace.readthedocs.io/en/stable/index.html) visualization.\
**Yeo network**: *hcp_mmp10_yeo7_modes.txt* - reference for Yeo 7 network mapped onto HCP-MMP1 parcellation from [here](https://pubmed.ncbi.nlm.nih.gov/30793087/).\
**Glasser 360 fsa5 label files**:_glasser_360_fsaverage5_{lh,rh}label.gii_ - Glasser parcellation labels in fsa10k for parcellating whole brain data (such as the geodesic, myelin and FEOBV data).\
**BF surface label**:_seed-BASF.{L,R}.bin.fsa5.shape.gii_ - BF seed label in surface space (see Methods section of the publication for the details of creating this file).\

## Notebooks and Results

The notebook folder contains the following jupyter notebooks for running the analysis and creating the figures used in this work.\
The results folder has sub-folders each containing respective resultant data (such as .nii.gz and .gii files) and figures inside the figures folder. Reference surface for fsa-10k can be downloaded from [here](https://github.com/MICA-MNI/BrainSpace/tree/master/brainspace/datasets/surfaces) for visualizing gii results files using workbench.

### Diff_concat

This notebook contains the code to compute ..... 

### Func_concat

This notebook contains the code to compute .....

### Diff_avg

This notebook is used to compute ...

### Func_avg

This notebook is for calculating .....
