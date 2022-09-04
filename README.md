# Module 18 Challenge - Cryptocurrencies

## Overview of the Project

### Purpose
The purpose of this project is to perform a K-Means analysis on the cryptocurrencies dataset provided. Our client, Accountability Accounting, has requested a report of what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for a new cryptocurrency investement portfolio.

## Results

### Deliverable 1 - Preprocessing the Data for PCA
The image below shows our crypto_df DataFrame before transforming the "Algorithm" and "ProofType" columns into dummy variables. We then use the StandardScaler method to standardize the features that will be used during PCA.
![Del1](https://user-images.githubusercontent.com/103288980/188291657-bc1e8f9e-06b8-4c98-8c12-a137e7038a79.PNG)

### Deliverable 2 - Reducing Data Dimensions Using PCA
The image below shows the resulting PCA columns for our standardized DataFrame. At this stage, the data has been reduced to three principal components.
![Del2](https://user-images.githubusercontent.com/103288980/188291659-1c17f3c3-d85a-4f12-b7f0-5c1d392f552a.PNG)

### Deliverable 3 - Clustering Cryptocurrencies Using K-Means
As we do not know the output for what our client is looking for, our model uses the K-Means clustering algorithm for unsupervised learning. To determine our clusters, our program generated the Elbow curve seen below. Using this plot, we have decided run the K-Means model for k=4 clusters. The results have been aggregated into the clustered_df DataFrame pictured below.
![Del3-elbow](https://user-images.githubusercontent.com/103288980/188291666-3e3a8df2-cf4a-4018-9c8e-dbb5a1fc3c85.PNG)

![Del3](https://user-images.githubusercontent.com/103288980/188291662-1981fba9-0f6b-4a0e-bbfc-020dd501a3e2.PNG)

### Deliverable 4 - Visualizing Cryptocurrencies Results
Using the clustered_df from the previous deliverable, our program generates a 3D plot based on the three PC columns in the DataFrame. Finally, our program generates a 2D scatterplot based on a standardized "TotalCoinSupply" and "TotalCoinsMined" columns. Both graphs are customized to display information when you hover over a data point.
![Del4-3d](https://user-images.githubusercontent.com/103288980/188291671-f9974d34-3bdc-46ef-ac54-16c433c4e6df.PNG)

![Del4-2d](https://user-images.githubusercontent.com/103288980/188291672-2bfa1a43-4d86-44c1-baf7-71d49349b83f.PNG)

## Summary
In summary, our analysis has found 4 potential classification groups based. Our algorithm makes predictions on which group to classify each cryptocurrency. The results are collected in the clustered_df printed on Deliverable 3.

### Recommendations
Our algorithm could be improved by testing other number of clusters in our K-means analysis step. The Elbow Curve generated from the pcs_df DataFrame suggests that we could repeat our analysis with k=5 or k=6 clusters.
