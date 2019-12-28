# Predict Future Sales

## Problem description
A time-series dataset consisting of daily sales data is kindly provided by one of the largest Russian software firms. The task is to predict total sales for every product and store in the next month.

All datasets can be found here: [dataset](https://www.kaggle.com/c/competitive-data-science-predict-future-sales/data)

## Motivation
With accurate sales prediction, it guarantees that sufficient products will be manufactured or ordered to service customers on a timely basis, resulting in happier customers and fewer complaints. It can also help with sales planning, inventory controls, etc. In the end, it boosts the profit by increasing revenue and reducing the cost. 

## Project pipeline
* **Set up a metric:** According to the problem description, root mean square error (RMSE) is used to evaluate the performance. For regular classification problem, accuracy is selected as the evaluation metric; for unbalanced data, AUC is a useful metric.
*  **Exploratory data analysis (EDA):** Dive into the data to get some insights. This step includes visualizing data, developing a good understanding of data type, statistical information, data distribution, and analyzing correlations.
* **Data cleaning:** Based on EDA, outliers are either removed or replaced with the median of its group; duplicate records are removed; no missing values need to be dealt with.
* **Feature engineering:**  New features, such as month, days, city, statistical features, trend features, first sales and last sales, etc. are derived. Feature selection is performed to remove the features that has little correlation with the target value.  
* **Train/validation split:** The first 32 months are selected as training set; 33rd month is selected as validation set; 34th month is used as test set. 
* **Develop models:** Multiple machine learning algorithms (Linear Regression, Random Forest, xgboost) are applied to predictive modeling. Hyperparameters tuning is performed to optimize the performance.
* **Compare Performance:** * Among all the algorithms, xgboost has the best performance, achieving a RMSE of 0.91704 in the unseen test set.



