# CryptoClustering

Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:
  - Create a list with the number of k values from 1 to 11.
  - Create an empty list to store the inertia values.
  - Create a for loop to compute the inertia with each possible value of k.
  - Create a dictionary with the data to plot the elbow curve.
  - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
  - Answer the following question: What is the best value for k?
      - The best value for k = 4.
   
Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
  - Initialize the K-means model with the best value for k.
  - Fit the K-means model using the original scaled DataFrame.
  - Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
  - Create a copy of the original data and add a new column with the predicted clusters.
  - Create a scatter plot using hvPlot as follows:
    - Set the x-axis as "PC1" and the y-axis as "PC2".
    - Color the graph points with the labels found using K-means.
    - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
   
Optimize Clusters with Principal Component Analysis
  - Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
  - Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question:
    - What is the total explained variance of the three principal components?
        - When adding the variance of the three principal components the answer is 0.8886218549859446 (0.34871677 + 0.31363391 + 0.22627118)
  - Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

Find the Best Value for k Using the PCA Data
  - Use the elbow method on the PCA data to find the best value for k using the following steps:
    - Create a list with the number of k-values from 1 to 11.
    - Create an empty list to store the inertia values.
    - Create a for loop to compute the inertia with each possible value of k.
    - Create a dictionary with the data to plot the Elbow curve.
    - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
    - Answer the following question:
      - What is the best value for k when using the PCA data?
        - The best value is k is 4
      - Does it differ from the best k value found using the original data?
        - No, it is the same k value result that was also found in the orginial data.
       
Cluster Cryptocurrencies with K-means Using the PCA Data
  - Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
    - Initialize the K-means model with the best value for k.
    - Fit the K-means model using the PCA data.
    - Predict the clusters to group the cryptocurrencies using the PCA data.
    - Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
    - Create a scatter plot using hvPlot as follows:
      - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
      - Color the graph points with the labels found using K-means.
      - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
    - Answer the following question:
      - What is the impact of using fewer features to cluster the data using K-Means?
        - The impact of using PCA data resulted in tighter and having more results within cluster 0 and 1 than the orginial anaylsis did.
