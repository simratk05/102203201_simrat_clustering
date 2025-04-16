# Comparative Performance Study of Clustering Algorithms on the Iris Dataset
**Overview -**
This project presents a comparative analysis of different clustering algorithms using various preprocessing techniques and cluster numbers, evaluated across several performance metrics. The Iris dataset from the UCI Machine Learning Repository is used as the benchmark. The study aims to highlight how preprocessing and algorithm choice impact clustering quality.
Dataset: Iris

**Methodology -**
Preprocessing Techniques
No Data Processing: Raw features

Normalization: MinMaxScaler

Transform: StandardScaler

PCA: Principal Component Analysis (2 components)

T+N: StandardScaler after MinMaxScaler

T+N+PCA: PCA after both scaling methods

**Clustering Algorithms -**
K-Means Clustering

Agglomerative (Hierarchical) Clustering

K-Means Shift Clustering

**Cluster Numbers -**
Experiments conducted with c = 3, 4, 5 clusters (where applicable)

**Evaluation Metrics -**
Silhouette Score: Measures cluster cohesion and separation (higher is better)

Calinski-Harabasz Index: Ratio of between-cluster to within-cluster dispersion (higher is better)

Davies-Bouldin Index: Average similarity between clusters (lower is better)

**Results -**

![image](https://github.com/user-attachments/assets/838b9c98-84df-4d96-ba81-ae51dd3e8b80)

![image](https://github.com/user-attachments/assets/73eae9e2-fabc-41b2-a31a-f94a04bc36ae)

![image](https://github.com/user-attachments/assets/1901fa45-0366-4f91-a551-8d15eef42944)


**Findings -**
Preprocessing significantly affects clustering performance. Normalization and combined scaling (T+N) often improved metrics over raw data.

K-Means generally achieved the best Silhouette and Calinski-Harabasz scores when the number of clusters matched the true class count (c=3).

Hierarchical Clustering was sensitive to preprocessing and sometimes produced degenerate clusters.

K-Mean Shift Clustering tended to find fewer clusters and was less sensitive to preprocessing, but sometimes failed to match the true cluster count.

Davies-Bouldin Index was lowest (best) for well-separated clusters, especially after normalization and PCA.
