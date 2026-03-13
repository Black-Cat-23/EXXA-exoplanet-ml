# EXXA – Protoplanetary Disk Clustering (ML4Sci GSoC Test)

This repository contains my solution to the **ML4Sci EXXA General Evaluation Test** for Google Summer of Code 2026.

The goal of this project is to analyze **synthetic ALMA observations of protoplanetary disks** and identify structural similarities using unsupervised machine learning techniques.

---

## Scientific Motivation

Protoplanetary disks are rotating structures of gas and dust surrounding young stars. Observations of these disks often reveal morphological features such as:

- rings
- gaps
- spiral arms

These structures are believed to be signatures of planet formation.

Machine learning methods can help automatically identify and group disks with similar structural properties.

---

## Dataset

The dataset contains **150 synthetic ALMA observations** stored as FITS files.

Each file contains a data cube with dimensions:
(4, 1, 1, 600, 600)


The first dimension corresponds to different observational channels.

For analysis, the channels are combined into a single 2D disk image.

---

## Pipeline Overview

The implemented pipeline performs the following steps:

1. Load and preprocess FITS disk observations
2. Normalize disk images
3. Construct a dataset of flattened disk images
4. Perform dimensionality reduction using PCA
5. Apply KMeans clustering to identify disk morphology groups
6. Evaluate cluster quality using silhouette score
7. Visualize clusters using PCA and t-SNE
8. Analyze disk structures through radial brightness profiles

---

## Example Disk Observation

Example visualization of a synthetic protoplanetary disk.

---

## Clustering Visualization

The PCA-reduced dataset reveals distinct disk morphology clusters.

---

## Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-Learn
- Astropy
- Jupyter Notebook

---

## Repository Structure
EXXA-exoplanet-ml
│
├── notebooks
│ └── exxa_general_test.ipynb
|
│── data
|
├── requirements.txt
│
└── README.md


---

## Author

Mitul Rishi  
B.Tech Computer Science  
IIIT Kota

Interested in machine learning applications in astrophysics and planetary science.