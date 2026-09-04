# 🛒 SmartCart Customer Segmentation using Unsupervised ML

## 📌 Project Overview
This project applies **Unsupervised Machine Learning (Clustering)** to automatically segment a retail store's customer database into distinct behavioral personas. By analyzing demographic data and purchasing histories, this pipeline allows the business to transition from generic marketing to hyper-targeted, high-conversion campaigns.

---

## 🛠️ Data Pipeline & Workflow Sequence

This project strictly follows the standard end-to-end data science lifecycle:

1. Data Inspection: Evaluated structural metadata (`df.shape`, `df.info()`) to map out the data canvas.
2. Data Cleaning: Imputed missing income records using robust median-based replacement and filtered out age/income statistical outliers.
3. Feature Engineering: Constructed high-value combined metrics (`Total_Spending` and `Total_Children`) and condensed overlapping categorical values.
4. Exploratory Data Analysis (EDA): Leveraged data visualizations to evaluate feature distributions and mapped an internal correlation heatmap.
5. Data Preprocessing: Deployed `OneHotEncoder` for fair categorical encoding and utilized `StandardScaler` to equalize feature mathematical weights.
6. Dimensionality Reduction: Squashed the complex 18-dimensional feature space down to 3 core coordinates using Principal Component Analysis (PCA).
7. Optimal Cluster Determination: Computed internal cluster cluster tightness (WCSS) loops and utilized `KneeLocator` to pinpoint the mathematical "elbow bend" at K = 4.
8. Model Execution: Deployed Agglomerative Hierarchical Clustering using Ward linkage to map out the final 4-family consumer segments.


## 📊 Discovered Customer Personas (Results)

* Cluster 0: Lower-income families with high children counts. Best targeted with bulk-buy discounts and family essential coupons.
* Cluster 1: Highly affluent power couples. Premium target audience for luxury product lines, gourmet goods, and high-end tech.
* Cluster 2: Budget solo shoppers. Ideal candidates for daily-necessity discounts and low-ticket convenience items.
* Cluster 3: High-income solo spenders. Best targeted with convenience-based premium services, single-serve gourmet lines, and express perks.



## 💻 Tech Stack & Libraries Used
* Language: Python
* Data Manipulation: Pandas, NumPy
* Data Visualization: Seaborn, Matplotlib
* Machine Learning: Scikit-Learn (KMeans, AgglomerativeClustering, PCA, StandardScaler, OneHotEncoder)
* Optimization: Kneed (KneeLocator)

