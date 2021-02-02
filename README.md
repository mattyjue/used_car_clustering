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

<img src='imgs/heir umap.png' width='70%' align='left' title='Dimension Reduction with UMAP'>

<img src='imgs/hier clusters.png' width='70%' align='right' title='Dimension Reduction with UMAP'>

### Hierarchical Clustering
* Even worse results that Hierarchical with DBSCAN. 
* Silhouette Score: -0.0045
* Looking at 2D representation of cluster below:
  * One giant cluster (cluster 0)
  * A few in cluster 1 and a a few with no cluster.

<img src='imgs/dbscan umap.png' width='70%' align='left' title='Dimension Reduction with UMAP'>

<img src='imgs/dbscan clusters.png' width='70%' align='reight' title='Dimension Reduction with UMAP'>
