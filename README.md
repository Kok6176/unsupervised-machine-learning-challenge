# unsupervised-machine-learning-challenge
This is Kokila's Unsupervised ML challenge 

## Part 1: Prepare the Data
* Read myopia.csv into a Pandas DataFrame.
* Remove the "MYOPIC" column from the dataset.
Note: The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already!
* Standardize your dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

## Part 2: Apply Dimensionality Reduction
* Perform dimensionality reduction with PCA. How did the number of the features change?
    * How do you interpret the explained variance ratio in PCA? The explained variance ratio is the percentage of variance that is attributed by each of the selected components. Ideally, you would choose the number of components to include in your model by adding the explained variance ratio of each component until you reach a total of around 0.8 or 80% to avoid overfitting.
    * From the above attributes array the sum for my pca is 0.83185295, which is 0.8 or 80 percentile value indicating that my data is not a overfitting one.
* Further reduce the dataset dimensions with t-SNE and visually inspect the results. To do this, run t-SNE on the principal components, which is the output of the PCA transformation.
* Create a scatter plot of the t-SNE output. Are there distinct clusters?
    * By looking at the scatter plot after performing the t-sne on the myopia dataset do not show any distinct clusters.    

## Part 3: Perform a Cluster Analysis with K-means
* Create an elbow plot to identify the best number of clusters. Make sure to do the following:
    * Use a for loop to determine the inertia for each k between 1 through 10.
    * If possible, determine where the elbow of the plot is, and at which value of k it appears.

## Part 4: Make a Recommendation
Based on your findings, write up a brief (one or two sentences) recommendation for your supervisor in your Jupyter Notebook. Can the patients be clustered? If so, into how many clusters?
    * Myopia Clusters Findings
After Preparing the Data, Applying Dimensionality Reduction using PCA and reducing this further with t-SNE I performed a Cluster Analysis with K-Means model. My findings are:
The optimal number of clusters seems to be 3
t-SNE was not helpful in finding clusters, there was some some difference after adjusting perplexity but this could be due to random noise.

k-means cluster analysis is an algorithm that groups similar objects into groups called clusters. The endpoint of cluster analysis is a set of clusters, where each cluster is distinct from each other cluster, and the objects within each cluster are broadly similar to each other.
I found some patterns or clusters after performing the K-Means clustering the dataset does not form any distinct clusters so say with one centroid for each cluster. Instead the clusters are overlapping with each other indicating that there is no specfic centroid for each cluster and with so many outliers.

# Conclusion
Either the dataset is insufficient or K-means clustering is not a right model to be used on this myopia dataset.
