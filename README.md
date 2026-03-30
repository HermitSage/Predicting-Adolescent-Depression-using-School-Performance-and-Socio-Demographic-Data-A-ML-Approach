## Predicting Adolescent Depression Using School Performance and Socio-Demographic Data: A Machine Learning Approach
🚀 *An interpretable machine learning framework for identifying depression risk in adolescents using school and socio-demographic data.*

### 📌1. Project Overview

Adolescent depression is a growing public health concern, yet early detection remains challenging due to reliance on clinical diagnosis.

This project explores how machine learning (ML) can be used to predict depression risk in adolescents aged 17–18 using non-clinical structured data, including:  
  
📊 Academic performance (GCSE / National 5)  
🏠 Socio-demographic factors  
❤️ Physical health indicators  
  
Using data from the UK Millennium Cohort Study (MCS) – Sweep 7, this study builds and compares multiple ML models to detect at-risk individuals and provide interpretable insights for early intervention.
## 2. 🎯 Objectives
- Build ML models to predict adolescent depression risk.  
- Identify key predictive factors influencing mental health.  
- Compare multiple algorithms (CatBoost, XGBoost, Random Forest, SVC, KNN).  
- Apply explainability techniques (SHAP & Permutation Importance).  
- Evaluate fairness across demographic groups.  
## 3. 📂 Dataset
Millennium Cohort Study – Sweep 7 (Age 17–18)
Accessed via UK Data Service under the End User Licence.
The dataset includes:
Sociodemographic characteristics
Household structure
Academic attainment (GCSE and National 5)
Physical health indicators
Psychological distress via the Kessler-6 (K6) scale
*Raw data is not included in this repository due to licensing restrictions.*

## 5. Methodology Summary
🔹 Data Processing
- Data cleaning & merging across multiple MCS datasets.  
- Handling missing values and duplicates.  
- Feature engineering for academic indicators
🔹 Class Imbalance Handling
- SMOTE (Synthetic Minority Oversampling Technique)
- Class weighting
🔹 Model Pipelines
- Pipeline A: CatBoost (native categorical handling)
- Pipeline B: One-Hot Encoding + Scaling (for SVC, KNN, etc.)
🔹 Evaluation Metrics
Due to class imbalance, priority was given to:
**F1-score (Depressed class)** ⭐
Precision-Recall AUC (PR-AUC)
Recall (Sensitivity)
ROC-AUC
*Accuracy (secondary metric)*

#### Key Finding:
CatBoost provided the strongest performance across minority-class metrics and overall discriminative ability.

## 6. Interpretability Highlights (SHAP)
Gender identity, sexual orientation, chronic illness, household structure, and academic attainment were the most influential features.
SHAP results aligned with established psychosocial determinants of depression.
Interpretability was essential due to the sensitivity of mental-health predictions.

## 7. Legal and Ethical Compliance
All work complied with UK GDPR and the Data Protection Act (2018).
Data access and use adhered to the UK Data Service End User Licence.
Ethical procedures followed Coventry University guidelines.
Sensitive predictors were analysed cautiously and interpreted with transparency.
No automated decision-making or individual profiling was conducted.

## 10. Future Work
Incorporate longitudinal predictors from earlier MCS sweeps.
Explore fairness-aware machine-learning algorithms.
Validate models using external datasets such as ALSPAC or LSYPE2.
Integrate multi-modal data (text, behavioural, digital indicators).
Develop practitioner-facing dashboards for explainable risk modelling.

#### Contact
Author: Rodrigue T.

Programme: MSc Data Science – Coventry University

For questions or collaboration opportunities, feel free to get in touch.
