# used_car_clustering

## Overview
  * Craigslist is the world's largest collection of used vehicles for sale. 
  * Grouping cars using unsupervised learning methods as a precursor to building a recommendation system.
  * Tried three different clustering methods. 
  * Used visual representations and the cluster’s silhouette score metrics to compare results of the different clustering methods. 
  
## Data Description
  * The dataset can be found at https://www.kaggle.com/austinreese/craigslist-carstrucks-data
  * Vehicles from all regions of the US were scraped from Craigslist.
  * The dataset had over 400,000 observations.
  * I took a sample of 6,000 observations after data cleaning and feature engineering. 
  * The variables I used to cluster the cars were price, year, condition, cylinders, odometer, drive (fwd, rwd, 4wd), type (sedan, truck, SUV, ect).
  * All the variables were made categorical and dummified. 

## Unsupervised Methods Used

### Hierarchical Clustering
* Not the best results with this method. 
* Silhouette Score: -0.083
* Looking at 2D representation of cluster below:
  * Uneven cluster distribution (almost 4300/6000 in cluster 0)
  * No clear groupings (purple and blue scattered)

#### Hierarchical Cluster Dimension Reduction with UMAP
<img src='imgs/heir umap.png' width='70%' align='center' title='Dimension Reduction with UMAP'>

#### Hierarchical Clusters
<img src='imgs/hier clusters.png' width='30%' align='center' title='Hierarchical clusters'>



### DBSCAN Clustering
* Even worse results that Hierarchical with DBSCAN. 
* Silhouette Score: -0.0045
* Looking at 2D representation of cluster below:
  * One giant cluster (cluster 0)
  * A few in cluster 1 and a a few with no cluster.

#### DBSCAN Cluster Dimension Reduction with UMAP
<img src='imgs/dbscan umap.png' width='70%' align='center' title='Dimension Reduction with UMAP'>

#### DBSCAN Clusters
<img src='imgs/dbscan clusters.png' width='30%' align='center' title='DBSCAN clusters'>



### K-Medoids Clustering
* Much better results than previous clustering methods. 
* Silhouette Score: 0.198
* Looking at 2D representation of cluster below:
  * We can see groupings more clearly
  * A more even distribution of clusters

#### K-Medoids Cluster Dimension Reduction with UMAP
<img src='imgs/kmeds umap.png' width='70%' align='center' title='Dimension Reduction with UMAP'>

#### K-Medoids Clusters
<img src='imgs/kmeds clusters.png' width='30%' align='center' title='KMedoids clusters'>



## K-Medoids Cluster Analysis

#### K-Medoids Charactersitics by Proportion

<img src='imgs/clust chars.png' width='70%' align='center' title='Cluster Charactersitics by Proportion'>

#### K-Medoids Cluster names and Desriptions
<img src='imgs/kmeds_clust_names.png' width='70%' align='center' title='Cluster names'>
