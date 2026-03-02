# Project Comprehensive Summary 
## Data Processing & Feature Engineering Pipeline 
This module implements a high-performance data cleaning and feature engineering pipeline designed for the Home Credit Default
Risk dataset. Leveraging Polars for memory-efficient processing, the workflow begins with an automated feature selection phase
using LightGBM and SHAP (SHapley Additive exPlanations), which identified and removed 18 non-predictive “noise” features. The
pipeline strictly enforces data quality by pruning columns with >90% missingness and performing rigorous type-checking. 
A key innovation in this workflow is the handling of high-cardinality categorical variables (e.g., ORGANIZATION_TYPE,
OCCUPATION_TYPE). Instead of standard One-Hot Encoding, which causes dimensionality explosion, we applied Weight of Evidence
(WoE) with Laplace Smoothing. This technique transformed qualitative job labels into quantitative risk scores, preserving predictive
signal while maintaining a compact feature space. The final output is a fully numeric, validated Parquet file, optimized for immediate
ingestion by gradient boosting models. 


## Machine Learning

- [Data Cleaning Report](https://vasif-asadov1.github.io/Home-Credit-Risk-Analysis/Machine%20Learning/01_data_cleaning.html)
- [ML Classification Models](https://vasif-asadov1.github.io/Home-Credit-Risk-Analysis/Machine%20Learning/02_ml_classification_models.html)

## SQL Analysis

- [DuckDB SQL Analysis](https://vasif-asadov1.github.io/Home-Credit-Risk-Analysis/SQL%20queries/duckdb_sql_analysis.html)
- [Feature Engineering with DuckDB SQL](https://vasif-asadov1.github.io/Home-Credit-Risk-Analysis/SQL%20queries/duckdb_feature_engineering.html)

Dataset Link: [Home Credit Default Risk Dataset](https://www.kaggle.com/competitions/home-credit-default-risk/data)
