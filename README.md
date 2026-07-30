# Customer Segmentation using Machine Learning

A machine learning project that segments retail customers using **RFM Analysis** and compares multiple clustering algorithms to identify meaningful customer groups and generate actionable business insights.

---

# Project Overview

Customer segmentation is a data-driven technique used to group customers based on similar purchasing behaviour. This project analyzes the **Online Retail Dataset**, performs extensive data preprocessing, creates customer-level **Recency, Frequency, and Monetary (RFM)** features, and applies multiple unsupervised machine learning algorithms to identify distinct customer segments.

The project compares the performance of **K-Means**, **DBSCAN**, and **Gaussian Mixture Models (GMM)** using clustering evaluation metrics to determine the most effective segmentation model.

---

# Objectives

- Clean and preprocess transactional retail data.
- Engineer customer-level RFM features.
- Standardize numerical features before clustering.
- Determine the optimal number of clusters.
- Implement multiple clustering algorithms.
- Compare model performance using evaluation metrics.
- Visualize customer segments.
- Generate meaningful business insights.

---

# Dataset

| Attribute | Description |
|------------|-------------|
| Dataset | Online Retail Dataset |
| Records | 541,909 Transactions |
| Customers | Approximately 4,300 |
| Duration | 2010–2011 |
| Features | Invoice, Product, Quantity, Unit Price, Customer ID, Country, Invoice Date |

The dataset contains transactional records of a UK-based online retail company.

---

# Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- OpenPyXL

---

# Project Workflow

## 1. Data Collection

The Online Retail dataset was loaded into Google Colab using Pandas.

---

## 2. Data Cleaning

The following preprocessing steps were performed:

- Removed missing Customer IDs
- Removed duplicate records
- Removed cancelled transactions
- Removed invalid quantities
- Converted InvoiceDate into datetime format

---

## 3. Feature Engineering

Customer behaviour was summarized using **RFM Analysis**.

### Recency

Number of days since the customer's last purchase.

### Frequency

Number of purchases made by the customer.

### Monetary

Total amount spent by the customer.

---

## 4. Data Scaling

The RFM features were standardized using **StandardScaler** before applying clustering algorithms.

---

## 5. Determining Optimal Clusters

The **Elbow Method** was used to determine the optimal number of clusters for K-Means.

---

## 6. Model Training

The following clustering algorithms were implemented:

- K-Means Clustering
- DBSCAN
- Gaussian Mixture Model (GMM)

---

## 7. Model Evaluation

Models were evaluated using:

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index

---

## 8. Cluster Interpretation

The resulting customer groups were analyzed using their average RFM values to identify purchasing patterns and customer behaviour.

---

# Machine Learning Models

## K-Means Clustering

K-Means partitions customers into K distinct clusters by minimizing the distance between customers and their cluster centroids.

### Advantages

- Fast
- Easy to interpret
- Performs well on standardized numerical data

---

## DBSCAN

DBSCAN identifies clusters based on density and is capable of detecting outliers.

### Advantages

- Does not require specifying the number of clusters
- Detects noise effectively

---

## Gaussian Mixture Model (GMM)

GMM assumes that the data is generated from multiple Gaussian distributions and assigns probabilistic cluster memberships.

### Advantages

- Flexible cluster shapes
- Soft clustering approach

---

# Model Evaluation

The clustering models were compared using standard evaluation metrics.

| Metric | Purpose |
|----------|----------|
| Silhouette Score | Higher is better |
| Davies-Bouldin Index | Lower is better |
| Calinski-Harabasz Index | Higher is better |

The best-performing model was selected based on these evaluation metrics.

---

# Visualizations

## Elbow Curve

![Elbow Curve](Images/elbow_curve.png)

---

## K-Means Customer Segments

![KMeans Clusters](Images/kmeans_clusters.png)

---

## Customer Distribution

![Cluster Distribution](Images/cluster_distribution.png)

---

## Average RFM Values

![RFM Summary](Images/rfm_cluster_summary.png)

---

## Model Comparison

![Model Comparison](Images/model_comparison.png)

---

# Business Insights

The customer segmentation analysis revealed several meaningful customer groups, including:

- High-value loyal customers
- Frequent purchasers
- Low-value customers
- Customers at risk of churn

These insights can help businesses:

- Improve customer retention
- Design personalized marketing campaigns
- Allocate marketing resources effectively
- Increase customer lifetime value

---

# Project Structure

```
customer-segmentation-ml/
│
├── data/
│   └── Online Retail.xlsx
│
├── Images/
│   ├── elbow_curve.png
│   ├── kmeans_clusters.png
│   ├── cluster_distribution.png
│   ├── rfm_cluster_summary.png
│   └── model_comparison.png
│
├── Notebook/
│   └── CustomerSegmentation.ipynb
│
├── README.md
├── requirements.txt
├── LICENSE
└── Customer_Segmentation_Report.docx
```

---

# Installation

Clone the repository.

```bash
git clone https://github.com/yourusername/customer-segmentation-ml.git
```

Install the required packages.

```bash
pip install -r requirements.txt
```

Open the notebook in **Google Colab** or **Jupyter Notebook**.

Place the dataset inside the **data/** directory and run all notebook cells.

---

# Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
openpyxl
jupyter
```

---

# Future Improvements

- Hyperparameter tuning
- Additional clustering algorithms
- Interactive dashboards
- Deployment as a web application
- Automated customer segmentation pipeline

---

# Conclusion

This project demonstrates an end-to-end machine learning workflow for customer segmentation, from data preprocessing and feature engineering to clustering, evaluation, visualization, and business interpretation. The resulting customer segments can support data-driven marketing strategies and improve business decision-making.

---

# Author

**Name:** Atlas Tencia  
**University:** Mahindra University  
**Program:** B.Tech ECM  
**Year:** 2026

---

## License

This project is licensed under the MIT License.
