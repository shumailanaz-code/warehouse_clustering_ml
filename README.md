# 🏭 Warehouse Order Status Analysis using Clustering

## 📖 Project Overview

A polypropylene bags warehouse has been facing increasing complaints related to **late deliveries** and **incomplete shipments**. 
To address this, the company wants to analyze past transaction data to identify and categorize order statuses. 
Since the dataset lacks predefined labels, we apply **unsupervised machine learning techniques** — specifically **KMeans Clustering** and **Agglomerative Hierarchical Clustering** — 
to uncover hidden patterns and group similar orders.

This model will help the company in identifying:
- Orders likely to be **disputed or incomplete**
- Historical trends to improve **logistics and customer service**
- Future **planning and fulfillment strategies**

---

## 📦 Dataset Description

- **File Name**: `Warehouse_data.csv`
- **Source**: Kaggle
- **Total Features**:
  
| Feature Name           | Type        | Description                                      |
|------------------------|-------------|--------------------------------------------------|
| `Purchase_Order_No`    | Numerical   | Unique identifier for each order                 |
| `Product_Name`         | Categorical | Name      of product ordered                     |
| `Customer_ID`          | Categorical | Unique customer identifier                       |
| `Gender`               | Categorical | Gender of the customer                           |
| `Age`                  | Numerical   | Age of the customer                              |
| `City`                 | Categorical | Location of the customer                         |
| `Quantity_Ordered`     | Numerical   | Number of items ordered                          |
| `Quantity_Delivered`   | Numerical   | Number of items actually delivered               |
| `Quantity_Returned`    | Numerical   | Items returned by the customer                   |
| `Quantity_Redelivered` | Numerical   | Items redelivered after returns                  |
| `Order_Status`         | *Output*    | Status label to be predicted via clustering      |

> Note: As the dataset is unlabeled, `Order_Status` will be inferred through clustering rather than directly provided.

---

## 🧪 Approach

### 🔹 Step-by-Step Procedure:
1. Data cleaning and preprocessing (handling missing values, standardization)
2. Feature selection:
   - `Quantity_Ordered`
   - `Quantity_Delivered`
   - `Quantity_Returned`
   - `Quantity_Redelivered`
3. Applied **KMeans Clustering**
   - Determined optimal clusters using Elbow Method
4. Applied **Agglomerative Hierarchical Clustering**
   - Visualized using dendrogram
5. Compared clustering results
6. Interpreted cluster groups as potential `Order_Status` labels:
   - e.g., Complete, Partially Delivered, Returned, Redelivered

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**, **NumPy** — Data manipulation
- **Scikit-learn** — Clustering algorithms
- **Seaborn**, **Matplotlib**, **Scipy** — Data visualization
- **Jupyter Notebook**

---

## 🚀 How to Run

1. Download or clone the repository.
2. Place the dataset `Warehouse_data.csv` in the working directory.
3. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn scipy
4. Open the Jupyter Notebook file (KMeans_clustering_ml.ipynb & agglomerative_hierarchical_clustering_ml.ipynb)
5. Run all cells to view clustering results and visualizations.

---
