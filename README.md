# SCT_ML_1: Customer Segmentation (K-Means Clustering)

Task 1 of the SkillCraft Technology Machine Learning internship.

**Goal:** group mall customers into segments that a business could target differently.

**Dataset:** Mall Customer Dataset (`Mall_Customers.csv`, 200 customers). The features used are Annual Income (k$) and Spending Score (1-100). The dataset has no purchase history, so the spending score is used as the closest proxy for buying behaviour.

## Method
1. Standardise income and spending score with `StandardScaler`.
2. Test k = 1 to 10 with the elbow method (inertia) and k = 2 to 10 with the silhouette score.
3. Choose k with the highest silhouette score, which gives **k = 5**.
4. Fit K-Means and summarise each cluster.

## Results
| Cluster | Avg income (k$) | Avg spending score | Customers | Interpretation |
|---|---|---|---|---|
| 0 | 55.30 | 49.52 | 81 | Middle income, middle spending |
| 1 | 86.54 | 82.13 | 39 | High income, high spending |
| 2 | 25.73 | 79.36 | 22 | Low income, high spending |
| 3 | 88.20 | 17.11 | 35 | High income, low spending |
| 4 | 26.30 | 20.91 | 23 | Low income, low spending |

Silhouette score at k = 5: [value]

## How to run
1. Open `SCT_ML_1.ipynb` in Google Colab.
2. Upload `Mall_Customers.csv` to the Files panel.
3. Run all cells (Runtime → Run all).

## Files
- `SCT_ML_1.ipynb`: Colab notebook with the full run and outputs
- `kmeans_customers.py`: the same code as a script
- `outputs/`: elbow and silhouette plots, cluster labels and summary
