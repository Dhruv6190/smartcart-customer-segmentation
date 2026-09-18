# SmartCart — Customer Segmentation

An unsupervised machine learning project that segments customers into distinct groups based on demographic, purchasing, engagement, and behavioral characteristics.

## Overview

SmartCart Customer Segmentation uses clustering techniques to identify groups of customers with similar characteristics and purchasing behavior.

The project applies data preprocessing, feature engineering, categorical encoding, feature scaling, dimensionality reduction using PCA, and K-Means clustering to discover meaningful customer segments.

## Dataset

The dataset contains **2,240 customer records and 22 columns**.

The dataset includes customer information such as:

* Year of Birth
* Education
* Marital Status
* Income
* Number of Children
* Customer Enrollment Date
* Recency
* Product Spending
* Deal Purchases
* Web Purchases
* Catalog Purchases
* Store Purchases
* Web Visits
* Complaints
* Campaign Response

## Project Workflow

### 1. Data Exploration

* Loaded the customer dataset
* Inspected its dimensions
* Checked missing values
* Examined customer attributes and purchasing behavior

### 2. Missing Value Handling

Missing income values were handled using median imputation.

### 3. Feature Engineering

Several features were created to better represent customer characteristics:

* **Age**
* **Customer Tenure**
* **Total Products**
* **Total Children**
* **Living With**

Education and marital-status categories were also consolidated into broader groups.

### 4. Categorical Encoding

Categorical variables such as:

* Education
* Living With

were converted into numerical representations using one-hot encoding.

### 5. Feature Scaling

`StandardScaler` was applied to standardize the numerical feature space before clustering.

### 6. Dimensionality Reduction

Principal Component Analysis (PCA) was applied to reduce the feature space to three principal components for visualization and clustering analysis.

A 3D PCA projection was created to visualize the transformed customer data.

### 7. K-Means Clustering

K-Means clustering was evaluated for different values of K.

The Elbow Method was used to examine the Within-Cluster Sum of Squares (WCSS).

The analysis identified:

**Optimal number of clusters: 5**

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Kneed
* Jupyter Notebook

## Repository Structure

```text
smartcart-customer-segmentation/
│
├── README.md
├── SmartCartSegmentationSystem.ipynb
├── smartcart_customers_data.xls
├── requirements.txt
└── .gitignore
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/<your-username>/smartcart-customer-segmentation.git
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook SmartCartSegmentationSystem.ipynb
```

Run the notebook cells sequentially to reproduce the preprocessing, dimensionality reduction, clustering analysis, and visualizations.

## Key Takeaway

This project demonstrates an end-to-end unsupervised learning workflow for customer segmentation, including data cleaning, feature engineering, categorical encoding, feature scaling, PCA-based dimensionality reduction, K-Means clustering, and cluster-number selection using the Elbow Method.

## Author

**Dhruv Saxena**
