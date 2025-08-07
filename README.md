# Project Title:
- Comparative Analysis of K-Means and K-Medoids Clustering on COVID-19 Global Dataset
# Objective:
- To perform unsupervised clustering using K-Means and K-Medoids algorithms on global COVID-19 data and analyze their performance in grouping countries/regions based on pandemic severity (Confirmed, Deaths, Recovered, Active cases).
# Why We Use This Project:
- To compare the effectiveness of centroid-based clustering (K-Means) vs medoid-based clustering (K-Medoids) on real-world COVID-19 data.
- To visualize country-level patterns of COVID-19 spread and identify groupings with similar outbreak behavior.
- To demonstrate unsupervised learning techniques in public health and data science.
- K-Medoids is more robust to outliers, while K-Means is computationally efficient—making their comparison insightful.
# Step-by-Step Approach:
### Data Import:
- Import COVID-19 dataset from Kaggle using kagglehub.
### Data Cleaning:
- Remove unnecessary columns (Province/State)
- Handle missing values (not explicitly needed here as main fields are complete)
# Exploratory Data Analysis (EDA):
- Total confirmed, recovered, and death cases grouped by Country and WHO Region
- Bar charts using Plotly to visualize top 10 countries/regions
### Feature Selection:
- Selected numerical features: Confirmed, Deaths, Recovered, Active
### Feature Engineering (Preprocessing):
- Normalize data using StandardScaler to prepare for clustering
# Model Training:
-K-Means Clustering: (using scikit-learn)
→ Clustered into 3 groups
-K-Medoids Clustering: (using pyclustering)
→ Clustered into 3 groups with predefined medoids [0,1,2]
# Model Testing (Evaluation):
- Used Silhouette Score to evaluate clustering quality:
- K-Means: 0.9767
- K-Medoids: 0.9542
# Visualization:
- Scatter plots of Confirmed vs Deaths colored by cluster labels (for both methods)
# Exploratory Data Analysis (Highlights):
- Top 10 Countries by Confirmed, Recovered, and Deaths
- WHO Regions Analysis for Confirmed, Recovered, and Deaths
- Clear disparities observed across regions (e.g., Americas and Europe had high case counts)
# Feature Engineering:
- Selected key pandemic metrics: Confirmed, Deaths, Recovered, Active
- Scaled features to normalize the effect of large value ranges across countries
# Model Training:
- K-Means:
- Algorithm: Lloyd’s Algorithm
### Clusters: 3
- Library: scikit-learn
- K-Medoids:
- Algorithm: Partitioning Around Medoids (PAM)
### Clusters: 3
- Library: pyclustering
# Model Testing (Evaluation):
### Algorithm	Silhouette Score
- K-Means	0.9767
- K-Medoids	0.9542
### Inference: Both models performed very well, but K-Means slightly outperformed K-Medoids in terms of cohesion and separation of clusters.
# Output:
![WhatsApp Image 2025-08-07 at 7 35 54 PM](https://github.com/user-attachments/assets/59523572-c31c-4b8c-80ba-96ee992de251)
<img width="790" height="299" alt="Screenshot 2025-08-07 110714" src="https://github.com/user-attachments/assets/026161c5-ec75-486f-8558-094c7e216a14" />

