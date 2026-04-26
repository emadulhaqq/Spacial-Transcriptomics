#  Spatial Transcriptomics Analysis

This repository contains a set of Jupyter notebooks demonstrating different workflows for spatial transcriptomics data analysis using tools like Scanpy and Squidpy. Each notebook focuses on a specific dataset and highlights key analysis steps, visualizations, and insights.

---

## Overview

The project includes four notebooks, each working with a different spatial dataset:

* Basic Spatial Analysis (Scanpy) — Human lymph node (Visium)
* Fluorescence Analysis (Squidpy) — Mouse brain with fluorescence channels
* H&E Analysis (Squidpy) — Mouse brain with spatial statistics
* Xenium Analysis (Squidpy + SpatialData) — Human lung cancer at single-cell resolution

---

## Project Structure

```
├── README.md
├── requirements.txt
├── notebooks/
│   ├── 01_basic_scanpy_spatial.ipynb
│   ├── 02_visium_fluorescence.ipynb
│   ├── 03_visium_hne.ipynb
│   └── 04_xenium_analysis.ipynb
└── results/
    ├── 01_basic_scanpy/
    ├── 02_visium_fluo/
    ├── 03_visium_hne/
    └── 04_xenium/
```

---

## Notebook Summaries

### 1. Basic Spatial Analysis

* Data loading and quality control
* Normalization and feature selection
* PCA, UMAP, and clustering
* Marker gene identification
* Spatial visualization

Key idea: spatial clusters correspond to biological regions.

---

### 2. Fluorescence Analysis

* Visualization of fluorescence channels
* Image smoothing and segmentation
* Feature extraction (intensity, texture, counts)
* Clustering based on image features

Key idea: image features reveal patterns beyond gene expression.

---

### 3. H&E Spatial Analysis

* Image feature extraction
* Spatial neighbor graph construction
* Neighborhood enrichment
* Co-occurrence analysis
* Ligand-receptor interactions
* Moran’s I for spatial genes

Key idea: spatial statistics help uncover tissue organization.

---

### 4. Xenium Analysis

* Data preprocessing and clustering
* UMAP and spatial visualization
* Centrality and neighborhood analysis
* Co-occurrence patterns
* Spatial gene detection

Key idea: single-cell resolution enables detailed spatial insights.

---

## Methods Used

* Preprocessing and normalization
* PCA and UMAP
* Leiden clustering
* Spatial visualization
* Image segmentation and feature extraction
* Spatial graph analysis
* Co-occurrence and enrichment
* Moran’s I

---

## Key Insights

* Spatial transcriptomics links gene expression with tissue structure
* Image data adds extra biological context
* Different technologies provide different levels of detail
* Spatial analysis reveals interactions between cell populations
