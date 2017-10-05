# Understanding-stock-data-by-Field-clustering-and-dimensionality
Cluster the different companies listed in SP500 and find the dimensionality of each stock price, thus explaining its variation

# Dependencies
1. PySpark
2. findspark

# Data

First, download data from this [link](https://drive.google.com/open?id=0B_Cz1ZeaITeDM196TnJnY24xMjA). Save it in the 
Data folder before running the code.

# Execution 

Run the .ipynb files as is. The outputs will be displayed inline

## 1. Prepare daily ratio file

Since the log of the daily ratio of the prices is a better indicator of a price change, we use that to power our analysis. We read it in, compute the ratio of prices, and save it to a Spark RDD dataframe for further analysis.

## 2. PCA of stocks

This file employs PCA  to cluster correlated variations in prices together. It is then visualized as a spatial distribution with 2D projections along the most significant eigen directions.

## 3. Dimensionality 

The intrinsic dimensionality (also called fractal dimension or Hausdorff dimesion) is found using a natively developed algorithm that tracks how frequent and by how much the signal changes. This gives an idea about the distribution of the variations and helps us to tie our results from #2.

All the obtained results are included in the ipynb files and in the Code/figs/ folder.
