# AIPROJECT.286981
# SHOPEASY PROJECT

# AIPROJECT.286981
# SHOPEASY PROJECT

## - Team Members
- Lucrezia Salerno 
- Elisa Presciutti
- Irma Di Nallo

##  - Introduction and Description
The goal of this project is to leverage the extensive user data collected by ShopEasy, a leading e-commerce platform, to understand customer buying habits and behaviors. By performing segmentation on this dataset, we aim to uncover hidden patterns that will help ShopEasy provide personalized user experiences, special promotions, and improved services.

The project involves an in-depth analysis of the ShopEasy dataset, starting with an understanding of the column meanings. To achieve this, we import several key libraries: NumPy, Pandas, and Matplotlib. These libraries are essential for data manipulation, analysis, and visualization.
Our base step is to import the dataset ‘shopeasy.csv’, which contains 21 columns, and obtain an overview of its structure using Pandas. This involves inspecting the dataset's basic information to comprehend its layout and content.
By following these steps, we aim to ensure a comprehensive understanding of the ShopEasy dataset for further analysis and insights.


## - Methods
The primary step in our analysis is conducting thorough Exploratory Data Analysis (EDA). EDA helps us understand the dataset by analyzing each column to discern the type of data it contains and its relevance to e-commerce user behavior. We ensure data integrity by checking for missing values, duplicates, and anomalies. For this purpose, we use a matrix plot to visualize missing data and assess its extent. Additionally, we employ various plotting techniques such as pair plots and count plots to delve deeper into the relationships between variables. These visualizations aid in identifying patterns and insights that are crucial for understanding the dataset and its implications for e-commerce user behavior.

![Alt text](/images/correlation.png )

In this project, we apply three clustering methods—K-means, Hierarchical Clustering, and DBSCAN—to the ShopEasy dataset to segment users based on various factors. Each method offers unique advantages and insights, and their performance is evaluated using metrics such as the Silhouette score, Calinski-Harabasz index, and Davies-Bouldin index.

The combination of these clustering techniques ensures that the best possible approach is utilized for segmenting the ShopEasy customer base, providing valuable insights for enhancing the user experience and driving business growth.


## - Experimental Design 
K-means clustering is employed to segment users based on a variety of factors, such as purchase history, spending patterns, and product preferences. This method partitions the dataset into a predefined number of clusters by minimizing the variance within each cluster. It is a strategic tool for understanding and categorizing customer behavior, facilitating targeted marketing, personalized services, and informed business decision-making. The effectiveness of K-means is compared with other clustering techniques to ensure the optimal approach for the dataset. We used also the Elbow Method which is a technique used in clustering analysis to determine the optimal number of clusters (k) in a dataset. It helps identify the point at which adding more clusters does not significantly improve the variance reduction within clusters.

![Alt text](/images/elbow.png )
![Alt text](/images/kmeans.png )


Hierarchical clustering does not require pre-specifying the number of clusters. Instead, it builds a hierarchy of clusters through either agglomerative (bottom-up) or divisive (top-down) approaches. This method is particularly useful for understanding the underlying data structure and provides a detailed and nuanced view of the dataset. We used dendrogram, a tree-like diagram used to illustrate the arrangement of the clusters produced by hierarchical clustering. It visually represents the process of clustering data points in a hierarchical manner and to choose the number of clusters, you can make a horizontal cut through the dendrogram, the number of branches intersected by the cut indicates the number of clusters.

![Alt text](/images/dendrogram.png )
![Alt text](/images/hierarchical.png )

DBSCAN is applied to effectively handle outliers and identify clusters of arbitrary shapes. This method clusters points based on the density of their local neighborhoods and does not require specifying the number of clusters in advance. DBSCAN is especially valuable for datasets with noise and complex cluster shapes.

![Alt text](/images/DBSCAN.png )

Then we used the chosen evaluation metrics —Silhouette Score, Calinski-Harabasz Index, and Davies-Bouldin Index— to provide a comprehensive assessment of clustering quality. The Silhouette Score focuses on cohesion and separation, the Calinski-Harabasz Index balances compactness and separation, and the Davies-Bouldin Index evaluates cluster similarity. These metrics collectively ensure a robust and reliable evaluation of the clustering methods applied to the ShopEasy dataset.


## - Interpretation of Results 
 Silhouette Index:
- Measures how similar an object is to its own cluster compared to other clusters.
- Ranges from -1 to 1, where a higher value indicates better clustering performance.
 = DBSCAN has the highest Silhouette Index (0.251), indicating the best clustering quality among the three methods.

 Calinski-Harabasz Index:
- Measures the ratio of the sum of between-cluster dispersion to within-cluster dispersion.
- Higher values indicate better-defined clusters.
 = K-means has the highest Calinski-Harabasz Index (1465.278), suggesting it has well-separated and compact clusters compared to the other methods.

 Davies-Bouldin Index:
- Evaluates the average similarity ratio of each cluster with its most similar cluster.
- Lower values indicate better clustering performance.
 = DBSCAN has the lowest Davies-Bouldin Index (0.959), indicating the clusters are well-separated and less similar to each other.



 K-means Clustering:
Pro: High Calinski-Harabasz Index indicates well-defined clusters.
Cons: Low Silhouette Index and moderate Davies-Bouldin Index suggest that clusters might not be as distinct or well-separated as desired.

 DBSCAN:
Pro: Highest Silhouette Index and lowest Davies-Bouldin Index indicate high-quality clustering with well-separated clusters. It effectively handles outliers and clusters of arbitrary shapes.
Cons: Low Calinski-Harabasz Index might suggest less compact clusters, but this is often acceptable given DBSCAN's strength in handling noise and complex cluster shapes.

 Hierarchical Clustering: 
Pro: Moderate Calinski-Harabasz Index indicates reasonable cluster definition.
Cons: Lowest Silhouette Index and highest Davies-Bouldin Index suggest poor clustering quality and less distinct clusters compared to the other methods.



## - Conclusions 
Given the results, DBSCAN emerges as the best method for our problem purpose. It has the highest Silhouette Index and the lowest Davies-Bouldin Index, indicating superior clustering performance with well-separated and distinct clusters. Despite its lower Calinski-Harabasz Index, DBSCAN's ability to handle outliers and identify clusters of arbitrary shapes makes it particularly suitable for the ShopEasy dataset, which might contain noise and complex patterns in customer behavior.

This characteristic of DBSCAN proves especially valuable in the e-commerce domain where customer behaviours and interactions can form complex, non-linear patterns that are not adequately captured by more traditional clustering methods like K-means.

The insights derived from the clustering analysis have significant implications for targeted marketing strategies and customer relationship management in e-commerce. By understanding the distinct segments within the customer base, businesses can tailor their marketing efforts more effectively, personalise customer experiences, and ultimately drive better business outcomes.

