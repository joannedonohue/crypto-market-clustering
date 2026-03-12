# Crypto Market Clustering

Unsupervised machine learning analysis of cryptocurrency price behavior — using K-Means clustering and PCA dimensionality reduction to identify distinct market segments across 24-hour and 7-day price change patterns.

## Overview

This project applies clustering techniques to answer a practical question: do cryptocurrencies naturally group into behavioral segments based on short-term price volatility? The analysis compares cluster quality with and without PCA, demonstrating how dimensionality reduction affects both model performance and interpretability.

## Key Findings

- Optimal cluster count: **k = 4** (identified via elbow method)
- PCA reduced features to 3 components capturing ~90% of total variance
- Four behavioral clusters identified: stable, high-volatility, moderate-growth, and outlier coins
- PCA-reduced clustering produced tighter, more interpretable groupings

## Methodology

1. Normalized price change data using StandardScaler
2. Applied elbow method to identify optimal k
3. Fit K-Means on original feature set; visualized clusters with hvPlot
4. Reduced dimensionality with PCA; re-ran K-Means on 3 principal components
5. Compared inertia and cluster separation between both approaches

## Stack

Python | scikit-learn | pandas | hvPlot | PCA | K-Means

## Usage

Run: pip install -r requirements.txt
Then: jupyter notebook crypto_investments.ipynb
