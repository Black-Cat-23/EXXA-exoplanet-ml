# EXXA – ML4Sci GSoC 2026 Test Submission

![Python](https://img.shields.io/badge/Python-3.10-blue)
![ML](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Astronomy](https://img.shields.io/badge/Domain-Astrophysics-purple)
![Status](https://img.shields.io/badge/Status-GSoC%20Test%20Submission-green)

Author: Mitul Rishi  
B.Tech Computer Science – IIIT Kota

This repository contains my solutions for the **ML4Sci GSoC 2026 EXXA test tasks**.

The project demonstrates machine learning pipelines applied to astronomical data analysis.

---

## Scientific Motivation

Protoplanetary disks are rotating structures of gas and dust surrounding young stars. Observations of these disks often reveal morphological features such as:

- rings
- gaps
- spiral arms

These structures are believed to be signatures of planet formation.

Machine learning methods can help automatically identify and group disks with similar structural properties.

---

# 🚀 Quick Reproducibility

All experiments can be reproduced by running the notebooks in order:

1. `general_test/exxa_general_test.ipynb`
2. `exxa3_test/exxa3_transit_detection.ipynb`

Clone the repository and install dependencies:

git clone https://github.com/Black-Cat-23/EXXA-exoplanet-ml.git

cd EXXA-exoplanet-ml

pip install -r requirements.txt

Launch Jupyter Notebook:

jupyter notebook

Open the notebooks and run all cells.


---

## Dataset

The dataset used in the General Test consists of **150 synthetic ALMA-like protoplanetary disk observations** stored in FITS format.

Each file contains a data cube with dimensions:

(4, 1, 1, 600, 600)

The first dimension represents multiple observational channels.

For analysis, the primary observational channel is extracted to obtain a **single 600 × 600 disk image** representing the intensity distribution.

These synthetic observations mimic structures commonly observed in protoplanetary disks, including rings, gaps, and spiral features.

**Note: The FITS dataset is part of the ML4Sci EXXA test resources and is not included in this repository.**

---

## Repository Structure

```
EXXA-exoplanet-ml
│
├── general_test
│   └── exxa_general_test.ipynb
│
├── exxa3_test
│   └── exxa3_transit_detection.ipynb
│
├── data
│   └── FITS dataset provided in the ML4Sci test resources
│
├── requirements.txt
└── README.md
```


# General Test – Protoplanetary Disk Analysis

This notebook analyzes **protoplanetary disk images stored in FITS format**.

Pipeline:

1. Load and preprocess FITS disk observations
2. Normalize disk images
3. Construct a dataset of flattened disk images
4. Perform dimensionality reduction using PCA
5. Apply KMeans clustering to identify disk morphology groups
6. Evaluate cluster quality using silhouette score
7. Visualize clusters using PCA and t-SNE
8. Analyze disk structures through radial brightness profiles

This analysis identifies **distinct morphological groups of protoplanetary disks**.

---

# EXXA3 – Simulated Exoplanet Transit Detection

This notebook implements a **machine learning pipeline for  simulated exoplanet transit signals** in stellar light curves

Pipeline:

1. Simulate transit light curves
2. Generate synthetic dataset
3. Explore orbital parameter distributions
4. Phase-fold transit signals
5. Train Random Forest classifier
6. Evaluate with classification metrics
7. Confusion matrix visualization
8. Signal-to-Noise Ratio analysis
9. Injection-recovery validation
10. Feature importance analysis

The goal is to demonstrate how **machine learning can assist in exoplanet detection workflows**.

---

# Key Techniques Used

Astrophysics

- Transit photometry
- Phase folding
- Radial brightness profiles
- Signal-to-Noise Ratio analysis

Machine Learning

- PCA dimensionality reduction
- KMeans clustering
- Random Forest classification

---

# Future Improvements

Possible extensions include:

- convolutional neural networks for disk morphology classification
- deep learning models for transit detection
- training on real datasets (Kepler / TESS)

---

## Tools and Libraries

- Python
- NumPy
- Matplotlib
- Scikit-Learn
- Astropy
- Jupyter Notebook

---


## Author

Mitul Rishi  
B.Tech Computer Science – IIIT Kota  

Interested in machine learning applications in astrophysics, planetary science, and scientific data analysis.