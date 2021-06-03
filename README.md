# K- Means and PCA on Pokemon 
## Clustering :fire:
**Clustering** is one of the most common exploratory data analysis technique used to get an intuition about the structure of the data. It can be defined as the task of identifying subgroups in the data such that data points in the same subgroup (cluster) are very similar while data points in different clusters are very different. In other words, we try to find homogeneous subgroups within the data such that data points in each cluster are as similar as possible according to a similarity measure such as euclidean-based distance or correlation-based distance. The decision of which similarity measure to use is application-specific.
Unlike supervised learning, clustering is considered an unsupervised learning method since we don’t have the ground truth to compare the output of the clustering algorithm to the true labels to evaluate its performance. We only want to try to investigate the structure of the data by grouping the data points into distinct subgroups.

---
### K-means is one of the clustering algorithms commonly used 

---

##  Kmeans Algorithm :zap:
**Kmeans** algorithm is an iterative algorithm that tries to partition the dataset into _K_pre-defined distinct non-overlapping subgroups (clusters) where each data point belongs to **only one group**. It tries to make the intra-cluster data points as similar as possible while also keeping the clusters as different (far) as possible. It assigns data points to a cluster such that the sum of the squared distance between the data points and the cluster’s centroid (arithmetic mean of all the data points that belong to that cluster) is at the minimum. The less variation we have within clusters, the more homogeneous (similar) the data points are within the same cluster.
The way kmeans algorithm works is as follows:

1.  Specify number of clusters _K_.
2.  Initialize centroids by first shuffling the dataset and then randomly selecting _K_ data points for the centroids without replacement.
3.  Keep iterating until there is no change to the centroids. i.e assignment of data points to clusters isn’t changing.

-   Compute the sum of the squared distance between data points and all centroids.
-   Assign each data point to the closest cluster (centroid).
-   Compute the centroids for the clusters by taking the average of the all data points that belong to each cluster.

> The approach kmeans follows to solve the problem is called **Expectation-Maximization**. The E-step is assigning the data points to the closest cluster. The M-step is computing the centroid of each cluster.

# Dataset 
The dataset contains information about pokemon and their basic attributes such as attack, defense. 

# Conclusion :soccer:
After applying kmeans to the dataset, the optimal amount of clusters was 4. This is different from the expected 3. From this we find that 3 clusters are for those pokemon that have 3 stages of evolution, where as the other cluster contains all pokemon with 2 stages of evolution 
