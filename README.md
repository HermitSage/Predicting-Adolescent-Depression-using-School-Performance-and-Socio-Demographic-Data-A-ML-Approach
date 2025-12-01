# Predicting Adolescent Depression Using School Performance and Socio-Demographic Data: A Machine Learning Approach
## MSc Data Science Project – Coventry University

This repository contains the full implementation of a machine-learning framework designed to predict adolescent depression using structured demographic, academic, and health-related data from the Millennium Cohort Study (MCS) Sweep 7. The project evaluates multiple algorithms under class imbalance and incorporates SHAP interpretability to ensure transparency and ethical model behaviour.

## 1. Project Overview
Adolescent depression is a growing public-health concern, yet early identification remains difficult in non-clinical populations. This project investigates whether machine-learning models can support early risk detection using structured MCS survey data. Several classifiers are compared, and their interpretability is examined to ensure responsible and transparent use.

## 2. Objectives
Develop a classification model to predict adolescent depression using MCS Sweep 7 data.
Compare multiple machine-learning algorithms under class-imbalance conditions.
Evaluate performance using metrics appropriate for minority-class prediction.
Apply SHAP to interpret model outputs and examine potential bias.
Identify key sociodemographic, academic, and health features associated with depression risk.

## 3. Tools and Technologies
Python 3.10+
Google Colab (primary compute environment)
Scikit-learn, CatBoost, XGBoost
Pandas, NumPy, Matplotlib, Seaborn
SHAP for explainability

Hardware Used:
Intel Core i5-8250U CPU
8GB RAM
Local machine supplemented by Colab CPU/GPU

## 4. Dataset
Millennium Cohort Study – Sweep 7 (Age 17–18)
Accessed via UK Data Service under the End User Licence.
The dataset includes:
Sociodemographic characteristics
Household structure
Academic attainment (GCSE and National 5)
Physical health indicators
Psychological distress via the Kessler-6 (K6) scale

Target Variable:
Binary depression indicator derived from K6 ≥ 13 threshold.
Raw data is not included in this repository due to licensing restrictions.

## 5. Methodology Summary
### 5.1 Data Preprocessing
Removal of missing values and duplicates
Harmonisation of GCSE and N5 academic measures
Recoding of categorical demographic variables
### 5.2 Feature Engineering
Creation of Total_GCSE_N5 and A_Grades variables
Consolidation of academic performance indicators
### 5.3 Class Imbalance Handling
Balanced class weights (no SMOTE used for interpretability)
### 5.4 Model Training and Comparison
CatBoostClassifier, AdaBoostClassifier, RandomForestClassifier
XGBoostClassifier, Support Vector Classifier (RobustScaler)
K-Nearest Neighbours (RobustScaler)
### 5.5 Evaluation Metrics
F1-score for depressed class,
PR-AUC, ROC-AUC,
Weighted F1-score (for comparison with literature)
### 5.6 Interpretability
SHAP global importance plots
SHAP beeswarm and bar plots
Individual SHAP waterfall plots

## 6. Results Summary
Model	F1 (Weighted)	F1 (Depressed)	ROC-AUC
CatBoost	0.7521	0.3218	0.6773
AdaBoost	0.7795	0.2857	0.6400
Random Forest	0.7891	0.1805	0.5809
XGBoost	0.8053	0.1802	0.5797
SVC (RobustScaler)	0.7820	0.2335	0.5627
KNN (RobustScaler)	0.7960	0.2195	0.5861

#### Key Finding:
CatBoost provided the strongest performance across minority-class metrics and overall discriminative ability.

## 7. Interpretability Highlights (SHAP)
Gender identity, sexual orientation, chronic illness, household structure, and academic attainment were the most influential features.
SHAP results aligned with established psychosocial determinants of depression.
Interpretability was essential due to the sensitivity of mental-health predictions.

## 9. Legal and Ethical Compliance
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
Author: Rodrigue T
Programme: MSc Data Science – Coventry University

For questions or collaboration opportunities, feel free to get in touch.
