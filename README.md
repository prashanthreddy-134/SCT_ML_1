# SCT_ML_2 – Customer Segmentation (K-Means Clustering)

**Task:** Create a K-Means clustering algorithm to group customers of a retail store based on their purchase history.
**Dataset:** Mall Customer Dataset (link in the internship brief).

## Setup
```bash
pip install -r requirements.txt
```
Place the file at `data/Mall_Customers.csv`.

## Run
```bash
python kmeans_customers.py                  # chooses k with the best silhouette score
python kmeans_customers.py --k 5            # or set k yourself
```

## Method
1. Use Annual Income and Spending Score as the customer features (the spending score is the closest proxy for purchase behaviour in this dataset).
2. Standardise the features with `StandardScaler`.
3. Choose the number of clusters with the elbow method and silhouette score (k = 2 to 10).
4. Fit `KMeans` and summarise each segment.

## Outputs (`outputs/`)
- `kmeans_analysis.png`: elbow curve, silhouette curve and labelled cluster plot
- `customer_clusters.csv`: every customer with its cluster label
- `cluster_summary.csv`: average income and spending score per cluster

## Results
Chosen k: ____  Silhouette score: ____
