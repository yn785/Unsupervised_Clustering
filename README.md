# Project README

## Introduction

This project involves data preprocessing and clustering analysis on the Online Retail dataset. The dataset contains information about customer transactions, including invoice details, product information, and customer demographics.

## Dependencies

The following dependencies are required to run the code:
- pandas
- numpy
- sklearn
- seaborn
- matplotlib
- yellowbrick

## Data Preprocessing

1. Reading the dataset: The dataset is read from the 'OnlineRetail.csv' file using pandas. Encoding is handled based on the file's format (utf-8 or latin-1).

2. Handling missing values: Missing values in the 'Description' column are replaced with NaN values. Empty cells and spaces are also replaced with NaN using the `replace()` function.

3. Removing rows with missing CustomerID: Rows with missing CustomerID values are dropped from the dataset using the `dropna()` function.

4. Data transformation: The 'InvoiceDate' column is converted to datetime format. Additional date and time features are extracted, including 'Year', 'Month', 'Day', 'Hour', and 'Minute'. The 'Description' column is dropped as it is no longer needed.

5. Encoding categorical columns: The 'InvoiceNo' and 'StockCode' columns are encoded using a custom encoding function `encoder()`. Alphabetic characters are encoded as numeric values, while spaces are skipped. The encoded values are applied to the respective columns.

6. Label encoding: The 'Country' column is label encoded using the `LabelEncoder` class from sklearn. The encoded values are stored in a new column 'Country_encoded', and the original 'Country' column is dropped.

## Clustering Analysis

1. Data normalization: The dataset is normalized using the `MinMaxScaler` from sklearn to ensure all features have the same scale.

2. Determining the number of clusters: The optimal number of clusters is determined using the elbow method. The distortion score is calculated for different numbers of clusters using KMeans, and the elbow point is visualized using the `KElbowVisualizer` from yellowbrick.

3. K-means clustering: K-means clustering is performed with the chosen number of clusters. The cluster labels are assigned to the data points.

4. Dimensionality reduction and visualization: The data is further reduced to two dimensions using PCA (Principal Component Analysis). The reduced data is visualized using a scatter plot, where each cluster is represented by a distinct color.

## Conclusion

This project demonstrates the process of data preprocessing and clustering analysis on the Online Retail dataset. It provides insights into customer transactions and helps identify patterns and segments within the data.

For more details, refer to the code provided in the repository.

