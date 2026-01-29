# Mall Customer Segmentation using K-Means Clustering

## Project Overview
This project performs **unsupervised learning** on the Mall Customers dataset(taken from kaggle) to segment customers based on their **Annual Income, Spending Score, and Age**.  

---

## Dataset
**Columns:**
- `CustomerID` : Unique ID for each customer  
- `Genre` : Male/Female  
- `Age` : Age of the customer  
- `Annual Income ` : Customer's annual income in $k  
- `Spending Score` : Mall spending behavior score  


## Project Workflow

1. **Exploratory Data Analysis (EDA)**
   - Checked dataset shape, missing values, and basic statistics  
   - Visualized distributions of `Age`, `Annual Income`, and `Spending Score`  
   - Explored relationships via scatter plots and pairplots to identify natural groupings  

2. **Preprocessing**
   - Selected key features for clustering (`Annual Income` and `Spending Score`)  
   - Scaled features using `StandardScaler` for fair distance calculations  

3. **Finding Optimal Clusters (K)**
   - Applied **Elbow Method** (Inertia/SSE)  
   - Evaluated **Silhouette Scores**  
   - Determined `K = 5` as the optimal number of clusters  

4. **K-Means Clustering**
   - Applied K-Means with `K = 5`  
   - Assigned cluster labels to each customer  
   - Visualized clusters in a 2D scatter plot (Income vs Spending) with centroids  

5. **Cluster Interpretation**
   - Gave **business labels** based on behavior:
     - `VIP` → High income, high spender  
     - `Impulsive` → Low income, high spender  
     - `Savers` → High income, low spender  
     - `Budget` → Low income, low spender  
     - `Average` → Medium income & spending  

6. **Visualization**
   - Bar charts for each cluster showing **average income, spending score, and age**  

---

## Key Insights

- **VIPs** (High income, high spending) are mostly young professionals (~32 years old)  
- **Impulsive shoppers** (Low income, high spending) are the youngest (~25 years old)  
- **Savers** (High income, low spending) and **Budget shoppers** (Low income, low spending) are older (~41–45 years old)  
- **Average customers** fall in the middle for both income and spending (~55k income, ~50 score)  
- Income does not always predict spending behavior → segmentation by clustering reveals **hidden patterns**

---
