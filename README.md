# 📊 COVID Behavior and Vaccine Modeling

## 📁 Project Overview

This project predicts U.S. county-level COVID test positivity and vaccine uptake using behavioral survey data. It combines regression modeling (XGBoost, NeuralNet) and policy-aware clustering to inform targeted public health interventions.

## 🧠 Key Objectives

- Predict vaccine uptake and test positivity using survey features
- Impute missing data using proxy models (XGB/RF)
- Engineer interpretable features
- Cluster counties by beliefs/behaviors
- Recommend policies based on model-aligned insights

## 🔧 Pipeline

1. `01_data_cleaning.ipynb` — Imputation (KNN vs contextual), outlier handling
2. `02_feature_engineering.ipynb` — Feature transformations and correlation pruning
3. `03_modeling_vaccine_uptake.ipynb` — Model comparison and feature importance
4. `04_modeling_covid_positive.ipynb` — Same for positivity
5. `05_policy_analysis.ipynb` — Clustering and actionable segmentation

## 🧪 Final Model Performance

| Task | Model | R² | MAE | RMSE |
|------|-------|----|-----|------|
| Vaccine Uptake | NeuralNet / XGBoost | 0.71 | ~2.6 | ~3.5 |
| Test Positivity | XGBoost | **0.82** | ~2.0 | ~2.6 |

## 🧩 Key Insights

- Vaccine uptake is driven by intent, temporal features, and belief in public health bodies.
- COVID positivity aligns with illness reports and mobility behaviors.
- Cluster analysis reveals mismatches between risk and behavior—informing outreach strategies.

## 📥 How to Run

1. Clone repo
2. `pip install -r requirements.txt`
3. Run notebooks in order
4. Optionally explore clusters in `05_policy_analysis.ipynb`

## 🧾 Data Source

The dataset used in this study is derived from the COVID-19 Trends and Impact Survey (CTIS), conducted by the Delphi Group at Carnegie Mellon University. This dataset ag-
gregates responses from a representative sample of Facebook users (aged 18+) at the U.S. county level. Responses were gathered during one-month time frame at the peak of the
COVID pandemic (from January 07, 2021 to February 12, 2021), offering rich information to analyze temporal dynamics in health behaviors and perceptions. The dataset contains 25627 instances where each row represents one U.S. county in a given day.

## 👤 Author

Connie Lo (Carnegie Mellon University)
Machine Learning in Problem Solving Course
