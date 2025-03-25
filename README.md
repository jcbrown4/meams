# MEAM Emotion Clustering & Modeling

This repository contains the code and data used to explore how age and the thematic content of memories (derived from clustering) relate to mixed emotionality in autobiographical music-evoked memories.

## Overview

The analysis investigates whether age predicts the degree of emotional complexity (mixed emotions) recalled in MEAMs, and whether this relationship is moderated by thematic clusters derived from SBERT-embedded memory descriptions.

## File Structure

data/
    MEAMdata_complete.xlsx              - Full dataset with metadata, GoEmotion labels, age info
    SBERT/SBERT-L6-v2_embed.csv        - SBERT embeddings of memory descriptions

output/
    MEAM_fuzzy_clustered.csv           - Fuzzy cluster labels and memberships from UMAP features
    OLS_Regression_Results.xlsx        - Results of the regression model (Age × Theme → Mixed Emotions)

notebooks/
    Analysis2.ipynb                    - UMAP + Fuzzy C-Means clustering
    Model.ipynb                        - Regression model (OLS) on age, emotion count, and cluster

requirements.txt                       - Python package requirements
README.md                              - This file

## Method Summary

- UMAP is used to reduce SBERT embeddings to 2D space.
- Fuzzy C-Means clustering is applied to UMAP outputs (n=2–4 clusters).
- Mixed emotions are calculated as the count of GoEmotion-derived binary labels per memory.
- OLS regression tests whether Age × Cluster membership predicts mixed emotion scores.

## How to Run

1. Clone this repository.
2. Set up a virtual environment.
3. Install dependencies with:

    pip install -r requirements.txt

4. Open the notebooks in JupyterLab or Jupyter Notebook and run them step by step.

## Notes

- GoEmotion labels are used for the first iteration of mixed emotionality measurement.
- Future updates will incorporate self-reported emotion labels and memory age as a covariate.
