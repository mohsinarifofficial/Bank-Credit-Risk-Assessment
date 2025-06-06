# Bank-Credit-Risk-Assessment
This project focuses on building a predictive model for credit default risk, aiming to identify loan applicants likely to default (defined as repayment delays exceeding 90 days). The dataset was multilingual and required substantial preprocessing, translation, and transformation to enable robust modeling.


Key Components:
1. Data Translation and Localization:
Translated Russian column headers, education levels, gender values, and industry categories into English.

Normalized and mapped over 400+ city and settlement names from Cyrillic to their English equivalents to support regional analysis.

Unified region names for consistent geographic segmentation (e.g., “Минская область” → “Minsk Region”).

2. Exploratory Data Analysis (EDA):
Analyzed demographics (age from BIRTHDATE), salary distributions, education types, and loan patterns.

Visualized overdue patterns across top 10 cities, industries, and loan repetition behavior using pie charts, KDE plots, and count plots.

3. Feature Engineering:
Created a binary target variable Overdue for repayment delays > 90 days.

Engineered TOOK_ANOTHER_CREDIT to capture recurring borrowers.

Applied LabelEncoding on all categorical features including complex ones like industry, area, and credit history rating.

Imputed missing categorical and numeric data using KNNImputer with careful handling of encoded values.

4. Feature Selection and Correlation Analysis:
Conducted correlation matrix (heatmap) and Variance Inflation Factor (VIF) analysis to remove multicollinearity.

Dropped Primary limit due to strong correlation with Debt, based on both VIF and feature importance.

5. Model Training & Evaluation:
Trained a Logistic Regression model with balanced class weights to handle imbalance in overdue cases.

Scaled features using StandardScaler and split the data using stratified sampling.

Evaluated performance using:

Classification Report

ROC Curve and AUC

Precision-Recall Curve

Gini Coefficient as a risk score


