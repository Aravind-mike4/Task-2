Customer Segmentation Analysis
Objective
This project aims to perform customer segmentation using clustering techniques. By grouping customers based on their purchasing behavior, businesses can gain insights to effectively target each segment with tailored strategies.

Project Steps
The analysis follows a structured approach, encompassing data generation, preprocessing, clustering, and visualization:

Dataset Generation:

For demonstration purposes, a synthetic dataset named customer_data.csv is generated in memory. This dataset includes Customer ID, Age, Annual Income, and Spending Score.

The synthetic data is designed to mimic potential customer segments to showcase the clustering effectively.

Data Loading and Inspection:

The generated dataset is loaded into a Pandas DataFrame.

Initial inspection is performed to understand the data's structure, including checking its shape, identifying any missing values or duplicates, examining data types, and reviewing summary statistics to understand the range and distribution of values.

Data Preprocessing:

Standardization: The Age, Annual Income, and Spending Score features are standardized using StandardScaler from sklearn.preprocessing. This crucial step ensures that all features are on a similar scale, preventing features with larger magnitudes from dominating the clustering algorithm.

Clustering:

Optimal Number of Clusters (Elbow Method): The Within-Cluster Sum of Squares (WCSS) is calculated for a range of cluster numbers (1 to 10). The results are plotted to identify the "elbow point," which suggests the optimal number of clusters (K). In this script, an optimal K=5 is assumed based on typical patterns for the generated data.

K-Means Clustering: The K-Means algorithm is applied to the standardized data using the determined optimal number of clusters. Each customer is then assigned a Cluster label, which is added as a new column to the original dataset.

Summary statistics per cluster are printed to understand the characteristics of each segment.

Visualization:

2D Scatter Plot (PCA): Principal Component Analysis (PCA) is used to reduce the dimensions of the standardized features to two principal components. A scatter plot visualizes the clustered customers in this 2D space, with each cluster represented by a different color.

Elbow Method Plot: The plot showing WCSS against the number of clusters is displayed to aid in identifying the optimal K.

Pair Plots: Pair plots are generated to visualize the relationships between Age, Annual Income, and Spending Score for each cluster, providing deeper insights into feature distributions within segments.

Centroid Visuals: The centroids of each cluster are inverse-transformed back to the original scale of the features. Bar charts are then used to visualize these centroids, offering clear interpretations of the average characteristics of customers within each segment.

Dataset Columns
The synthetic customer_data.csv dataset contains the following columns:

Customer ID: Unique identifier for each customer.

Age: Age of the customer.

Annual Income: Income of the customer (in a generic currency).

Spending Score: A score (1-100) indicating the customer's spending patterns and behavior.

Deliverables
Upon successful execution of the script, the following will be generated:

Clustered Dataset: The original DataFrame (df) will include a new column named Cluster, containing the assigned cluster label for each customer.

Visualizations:

An "Elbow Method for Optimal K" plot.

A "Customer Clusters (2D PCA)" scatter plot.

"Pair Plots of Features by Cluster".

"Cluster Centroids by Feature (Original Scale)" bar charts.

How to Run
Follow these steps to set up and run the customer segmentation script:

Prerequisites
Python 3.x installed.

pip (Python package installer) installed.

Installation
Open your terminal or command prompt and install the required Python libraries using pip:

pip install pandas numpy matplotlib seaborn scikit-learn

Execution
Save the provided Python script as, for example, customer_segmentation.py.

Navigate to the directory where you saved the file in your terminal or command prompt.

Run the script using the Python interpreter:

python customer_segmentation.py

The script will print progress messages to the console and display the various plots. Close each plot window to proceed to the next step of the script.

Key Libraries Used
pandas: For data manipulation and analysis.

numpy: For numerical operations.

matplotlib: For creating static, interactive, and animated visualizations.

seaborn: A high-level data visualization library based on matplotlib.

scikit-learn (sklearn): For machine learning algorithms, including StandardScaler, KMeans, and PCA.