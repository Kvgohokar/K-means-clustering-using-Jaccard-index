# Document Clustering Using K-Means with Jaccard Index
This repository contains the implementation and results of a document clustering project using K-means clustering with the Jaccard index as the similarity measure. The project aims to cluster documents from three datasets: Enron Emails, NIPS full papers, and KOS blog entries, and determine an optimum value of K for each dataset.

## Methodology Overview
### Jaccard Index
The Jaccard index is utilized as the similarity measure between two documents. Unlike traditional bag-of-words models, the Jaccard index considers documents as sets of words, focusing on the intersection and union of words present in both documents.

### Custom K-Means Implementation
Since the default K-means implementation in Scikit-learn does not support Jaccard distance, a custom function for K-means clustering along with a custom Jaccard distance function was developed. The custom K-means algorithm initializes clusters by selecting random documents as initial centroids and iteratively assigns documents to clusters based on the minimum Jaccard distance from the centroids. Stopping criteria for the algorithm include a maximum iteration limit and a threshold based on the average Jaccard distance between new and current centroids.

### Determining Optimal K
The optimal value of K is identified by plotting the total variation (total sum of Jaccard distances of each point in a cluster from its centroid) against different values of K. The value of K where the total variation exhibits diminishing returns is considered the optimal K.

## Conclusion
In this project, we successfully applied K-means clustering with the Jaccard index as the similarity measure to cluster documents.
Overall, this project highlights the effectiveness of leveraging custom implementations and domain-specific similarity measures in document clustering tasks. Future work could explore alternative clustering algorithms and similarity measures to further enhance clustering performance and scalability.
