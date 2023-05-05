# E-commerce Customer Segmentation using RFM Model and Clustering Algorithms

In the fiercely competitive retail industry, understanding customers and providing them with personalized product offerings and marketing strategies are crucial for success. To gain insights into customer behavior and preferences, we have used the Online Retail II dataset to analyze transactions made by customers of a UK-based online retail firm.

Our goal is to use the Recency, Frequency and Monetary model (RFM) to segment customers based on their purchasing behavior. We have preprocessed the data and handled any data issues related to the features. We have utilized K-Means, Agglomerative, and DBSCAN clustering algorithms to compute the RFM scores and divide customers into different groups.

To determine the optimal number of clusters, we have used the Elbow method along with the Silhouette score. Customers are assigned to one of the clusters based on their RFM scores, and we have visualized the clustered data using scatter plots and box plots to gain insights into customer behavior.

Since our dataset does not have any ground truth values, we have used intrinsic metrics such as Silhouette score, Calinski Harabasz score, and Davies Bouldin score to compare the KMeans, Agglomerative, and DBSCAN clustering models to determine the best clustering models for customer segmentation.

## Dataset

We have used the Online Retail II dataset for this project. The dataset contains transaction details for a UK-based online retail company from 01/12/2009 to 09/12/2011. The dataset has the following features:

- InvoiceNo: Unique identifier for each transaction
- StockCode: Unique identifier for each product
- Description: Product name
- Quantity: Quantity of the product purchased
- InvoiceDate: Date and time of the transaction
- UnitPrice: Unit price of the product
- CustomerID: Unique identifier for each customer
- Country: Country where the transaction was made

## Preprocessing

We have performed the following preprocessing steps on the dataset:

- We have removed any duplicate entries from the dataset.
- We have removed any entries with missing values.
- We have converted the InvoiceDate column to a datetime format.
- We have created a new column called TotalPrice, which is the product of Quantity and UnitPrice.

## RFM Model

The RFM model is a popular customer segmentation technique that uses the following three metrics:

- Recency: The number of days since the customer's last transaction.
- Frequency: The total number of transactions made by the customer.
- Monetary: The total amount of money spent by the customer.

We have computed the RFM scores for each customer using the following steps:

- We have determined the date of the most recent transaction in the dataset and subtracted the InvoiceDate of each customer's last transaction from it to calculate the Recency score.
- We have counted the number of transactions made by each customer to calculate the Frequency score.
- We have calculated the total amount spent by each customer to calculate the Monetary score.

We have then divided the customers into different groups based on their RFM scores using clustering algorithms.

## Clustering Algorithms

We have used the following clustering algorithms to group customers based on their RFM scores:

- K-Means: A popular clustering algorithm that groups data points into K clusters based on their similarity.
- Agglomerative: A hierarchical clustering algorithm that merges similar data points into clusters.
- DBSCAN: A density-based clustering algorithm that groups data points based on their density.

## Evaluation

Since our dataset does not have any ground truth values, we have used intrinsic metrics such as Silhouette score, Calinski Harabasz score, and Davies Bouldin score to compare the KMeans, Agglomerative, and DBSCAN clustering models and determine the best clustering models for customer segmentation.

##
