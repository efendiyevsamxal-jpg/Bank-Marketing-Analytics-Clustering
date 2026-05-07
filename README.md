Bank Customer Segmentation: Advanced Analysis (K-Means, PCA, HC)

1. Project Overview
This project focuses on segmenting bank customers based on behavioral and demographic data.
It utilizes unsupervised learning techniques, including data preprocessing, dimensionality reduction (PCA),
and a comparative study of K-Means and Hierarchical Clustering algorithms to derive actionable customer insights.

2. Technical Stack
The following libraries are essential for this analysis:

Data Handling: NumPy, Pandas

Visualization: Matplotlib, Seaborn, Scipy.cluster.hierarchy

Machine Learning: Scikit-learn (StandardScaler, PCA, KMeans, AgglomerativeClustering, Silhouette Score)

Optimization: Kneed (KneeLocator for elbow detection)

3. Data Pre-processing Pipeline
Descriptive Statistics: Comprehensive data audit using .describe().

Data Cleaning: Dropping redundant features and handling null values with .isnull().sum().

Label Encoding: Converting categorical attributes into numeric representations.

Outlier Treatment: Detecting and refining extreme values to prevent model bias.

Feature Scaling: Implementing StandardScaler to normalize features for distance-based clustering.

4. K-Means Clustering & Optimization
Elbow Method: Evaluation of WCSS (Within-Cluster Sum of Squares) from k=1 to k=7.
Silhouette Analysis: Measuring the separation distance between resulting clusters.
KneeLocator: Automated detection of the optimal k (elbow point).
Cluster Profiling: Segmenting data into 3 groups and calculating the mean, data count, and proportion for each cluster to understand market share.

5. PCA (Principal Component Analysis)
Dimensionality Reduction: Analyzed cumulative explained variance to reduce 12+ features into 7 principal components.

PCA-Enhanced Clustering: Re-applied K-Means on PCA-transformed data to identify 4 refined segments.

2D Projection: Visualized clusters using the first two principal components (Variable_1 vs Variable_2) for better spatial interpretation.

6. Hierarchical Clustering (HC)
Performed on both standardized raw data and PCA components:
Dendrograms: Visualizing the hierarchical relationship using the Ward linkage method. Thresholding at y=110 to determine optimal splits.
Agglomerative Clustering: Implemented the model to create segment_HC and segment_HC_PCA.
Final Profiling & Comparison: Aggregating segment means and proportions. Final
visualizations use rainbow-coded scatter plots to distinguish between customer types based on Income, CCAvg, and PCA variables.

7. Key Insights & Conclusion
This comprehensive analysis led to the following strategic conclusions:

Optimal Segmentation: Through a combination of K-Means and PCA, the customer base was successfully segmented into distinct personas. The PCA-enhanced approach provided much clearer cluster boundaries compared to the raw data alone.

Behavioral Patterns:

Segment 1: High-income individuals with moderate credit usage – Ideal candidates for premium wealth management services.

Segment 2: Mid-to-low income customers with high credit card activity – High potential for loyalty programs and personalized credit offers.

Segment 3: Conservative users with low credit engagement – Targeted for educational marketing about banking products.

Methodological Efficiency: The Hierarchical Clustering (Dendrogram) confirmed the cluster counts identified by the Elbow Method, ensuring the mathematical reliability of the segments.

Business Impact: These data-driven segments empower the bank to optimize marketing spend by targeting the right customers with the right products, ultimately increasing conversion rates and customer retention.
