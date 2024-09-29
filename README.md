# CryptoClustering
Module 19 Challenge

Prepare the Data

I Used the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

Find the Best Value for k Using the Scaled DataFrame

I used the elbow method to find the best value for k using the following steps:
I created a list with the number of k values from 1 to 11.
I created an empty list to store the inertia values.
I created a for loop to compute the inertia with each possible value of k.
I created a dictionary with the data to plot the elbow curve.
Ploted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.


Cluster Cryptocurrencies with K-means Using the Scaled DataFrame

I used the following steps to cluster the cryptocurrencies for the best value for k on the scaled DataFrame:
Initialised the K-means model with the best value for k.
Fit the K-means model using the scaled DataFrame.
Predicted the clusters to group the cryptocurrencies using the scaled DataFrame.
Created a copy of the scaled DataFrame and add a new column with the predicted clusters.
Created a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Colour the graph points with the labels found using K-means.
Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

Optimise Clusters with Principal Component Analysis

Using the original scaled DataFrame, I performed a PCA and reduced the features to three principal components.
I retrieved the explained variance to determine how much information can be attributed to each principal component and then answer the following questions:

What is the total explained variance of the three principal components?
I created a new DataFrame with the scaled PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

Find the Best Value for k Using the PCA DataFrame

I used the elbow method on the scaled PCA DataFrame to find the best value for k using the following steps:
Created a list with the number of k-values from 1 to 11.
Created an empty list to store the inertia values.
Created a for loop to compute the inertia with each possible value of k.
Created a dictionary with the data to plot the Elbow curve.
Ploted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answered the following question:
What is the best value for k when using the scaled PCA DataFrame?
Does it differ from the best k value found using the original scaled DataFrame?

i used the following steps to cluster the cryptocurrencies for the best value for k on the PCA DataFrame:
Initialised the K-means model with the best value for k.
Fit the K-means model using the scaled PCA DataFrame.
Predicted the clusters to group the cryptocurrencies using the scaled PCA DataFrame.
Created a copy of the scaled PCA DataFrame and add a new column to store the predicted clusters.
Created a scatter plot using hvPlot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Colour the graph points with the labels found using K-means.
Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

Answered the following question:
What is the impact of using fewer features to cluster the data using K-Means?
