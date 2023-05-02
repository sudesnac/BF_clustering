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
**BF surface label**:_seed-BASF.{L,R}.bin.fsa5.shape.gii_ - BF seed label in surface space (see Methods section of the publication for the details of creating this file).\

## Notebooks, Results and figures 

The notebook folder contains the following jupyter notebooks for running the analysis and creating the figures used in this work.\
The results and figures folders have sub-folders each containing respective resultant data (such as .nii.gz and .gii files) and figures inside the sub-folders. Reference surface for fsa-10k can be downloaded from [here](https://github.com/MICA-MNI/BrainSpace/tree/master/brainspace/datasets/surfaces) for visualizing gii results files using workbench.

### Diff_1p6mm-concat_clustering and DWI_concat

This notebook contains the code to compute clustering analyses done with concatenated diffusion data and the sub-folders have the corresponding results and figures which is presented in the Thesis (Chapter 2).

### Func_HCPMMP-concat_clustering.ipynb and Func_concat

This notebook contains the code to compute clustering analyses done with concatenated functional data and the sub-folders have the corresponding results and figures which is presented in the Thesis (Chapter 2).

### Diff_1p6mm-avg_clustering.ipynb and DWI_avg

This notebook contains the code to compute clustering analyses done with subjects group avaeraged diffusion data and the sub-folders have the corresponding results and figures.

### Func_HCPMMP-avg_clustering.ipynb and Func_avg

This notebook contains the code to compute clustering analyses done with subjects group avaeraged functional data and the sub-folders have the corresponding results and figures.
