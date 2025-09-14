# Loan Interest Rate Prediction  
## Overview:  
This is a project I created using the [Kaggle Credit Risk Default Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset) as a companion to my [Credit Default Risk](https://github.com/rmiller415/credit_default_risk) project. The Credit Risk Dataset has several missing values for the loan interest rate feature. I attempted to predict the loan interest rates here. However, I was ultimately unsuccessful at reliably predicting interest rates. I have abandoned this project, but I may return to it later if I find the time. My goal was to predict interest rates and use those predictions in the credit risk notebook.  
**Context:** In many business settings, datasets are incomplete and need to be found via imputation, collection of additional information, or other means. In some cases, imputation can cause issues with the algorithms or can lead to overfitting. I could not request the missing values because the dataset is synthetic and hosted on Kaggle. So I attempted to find the data on my own using patterns. I did this primarily to challenge myself and to show my familiarity with regressors and gradient descent.  

## Tools Used:  
### Python was used as the primary coding language.  
**Visualization:** Matplotlib and Seaborn  
**Data Storage/Structures:** Pandas and NumPy  
**Data Transformation and Feature Selection:** sklearn, scipy  
**Models:** sklearn (LinearSVR, RandomForestRegressor, GridSearch)  

## Methods:
**Data Visualization:** I sorted the loans by grade, intent, and min/max of interest rates to see what the loan grade feature meant. I made kernel density plots to view the distribution and look for skewness. I also looked for a correlation with the target (interest rate) with a heatmap of correlation coefficients.  
**Exploratory Data Analysis:** The EDA performed in the companion project (Credit Default Risk) was used to remove missing/outlier features and entries. The data entries with a missing interest rate were reserved for making predictions.   
**Feature Selection/Engineering:** I transformed the discrete and continuous features mathematically, then used k-fold t-tests to check which features were better. To find the best features.  

## Where I Left Off:  
I do not have a list of the best features. I have tried various transformations, encodings, and combinations. I cannot find a feature set that classifies more than ~30% of the test set correctly. I realize that I need to attempt to find a regression model that performs better. When I pick this project up again, I need to do the following.  

**Models To Try:**  
1. OLS, L1 LAsso Regression, L2 Ridge Regression - Simple, easy to impliment, quick.  
2. Gradient Boosting, XGBoost, LightGBM, CatBoost - *Benefits*:Easy to implement and able to handle more complex relationships between the features and the target. *Drawbacks:* Longer to train, requires larger datasets, and is more memory intensive.  
3. K-Nearest Neighbors - *Benefits:* Works with small data sets and can handle skewed datasets. *Drawbacks:* Longer prediction times, high chance of under/overfitting, memory intensive (must store entire dataset in memory).  
The list above is not a comprehensive list of models I was considering. More models are available in the notebook.

## Next Steps:  
1. Find a better model
2. Revisit the feature selection to find a set of features that works well
3. Retry other models with best features set
