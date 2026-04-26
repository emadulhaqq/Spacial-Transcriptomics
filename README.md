Spatial Transcriptomics Analysis

This repository contains a set of Jupyter notebooks demonstrating different workflows for spatial transcriptomics data analysis using common Python tools such as Scanpy and Squidpy. Each notebook focuses on a specific 10x Genomics technology and highlights key analysis steps, visualization methods, and biological insights.

Overview

The project includes four notebooks, each working with a different spatial dataset:

Basic Spatial Analysis (Scanpy) — Human lymph node dataset using Visium
Fluorescence Analysis (Squidpy) — Mouse brain with fluorescence channels
H&E Analysis (Squidpy) — Mouse brain tissue with spatial statistics
Xenium Analysis (Squidpy + SpatialData) — Human lung cancer at single-cell resolution

These workflows cover preprocessing, clustering, spatial visualization, and advanced spatial analysis techniques.

Project Structure
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
Setup Instructions
Requirements
Python 3.9 or higher
pip or conda
Installation
git clone https://github.com/<your-username>/spatial-transcriptomics.git
cd spatial-transcriptomics

pip install -r requirements.txt

jupyter notebook notebooks/
Notebook Summaries
1. Basic Spatial Analysis (Scanpy)

This notebook demonstrates a standard spatial transcriptomics workflow:

Data loading and quality control
Normalization and feature selection
PCA, neighborhood graph construction, and UMAP visualization
Clustering using Leiden algorithm
Identification of marker genes
Spatial mapping of clusters onto tissue images

Key takeaway:
Distinct spatial clusters correspond to biological regions, and marker genes help identify cell types.

2. Visium Fluorescence Analysis

This notebook integrates image data with gene expression:

Visualization of fluorescence channels (DAPI, neuronal, glial markers)
Image smoothing and segmentation
Extraction of image-based features (intensity, texture, counts)
Clustering based on image features
Comparison between image-derived and gene-derived clusters

Key takeaway:
Image features can reveal additional structure not captured by gene expression alone.

3. Visium H&E Analysis

This workflow focuses on spatial relationships between cell populations:

Extraction of image features from histology images
Construction of spatial neighbor graphs
Neighborhood enrichment analysis
Co-occurrence analysis across distances
Ligand-receptor interaction inference
Identification of spatially variable genes using Moran’s I

Key takeaway:
Spatial statistics help uncover interactions and organization within tissue.

4. Xenium Data Analysis

This notebook works with high-resolution single-cell spatial data:

Data loading and preprocessing
Dimensionality reduction and clustering
Spatial visualization of clusters
Centrality and neighborhood analysis
Co-occurrence patterns
Detection of spatially variable genes

Key takeaway:
Single-cell spatial data enables fine-grained analysis of tissue architecture and cellular interactions.

Summary of Methods

Across all notebooks, the following techniques are used:

Data preprocessing (filtering, normalization, feature selection)
Dimensionality reduction (PCA, UMAP)
Clustering (Leiden algorithm)
Spatial visualization
Image analysis (segmentation, feature extraction)
Spatial graph analysis
Co-occurrence and neighborhood enrichment
Spatial autocorrelation (Moran’s I)
Key Insights
Spatial transcriptomics reveals how gene expression is organized within tissue
Image-based features complement molecular data
Different technologies provide different resolutions and insights
Advanced spatial statistics help identify interactions between cell populations
