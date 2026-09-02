# Customer Segmentation using K-Means Clustering

## Project Overview

This project uses **K-Means Clustering** to segment customers into different groups based on their **Yearly Income** and **Spending Score**.

The project demonstrates an unsupervised machine learning approach for identifying customer segments with similar income and spending behavior.

## Objective

The objective of this project is to identify meaningful customer segments based on:

* Yearly Income
* Customer Spending Score

These segments can help businesses understand different customer groups and support customer-focused marketing strategies.

## Dataset

The dataset contains 200 customer records with the following features:

* **Cust_Number** – Unique customer identifier
* **Yearly_Income** – Customer's yearly income
* **Age** – Customer age
* **Cust_Spend_Score** – Customer spending score
* **Sex** – Customer gender

## Data Preparation

The following preprocessing steps were performed:

1. Checked the dataset shape and data types.
2. Converted the `Sex` field from integer to object data type.
3. Checked for missing values.
4. Removed `Cust_Number` because it is an identifier and is not useful for clustering.
5. Performed outlier analysis using boxplots.
6. Selected `Yearly_Income` and `Cust_Spend_Score` for clustering.
7. Standardized the selected features using `StandardScaler`.

## Machine Learning Approach

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** that groups similar observations into clusters.

The optimal number of clusters was evaluated using:

* Elbow Method
* Silhouette Score

### Elbow Method

The WCSS (Within-Cluster Sum of Squares) was calculated for different values of K from 1 to 20.

Based on the elbow analysis, **K = 5** was selected for the final clustering model.

### Silhouette Score

Silhouette scores were calculated for K values from 2 to 6:

| Number of Clusters | Silhouette Score |
| -----------------: | ---------------: |
|                  2 |           0.3401 |
|                  3 |           0.4042 |
|                  4 |           0.3795 |
|                  5 |           0.3533 |
|                  6 |           0.3869 |

Although K = 3 produced the highest silhouette score, K = 5 was selected based on the elbow analysis and the desired customer segmentation structure.

## Final Clusters

The final K-Means model was created with **5 clusters**.

Cluster sizes:

| Cluster | Customers |
| ------: | --------: |
|       0 |        38 |
|       1 |        36 |
|       2 |        54 |
|       3 |        37 |
|       4 |        35 |

The clusters were visualized using Yearly Income and Customer Spending Score to understand the differences between customer groups.

## Cluster Analysis

The clusters represent customers with different combinations of income and spending behavior.

For example:

* Customers in one segment have relatively high spending scores with lower or moderate income.
* Another segment contains customers with high yearly income and high spending scores.
* Other segments represent customers with lower spending behavior and different income levels.

The cluster characteristics were analyzed using descriptive statistics.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Machine Learning Algorithm

**K-Means Clustering**

The project demonstrates:

* Data preprocessing
* Data type conversion
* Missing value checking
* Outlier analysis
* Feature selection
* Feature scaling
* Elbow Method
* Silhouette Score
* K-Means clustering
* Cluster visualization
* Cluster analysis

## Project Structure

```text
customer-segmentation-kmeans/
│
├── Customer.csv
├── customer_segmentation_kmeans.ipynb
└── README.md
```

## Key Learning Outcomes

* Understanding unsupervised machine learning
* Understanding K-Means clustering
* Selecting features for clustering
* Understanding why scaling is important for K-Means
* Finding the number of clusters using the Elbow Method
* Evaluating clusters using Silhouette Score
* Visualizing customer segments
* Interpreting cluster characteristics
