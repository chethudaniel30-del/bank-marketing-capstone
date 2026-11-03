# Bank Marketing Campaign Analysis and Customer Subscription Prediction

## Integrative Capstone Project | Virtual Data Science with Python Internship

### Project Overview

This project performs an end-to-end data science analysis of a bank marketing campaign dataset. It explores customer characteristics, identifies patterns associated with term deposit subscriptions, builds machine learning models to predict customer responses, and applies K-Means clustering to identify customer segments.

The project uses Python and popular data science libraries to demonstrate data cleaning, exploratory data analysis, supervised learning, unsupervised learning, model evaluation, and business insight generation.

## Objectives

- Analyse and clean the bank marketing dataset.
- Perform exploratory data analysis using statistical summaries and visualisations.
- Identify factors associated with customer subscription.
- Develop classification models using Logistic Regression and Random Forest.
- Evaluate model performance using multiple classification metrics.
- Apply K-Means clustering for customer segmentation.
- Generate insights and recommendations for marketing strategies.

## Dataset

**Source:** [UCI Machine Learning Repository: Bank Marketing](https://doi.org/10.24432/C5K306)

The `bank-additional-full.csv` dataset contains 41,188 records and 21 columns, including 20 input features and one target variable (`y`).

The target variable indicates whether a customer subscribed to a term deposit.

## Technologies and Libraries

- Python 3.12
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- python-docx

## Project Workflow

1. **Data Acquisition:** Downloaded and loaded the Bank Marketing dataset.
2. **Data Cleaning:** Identified and removed 12 duplicate records. Retained unknown categorical values as a separate category.
3. **Exploratory Data Analysis:** Examined numerical and categorical distributions, subscription patterns, and feature correlations.
4. **Preprocessing:** Applied StandardScaler and OneHotEncoder using a ColumnTransformer.
5. **Supervised Learning:** Developed Logistic Regression and Random Forest classification models.
6. **Model Evaluation:** Compared accuracy, precision, recall, F1-score, ROC-AUC, confusion matrices, and ROC curves.
7. **Feature Importance:** Analysed the most influential predictive features using Random Forest.
8. **Unsupervised Learning:** Applied K-Means clustering and evaluated cluster quality using the elbow method and silhouette score.
9. **Interpretation:** Analysed customer segments and developed marketing recommendations.

## Machine Learning Results

### Classification Performance

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 83.03% | 87.38% |
| Precision | 35.91% | 44.22% |
| Recall | 64.55% | 45.80% |
| F1-Score | 46.15% | 45.00% |
| ROC-AUC | 80.02% | 78.51% |

Logistic Regression achieved higher recall, F1-score, and ROC-AUC, while Random Forest achieved higher accuracy and precision.

### Important Features

The top predictive features identified by Random Forest included:

1. Age
2. Euribor three-month rate (`euribor3m`)
3. Campaign contacts (`campaign`)
4. Number of employees (`nr.employed`)
5. Employment variation rate (`emp.var.rate`)

Feature importance indicates predictive contribution and does not establish causation.

## Customer Segmentation Using K-Means

K-Means clustering was performed using customer demographic information and campaign history.

The optimal number of clusters selected was **K = 2**, based on silhouette analysis.

**Best silhouette score: 0.5406**

### Cluster Summary

| Measure | Cluster 0 | Cluster 1 |
|---|---:|---:|
| Customers | 39,596 | 1,580 |
| Average Age | 39.95 | 41.76 |
| Average Campaign Contacts | 2.60 | 1.84 |
| Average Previous Contacts | 0.11 | 1.73 |
| Subscription Rate | 9.24% | 61.96% |

Cluster 0 represents the larger customer segment, with a comparatively lower subscription rate. Cluster 1 is smaller but has a substantially higher observed subscription rate and more previous campaign contact.

## Key Insights

- The dataset exhibits class imbalance, with approximately 11.27% of customers subscribing.
- Subscription rates vary across job categories, contact methods, education levels, and campaign months.
- Logistic Regression identifies a larger proportion of actual subscribers than Random Forest at the selected classification threshold.
- Age and economic indicators contribute substantially to Random Forest predictions.
- K-Means identifies two customer segments with markedly different subscription rates.
- Customer segmentation may help support more focused marketing campaign strategies.

## Project Files

- `Bank_Marketing_Capstone.ipynb` - Complete Jupyter Notebook containing the analysis and implementation.
- `Bank_Marketing_Capstone_Report.docx` - Detailed project report.
- `bank_marketing_cleaned.csv` - Cleaned dataset with customer cluster labels.
- `*.png` - Visualisations generated during exploratory analysis, model evaluation, and clustering.

## Limitations

- The target variable is imbalanced.
- Historical campaign patterns may not generalise to future campaigns.
- Unknown categorical values were retained as separate categories.
- Feature importance and cluster subscription rates indicate associations, not causal relationships.
- The models require further validation on newer campaign data before real-world deployment.

## Conclusion

This capstone project demonstrates a complete data science workflow, combining exploratory analysis, supervised machine learning, and unsupervised customer segmentation. The results highlight how predictive modelling and customer profiling can provide useful insights for understanding bank marketing campaign outcomes.

## Author

Virtual Data Science with Python Internship  
Integrative Capstone Project  
2026
