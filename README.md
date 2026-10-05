# Multi-level Modelling & Task fMRI: Course Notebooks

Practical Jupyter notebooks for the MSc course *Neuroimaging and Multi-level Modelling* at the University of Amsterdam.

The notebooks teach you how to analyse task-based functional MRI (fMRI) data in Python, the way researchers do it in practice. Instead of implementing every statistical step by hand, you will learn what each part of an analysis does and why, and then use established tools ([nilearn](https://nilearn.github.io)) to run it on real data. By the end of the course, you should be able to take an fMRI dataset with an events file, fit a first-level model, and combine results across participants with multi-level models.

## Course overview

| Week | Topic | Notebook |
|------|-------|----------|
| 1 | Goals of experimental science & modelling | [coming soon] |
| 2 | Introduction to multi-level models | [coming soon] |
| 3 | Introduction to neuroimaging and the General Linear Model | [Week3/MLM_fMRI_Week3.ipynb](Week3/MLM_fMRI_Week3.ipynb) |
| 4 | Preprocessing, prewhitening and contrasts | [coming soon] |
| 5 | Multi-level modelling of fMRI data | [coming soon] |

**Week 3** covers how MRI data are stored in NIfTI files (header, data array and affine), how to visualise brain images, and how to extract time series from single voxels and atlas regions. It then introduces the GLM with a face perception experiment: from events files and the haemodynamic response, to fitting a model by hand for one voxel, to whole-brain analysis with nilearn's `FirstLevelModel` and evaluating model fit. It ends with a practice exercise on an auditory dataset.

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
