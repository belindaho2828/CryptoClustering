# Overview #
This project focuses on clustering cryptocurrencies using K-Means clustering. The analysis involves scaling the data, determining the optimal number of clusters, and visualizing the clusters. Additionally, Principal Component Analysis (PCA) is applied to reduce the dimensionality of the data and observe the impact on clustering results.

# Tools Used #
Python: Primary programming language.


pandas: Data manipulation and analysis.


scikit-learn:
    StandardScaler: Data normalization.
    Means: Clustering.
    PCA: Dimensionality reduction.


hvPlot: Interactive visualizations.



# K-Means Clustering #
K-Means partitions data into k clusters by iteratively assigning data points to the nearest centroid and updating centroids based on the assigned points.

# Principal Component Analysis (PCA) #
PCA reduces data dimensions by transforming features into principal components, retaining most of the data's variance.

# Results #

## Clustering ##
Original Data: Used elbow method to find k=4.
PCA Data: Reduced to three components, k=4.

## Analysis ##
Elbow curves were similar for both methods.
Clusters mostly matched, with minor differences.
PCA clustering had two closer clusters and two far outliers. Original clustering had one far outlier, with potential cluster overlap.

## Data Preparation ##
Used StandardScaler() to normalize data and then created a scaled DataFrame 

## Optimal Value for k ##
Original Data: Used elbow method to determine k.
PCA Data: Applied PCA, then used elbow method to find k.

## Clustering and Visualization ##
### Visual Analysis ###
The elbow curve for both original K-Means and PCA did not change significantly.
Clusters were mostly the same, with slight variations:
Cluster 0: 26 different datapoints
Cluster 2: 13 different datapoints
Cluster 3: 1 different datapoint

### Optimization Impact: ###
PCA clustering showed two clusters much closer together, resulting in two far outliers.
Original K-Means clustering had one far outlier, with cluster 1 potentially grouped with cluster 0 without significant difference.
PCA made outliers in clusters 1 and 3 more distinct, justifying their inclusion in clusters 0 and 2, respectively.