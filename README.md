# **K-Means Clustering on Sales Data**

Welcome to the **Sales Data Clustering Analysis** repository!  
This project applies **K-Means Clustering** to uncover patterns and groupings in a real-world sales dataset. It leverages dimensionality reduction techniques like **PCA** to visualize clusters in a comprehensible way.

## **Overview**

This project demonstrates the end-to-end workflow for clustering analysis using **K-Means**:
- Data preprocessing and cleaning.
- Optimal cluster determination using the **Elbow Method**.
- Application of **PCA** for dimensionality reduction.
- Visualizing clusters and their centroids in 2D space.

---

## **Key Features**

- **Clustering with K-Means**: Groups data into distinct clusters for insightful segmentation.
- **Elbow Method**: Determines the ideal number of clusters by analyzing within-cluster variance.
- **Dimensionality Reduction**: Reduces dataset to two principal components using PCA for visualization.
- **Visual Insights**: Generates rich visualizations for intuitive understanding.

---

## **Tools and Libraries**

### **Languages**:
- Python

### **Libraries**:
- `pandas`: Data manipulation and cleaning.
- `numpy`: Numerical computation.
- `matplotlib` & `seaborn`: Data visualization.
- `scikit-learn`: Machine learning tools for clustering and PCA.

---

## **Dataset**

The analysis uses the `sales_data_sample.csv` file, which includes transactional sales data.  
**Columns dropped during preprocessing**:
- Irrelevant or redundant fields: `ADDRESSLINE1`, `STATUS`, `PHONE`, etc.
- Categorical columns replaced with dummy variables: `PRODUCTLINE`, `DEALSIZE`.

---

## **Methodology**

### 1. **Data Preprocessing**
- Dropped unnecessary columns to focus on clustering-relevant data.
- Converted categorical fields to numeric using **One-Hot Encoding**.
- Normalized features for uniform scaling.

### 2. **Finding theFinding the optimal number of clusters (k) by testing values from 1 to 10**
  - Plotted the **distortion scores** (inertia values) against the number of clusters.  
  - Chose the value of `k` where the distortion curve begins to "elbow", indicating an optimal balance between variance explained and complexity.

### 3. **K-Means Clustering**
- Applied K-Means with `k=3` (optimal clusters).
- Assigned each data point to one of the three clusters based on proximity to centroids.

### 4. **Dimensionality Reduction**
- Used **Principal Component Analysis (PCA)** to reduce the dataset to two principal components for visualization.
- Retained maximum variance in the data while enabling 2D plotting.

### 5. **Visualization**
- **Elbow Plot**: Displayed the optimal number of clusters.
- **Cluster Scatter Plot**: Visualized the clustering results in 2D PCA space.
- **Centroid Plot**: Highlighted the centroids for each cluster in the PCA-transformed space.

---

## **Code Overview**

### **Key Steps in the Code**:
1. **Preprocessing**:
   - Dropped redundant columns.
   - Converted categorical data to dummy variables.
   - Transformed `PRODUCTCODE` to numeric codes.
   - Dropped `ORDERDATE` (irrelevant for clustering).

2. **K-Means Implementation**:
   - Used `KMeans` from `sklearn` to fit the model and predict cluster labels.
   - Counted the number of samples in each cluster.

3. **Dimensionality Reduction**:
   - Used `PCA` from `sklearn` for reducing dimensions to 2 components.
   - Transformed both data points and cluster centroids to PCA space.

4. **Visualization**:
   - Plotted clusters, centroids, and the results of PCA using `matplotlib`.

---

## **Results**

### **Optimal Number of Clusters**
The **Elbow Method** revealed that 3 clusters (k=3) provide the best balance between cluster variance and complexity.

### **Cluster Distribution**
- The dataset was grouped into three distinct clusters, each representing a segment of the sales data.

### **PCA Visualization**
- **Clusters**: The clusters were visually separated in PCA-transformed space.
- **Centroids**: Centroids were distinctly plotted, representing the centers of each cluster.

---

## **Visuals**

### 1. **Elbow Plot**  
Illustrates the optimal number of clusters based on distortion scores.  
*(Insert image: `elbow_plot.png`)*  

### 2. **Cluster Scatter Plot**  
Visualizes the PCA-reduced data points grouped into clusters.  
*(Insert image: `cluster_scatter.png`)*  

### 3. **Centroid Visualization**  
Highlights cluster centroids in the PCA space.  
*(Insert image: `centroid_plot.png`)*

---

## **Usage Instructions**

### **Clone Repository**
```bash
git clone https://github.com/yourusername/sales-data-clustering.git

