# Cryptocurrency Price Change Prediction 

## Background:

In this project,I will be using Python and unsupervised learning techniques to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.I will be using the K-means clustering algorithm to group cryptocurrencies based on their price change percentages.

## Getting Started:

### Data Preparation

To prepare the data,I will use the ***StandardScaler() module*** from ***scikit-learn*** to normalize the data from the CSV file. We will create a DataFrame with the scaled data and set the ***"coin_id"*** index from the original DataFrame as the index for the new DataFrame.

### Option 1 :

### Finding the Best Value for k Using the Original Scaled DataFrame

I will use the ***elbow method*** to find the best value for k using the following steps:

*	Create a list with the number of k values from 1 to 11.
*	Create an empty list to store the inertia values.
*	Create a for loop to compute the inertia with each possible value of k.
*	Create a dictionary with the data to plot the elbow curve.
*	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k

![Screenshot 2023-04-23 063153](https://user-images.githubusercontent.com/113273722/233835042-bc0b69ec-6bd2-4f47-97b3-f9fbbe7987ad.png)

### Clustering Cryptocurrencies with K-means Using the Original Scaled Data

I will use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

*	Initialize the K-means model with the best value for k.
*	Fit the K-means model using the original scaled DataFrame.
*	Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
*	Create a copy of the original data and add a new column with the predicted clusters.
*	Create a scatter plot using ***hvPlot/plotly.express***

![Screenshot 2023-04-23 064550](https://user-images.githubusercontent.com/113273722/233835335-ae0c2cea-48af-4462-83c5-03243061051f.png)

### Option 2 :

### Optimizing Clusters with Principal Component Analysis

Using the original scaled DataFrame, I will perform a ***PCA*** and reduce the features to three principal components.I will retrieve the explained variance to determine how much information can be attributed to each principal component. Then I will create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Finding the Best Value for k Using the PCA Data

I will use the elbow method on the PCA data to find the best value for k using the following steps:
*	Create a list with the number of k-values from 1 to 11.
*	Create an empty list to store the inertia values.
*	Create a for loop to compute the inertia with each possible value of k.
*	Create a dictionary with the data to plot the Elbow curve.
*	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![Screenshot 2023-04-23 065520](https://user-images.githubusercontent.com/113273722/233835820-04f79620-e953-4fad-ba51-7be20230f2db.png)

### Clustering Cryptocurrencies with K-means Using the PCA Data

I will use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
*	Initialize the K-means model with the best value for k.
*	Fit the K-means model using the PCA data.
*	Predict the clusters to group the cryptocurrencies using the PCA data
* Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters
*Create a scatter plot using ***hvPlot/plotly.express-3D***

![Screenshot 2023-04-23 070204](https://user-images.githubusercontent.com/113273722/233836110-f0cc866e-d3fc-43e5-8c00-fcfecbb476ac.png)

## Conclusion

this project demonstrated how unsupervised learning and clustering can be used to gain insights into a datasets of cryptocurrency price data. Future work could involve exploring additional clustering algorithms or incorporating additional features into the analysis to improve the accuracy of the clustering



