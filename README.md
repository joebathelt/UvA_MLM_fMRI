# Multi-level Modelling & Task fMRI: Course Notebooks

Practical Jupyter notebooks for the MSc course *Neuroimaging and Multi-level Modelling* at the University of Amsterdam.

The notebooks teach you how to analyse task-based functional MRI (fMRI) data in Python, the way researchers do it in practice. Instead of implementing every statistical step by hand, you will learn what each part of an analysis does and why, and then use established tools ([nilearn](https://nilearn.github.io)) to run it on real data. By the end of the course, you should be able to take an fMRI dataset with an events file, fit a first-level model, and combine results across participants with multi-level models.

## Course overview

| Week | Topic | Notebook |
|------|-------|----------|
| 1 | Introduction to multi-level models | [MLM_fMRI_Week1.ipynb](MLM_fMRI_Week1.ipynb) |
| 2 | Introduction to multi-level models | [MLM_fMRI_Week2.ipynb](MLM_fMRI_Week2.ipynb) |
| 3 | Introduction to neuroimaging and the General Linear Model | [MLM_fMRI_Week3.ipynb](MLM_fMRI_Week3.ipynb) |
| 4 | Preprocessing, prewhitening and contrasts | [MLM_fMRI_Week4.ipynb]([MLM_fMRI_Week4.ipynb]) |
| 5 | Group-level Analysis & Multiple Comparison Correction | [MLM_fMRI_Week5.ipynb]([MLM_fMRI_Week5.ipynb]) |

**Week 1** along with **Week 2** introduce computational modelling in cognitive science at different levels. Week 1 will begin at the highest level, modelling behavior in humans and in AI models. It starts with exploring the basics of reinforcement learning as a means to model learning and decision making processes. Next, it moves on to modelling the behavior of language models by treating them as participants in a psychology experiment, probing the grammatical knowledge of small, open-source language models and then investigating biases in large chat-facing LLMs.

**Week 2** introduces the basics of artificial neural networks and applies them to task of object classification. The second part of the week goes one step lower to model the behavior of a single neuron, and then extending that to model an entire cortical microcircuit

**Week 3** covers how MRI data are stored in NIfTI files (header, data array and affine), how to visualise brain images, and how to extract time series from single voxels and atlas regions. It then introduces the GLM with a face perception experiment: from events files and the haemodynamic response, to fitting a model by hand for one voxel, to whole-brain analysis with nilearn's `FirstLevelModel` and evaluating model fit. It ends with a practice exercise on an auditory dataset.

**Week 4** covers how neuroimaging data are organised with the Brain Imaging Data Structure (BIDS) and walks through the main preprocessing steps: motion correction, susceptibility distortion correction, slice timing correction, coregistration, normalisation and spatial smoothing, with interactive demos and a simulation of how smoothing affects GLM statistics. It then returns to the GLM with fMRIPrep-preprocessed data from a face perception experiment (smiling and neutral faces), showing how motion confounds and prewhitening improve a first-level model. It ends with contrasts between experimental conditions and a discussion of why single-participant results need correction for multiple comparisons and group-level analysis.

**Week 5** moves from single participants to group-level inference. It starts with visualising statistical maps in nilearn: slices, glass brains, the cortical surface and atlas regions. It then runs a group-level analysis of the faces > others contrast from 12 participants of the NI-edu functional localiser, first as a random-effects one-sample t-test and then as a mixed-effects analysis that weights participants by the precision of their estimates. Next, it compares methods for correcting for multiple comparisons on a simulated 2D brain, where the true effect is known: uncorrected thresholds, Bonferroni, false discovery rate, random field theory and cluster-extent thresholding. It then applies them to the real group map. It ends with non-parametric permutation tests, which use sign flipping and the maximum statistic to control the family-wise error rate, and a region-of-interest analysis showing that the same test becomes more sensitive when the search space is reduced to a region chosen in advance.

## Getting started

The notebooks are designed to run in [Google Colab](https://colab.research.google.com), so you don't need to install anything locally. Open a notebook in Colab and run the installation cell at the top first. You will need to run it again each time the Colab session restarts.

To run the notebooks locally instead, you need Python 3.10 or later and the following packages:

    pip install nilearn nibabel numpy pandas matplotlib scipy jupyter

All datasets are downloaded automatically by the notebooks the first time you run them.

## Prerequisites

- Basic Python programming (variables, loops, functions, NumPy arrays)
- Basic statistics, in particular linear regression

No prior experience with neuroimaging is needed.

## Data

The notebooks use openly available datasets, downloaded through nilearn:

- SPM multimodal faces dataset (Henson et al.), via `fetch_spm_multimodal_fmri`
- SPM auditory dataset (Rees, Friston and the FIL methods group), via `fetch_spm_auditory`
- Brain development fMRI dataset (Richardson et al., 2018), via `fetch_development_fmri`
- Harvard-Oxford atlas, via `fetch_atlas_harvard_oxford`

Please check the terms of use of each dataset before using it outside this course. The SPM auditory dataset, for example, is provided for personal education and evaluation purposes only.

## Acknowledgements

Parts of these materials are adapted from the notebook of the course Neuroimaging: BOLD MRI, originally developed by H. Steven Scholte and Lukas Snoek (2019) and updated by Joe Bathelt (2025).

## License

CC-BY-Universal

## Contact

Dr Joe Bathelt, j.m.c.bathelt [at] uva.nl
