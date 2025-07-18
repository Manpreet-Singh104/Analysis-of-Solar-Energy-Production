# Analysis-of-Solar-Energy-Production

Certainly! Here's a concise summary of **K-Means Clustering with Python and Scikit-Learn** using the ** India and World dataset**:

---

### 🧠 **K-Means Clustering with Python and Scikit-Learn** – Summary

**Objective:**
To identify **intrinsic groups (clusters)** in unlabelled data using the **K-Means algorithm**, applied to the **India and World** dataset.

---

### 📌 **Key Concepts:**

* **K-Means Clustering:**
  An unsupervised learning algorithm that:

  1. Chooses `K` cluster centers (centroids),
  2. Assigns each data point to the nearest centroid,
  3. Updates centroids based on mean of assigned points,
  4. Repeats until convergence.

* **Use Case in Project:**
  To group posts based on **status\_type** behavior — such as different engagement types (e.g., live video, photo, status update).

* **Why K-Means?**
  Efficient for large datasets, easy to interpret, and useful when you don’t have labels.

---

### 🛠️ **Implementation Steps in Python:**

1. **Import Libraries:**

   ```python
   import pandas as pd
   from sklearn.cluster import KMeans
   import matplotlib.pyplot as plt
   ```

2. **Load Dataset:**

   ```python
   df = pd.read_csv("facebook_live_sellers.csv")
   ```

3. **Preprocessing:**

   * Handle missing values
   * Normalize features
   * Select relevant columns

4. **Find Optimal K (Elbow Method):**

   ```python
   distortions = []
   for i in range(1, 11):
       km = KMeans(n_clusters=i)
       km.fit(data)
       distortions.append(km.inertia_)
   ```

5. **Fit K-Means:**

   ```python
   kmeans = KMeans(n_clusters=3)
   kmeans.fit(data)
   df['Cluster'] = kmeans.labels_
   ```

6. **Visualize Clusters (optional 2D):**

   ```python
   plt.scatter(data['feature1'], data['feature2'], c=df['Cluster'])
   ```

---

### 📊 **Insights Gained:**

* Identified **group behavior patterns** based on content performance.
* Useful for **targeted marketing**, **content strategy**, or **anomaly detection**.

---



