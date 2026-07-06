# Stores Data Mining Project 🏪📊

A data mining analysis of a retail stores dataset, covering Regression, Clustering, Association Rules, and Classification, aimed at understanding the factors that drive sales, profit, and customer behavior across different store branches.

## 📁 Project Contents

The project is a Jupyter Notebook (`last_mining.ipynb`) organized into the following sections:

1. **Data Preprocessing**
   - Reading the store data from an Excel file (`StoresData.xlsx`)
   - Renaming columns and cleaning text values (e.g., removing `Del:` and `Sun:` prefixes)
   - Checking for missing values and duplicates
   - Handling outliers using the IQR method

2. **Data Visualization (EDA)**
   - Histograms and KDE plots for the distribution of numeric columns
   - Correlation heatmap
   - Scatter/Box/Violin plots to explore relationships between sales and wages, advertising, car spaces, store age, and manager gender
   - Comparison of customer basket value between 2013 and 2014

3. **Sales Prediction (Multiple Linear Regression)**
   - Predicting sales (`Sales_$m`) based on wages, number of staff, advertising budget, car spaces, and location
   - Model evaluation using MSE and R²

4. **Customer Segmentation (K-Means Clustering)**
   - Segmenting stores into groups based on sales, wages, advertising, and staff count
   - Determining the optimal number of clusters using the Elbow Method
   - Model evaluation with Silhouette Score

5. **Association Rules (Apriori Algorithm)**
   - Studying the relationship between home delivery service and store location
   - Extracting frequent itemsets and association rules (Support, Confidence, Lift)

6. **Hierarchical Clustering**
   - Clustering stores using Ward linkage and a dendrogram
   - Determining the best number of clusters and evaluating with Silhouette Score

7. **RandomForestRegressor**
   - Predicting the 2014 customer basket value based on advertising budget and store age
   - Model evaluation using MAE and MAE percentage

8. **XGBClassifier**
   - Classifying whether a store opens on Sundays, based on features like competitors, state, trading hours, etc.
   - Classifying manager gender based on age, experience, and union percentage
   - Handling class imbalance using SMOTE
   - Model evaluation with Classification Report and Confusion Matrix

## 🛠️ Technologies & Libraries Used

- **Python**
- `pandas`, `numpy` – data processing
- `matplotlib`, `seaborn` – data visualization
- `scikit-learn` – regression, clustering, metrics
- `xgboost` – classification
- `imbalanced-learn (SMOTE)` – handling imbalanced data
- `mlxtend` – Apriori & association rules
- `scipy` – hierarchical clustering

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```

2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn mlxtend scipy openpyxl
   ```

3. Place the `StoresData.xlsx` file in the required path, or update the path in the code:
   ```python
   df = pd.read_excel('path/to/StoresData.xlsx')
   ```

4. Open and run the notebook:
   ```bash
   jupyter notebook last_mining.ipynb
   ```

## 📊 Key Findings

- **Location, wages, and advertising** are among the most influential factors affecting sales.
- Stores are grouped into two main segments: High-Value stores and Lower-Value stores, based on sales, wages, advertising, and staff count.
- There is a clear relationship between home delivery service and two specific store locations.
- The Random Forest model performed well in predicting basket value, with an error rate below 10%.

## 📌 Notes

- The dataset used (`StoresData.xlsx`) is not included in this project; it must be available with the same column names referenced in the code.
- Some code related to Hierarchical Clustering and Customer Segmentation assumes certain variables (e.g., `behavior_features`) are already defined — make sure to check this before running.

## 📄 License

This project is available for educational and research purposes.