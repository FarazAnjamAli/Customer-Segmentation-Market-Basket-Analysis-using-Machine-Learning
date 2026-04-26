# Customer-Segmentation-Market-Basket-Analysis-using-Machine-Learning
End-to-end data mining project including customer segmentation, clustering, association rule mining, and classification on retail dataset.
# Customer Segmentation and Market Basket Analysis using Machine Learning

## Overview
This project presents a comprehensive data mining pipeline applied to an online retail dataset from the UCI Machine Learning Repository. The objective is to analyze customer behavior, segment customers based on purchasing patterns, discover product associations, and build predictive models for customer value classification.

The project covers data preprocessing, feature engineering, clustering, association rule mining, and classification.

---

## Dataset
- Source: UCI Machine Learning Repository (Online Retail Dataset)
- Total Records: 541,909
- Features:
  - InvoiceNo
  - StockCode
  - Description
  - Quantity
  - InvoiceDate
  - UnitPrice
  - CustomerID
  - Country

---

## Data Preprocessing
- Removed records with missing CustomerID values (~25%)
- Removed canceled transactions
- Removed negative quantity and price values
- Final cleaned dataset size: 397,884 records

---

## Feature Engineering
RFM (Recency, Frequency, Monetary) analysis was performed to represent customer behavior:

- Recency: Days since last purchase
- Frequency: Number of transactions
- Monetary: Total spending

---

## Methodology

### Clustering

#### K-Means Clustering
- Identified 3 customer segments:
  - Low-value customers
  - Medium-value customers
  - High-value customers

#### DBSCAN Clustering
- Parameter tuning performed for eps and min_samples
- Best parameters:
  - eps = 0.3
  - min_samples = 5
- Silhouette Score: 0.674
- Noise points identified: approximately 2.5%

---

### Association Rule Mining

#### Apriori Algorithm
- Frequent itemsets generated: 251
- Rules extracted: 20 (confidence ≥ 0.6, lift ≥ 1.2)

#### FP-Growth Algorithm
- Similar results to Apriori
- Slightly faster execution time

---

### Classification

#### Gaussian Naive Bayes
- Accuracy: 96.16%
- Precision: 97.26%
- Recall: 87.12%
- F1-Score: 91.91%

#### Bernoulli Naive Bayes
- Accuracy: 79.26%
- Lower performance due to binary assumptions

---

### Support Vector Machines

#### Linear SVM
- Accuracy: 97.24%

#### RBF Kernel SVM (Best Model)
- Accuracy: 99.54%
- Precision: 99.69%
- Recall: 98.46%
- F1-Score: 99.07%

---

## Key Insights
- A small group of high-value customers contributes significantly to total revenue
- Strong product associations can be leveraged for recommendation systems
- Density-based clustering effectively identifies outliers
- RBF SVM provides the best classification performance among all models

---

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- mlxtend

---

## Project Structure
