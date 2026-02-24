# Dundalk Land Cover Analysis: Supervised & Unsupervised Models

This repository contains Jupyter Notebooks for analyzing land cover in Dundalk, Ireland, using **Sentinel-2 satellite imagery**. The project explores two different machine learning methodologies—unsupervised spectral index analysis and supervised classification using labeled geospatial data.

## Project Overview

The project aims to classify various land cover types (e.g., Vegetation, Urban, Water, and Soil) by processing multispectral data from a Sentinel-2 image (`Dundalk_Sentinel2_2023.tif`).

### Key Features
* **Spectral Index Calculation:** Automated generation of NDVI, NDBI, and NDWI.
* **Multispectral Processing:** Extraction and normalization of specific bands including Red (B4), Green (B3), NIR (B8), and SWIR (B11/B12).
* **Hybrid Approach:** Comparison between index-based visualization (unsupervised) and polygon-based training (supervised).

---

## Repository Contents

### 1. `Dundalk_Unsupervised_Model.ipynb`
This notebook focuses on **Exploratory Data Analysis (EDA)** and unsupervised visualization.
* **Technique:** Uses mathematical indices to differentiate land features without pre-labeled data.
* **Outputs:** Generates color-coded heatmaps for:
    * **NDVI** (Vegetation health)
    * **NDBI** (Built-up/Urban areas)
    * **NDWI** (Water bodies)

### 2. `Dundalk_Supervised_Model.ipynb`
This notebook implements a **Supervised Classification** workflow.
* **Training Data:** Utilizes GeoJSON files (`Green_polygons.geojson`, `Soil_polygons.geojson`, etc.) as ground truth labels.
* **Class Mapping:**
    * **Class 1:** Vegetation
    * **Class 2:** Soil
    * **Class 3:** Urban
    * **Class 4:** Water
* **Workflow:** Rasterizes vector polygons to align with satellite bands for model training.

---

## Technical Requirements

The notebooks are designed to run in a Python environment (such as Google Colab or Jupyter).

### System Dependencies
* `gdal-bin`
* `python3-gdal`

### Python Libraries
* `rasterio` (Satellite image processing)
* `geopandas` (Geospatial vector data handling)
* `numpy` & `pandas` (Data manipulation)
* `matplotlib` (Visualization)

---
