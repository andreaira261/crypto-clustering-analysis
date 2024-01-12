# Crypto Clustering Analysis 

## Overview
In this assignment, unsupervised learning techniques were applied to analyze and predict the impact of 24-hour and 7-day price changes on cryptocurrencies.

## Languages/ Tools: 
  - Python
  - Pandas
  - HoloViews
  - scikit-learn

## Preparing the Data
The data was prepared by using the `StandardScaler()` module to normalize the data.

<img width="1372" alt="data-prep" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/b2ca5e0d-4d32-48d1-88a2-9d6bd7b41659">

## Finding the Best Value for k Using the Original Data
In this section, the elbow method algorithm was used to find the best value for `k`. 

<img width="1347" alt="k-orig-1" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/13c86c73-39d2-46d5-b36e-5e8489cdffca">

A line chart was plotted to visually identify the optimal value for `k`. 

<img width="736" alt="k-orig-2" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/023bd451-0b97-478b-9c00-75794d187cd2">

It was determined that the best value to use for `k` was 3. 

## Clustering Cryptocurrencies with K-means Using the Original Data
In this section, the K-means model was initialized with 3 clusters. The model was fitted using the original data, and the clusters were predicted to group the cryptocurrencies.

<img width="1376" alt="predict-orig-1" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/8d0d3cd4-56e6-447f-82cb-a435ababe83b">

A scatterplot was then created by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. The graph points are colored with labels based on the clusters found using K-means. The cryptocurrency name is displayed on hover to identify each data point. 

<img width="722" alt="predict-orig-2" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/64f24317-bdf7-4e6f-9333-fe40322798f1">

## Optimizing the Clusters with Principal Component Analysis (PCA)
An instance of a PCA model was created with `n_components=3`. The model was then used to reduce the features to three principal components.

<img width="1373" alt="optimize-pca-1" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/e4832a43-23bf-4208-8d00-69fc42bde5e5">

A new DataFrame was created with the PCA data.

<img width="1376" alt="optimize-pca-2" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/479112eb-1166-4da6-8cce-3cba14e2829b">

## Finding the Best Value for k Using the PCA Data 
The elbow method algorigthm was repeated using the PCA data to find the best value for `k`. 

<img width="726" alt="k-pca" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/fc3f5f0b-f313-4d39-81f1-40345c8a810c">

It was determined that the best value to use for `k` was 3. 

## Clustering Cryptocurrencies with K-means Using the PCA Data
The K-means model was initialized again with 3 clusters. The model was fitted using the PCA data, and the clusters were predicted to group the cryptocurrencies.

Another scatterplot was then created by setting `x="PCA1"` and `y="PCA2"`. The graph points are colored with labels based on the clusters found using K-means. The cryptocurrency name is displayed on hover to identify each data point.

<img width="722" alt="predict-pca" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/80448a76-cef1-4d3b-8266-e5fd0920a9b6">

## Visualizing and Comparing the Results 
The impact of using fewer features to cluster the data using K-means include making the clusters more visually distinguishable. It appears that the predicted clusters using the original data with all of the factors yielded similar results from the PCA analysis; however in the second plot that resulted from the PCA data, the clusters appear to be more compact and distinct compared to the plot created from the original data. 

<img width="1425" alt="k-compare" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/5dcf2967-5ebd-4ebf-8826-21187853c964">

<img width="1417" alt="cluster-compare" src="https://github.com/andreaira261/crypto-clustering-analysis/assets/48165713/81a3b446-bc7f-4f3c-ab9a-7885d717f314">



