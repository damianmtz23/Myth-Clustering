# Myth Clustering with TF-IDF and K-Means

A digital humanities project that uses TF-IDF and k-means clustering to group myth passages by shared themes and compare patterns across texts.

## Overview

This project treats a small, hand-picked set of 15 Greek and Roman myth passages as data and uses a simple machine learning workflow to explore thematic clustering.

The notebook:
- defines a corpus of 15 myth passages
- assigns theme tags such as xenia, hubris, fate, and loyalty
- builds TF-IDF vectors from passage text
- runs k-means clustering
- compares results for k = 3, 4, and 5
- checks silhouette scores across those k values as supporting evidence
- visualizes clusters with PCA

## Files

- `CC_303_Project.ipynb` — main notebook with code, analysis, and visualizations
- `CC 303 Project – Myth Clustering with TF-IDF and K-Means.pdf` — project commentary / written analysis

## Tools Used

- Python
- Google Colab
- scikit-learn
- pandas
- matplotlib

## Main Question

Can a simple clustering model group myth passages in ways that match literary themes like hospitality, pride, fate, punishment, loyalty, and gender roles?

## Results / Key Findings

- With k = 4, one cluster lines up with a recognizable theme: the Helios cattle, Sirens, and Scylla/Charybdis passages group together, all sharing tags like fate, temptation, and leadership failure — a "peril and fate at sea" cluster.
- Other clusters mix passages with different manually assigned theme tags — for example, Arachne's weaving contest (hubris) lands in the same cluster as several suitor-punishment passages (xenia, justice), and Niobe's grief (hubris, divine punishment) lands with hospitality and loyalty passages (Eumaeus, Argos). This shows that lexical similarity (what TF-IDF actually measures) does not always match literary theme.
- Cluster assignments shift noticeably between k = 3, 4, and 5, which is expected given how small the dataset is.
- Silhouette scores across k = 3, 4, and 5 are close to each other and modest in value, so they're treated as supporting evidence rather than a definitive way to pick the "best" k.
- Overall, this is a small exploratory exercise, not a validated model of mythological themes — it shows that TF-IDF + k-means can pick up on *some* thematic structure in the text, but it's an imperfect stand-in for human literary judgment.

## Notes

This project uses a small hand-built dataset of 15 selected passages from Homer’s *Odyssey* and Ovid’s *Metamorphoses*.

## Author

Damian Martinez
