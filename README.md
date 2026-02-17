# Employee Attrition ML Risk Analysis 

## Overview

This project analyzes workforce mobility patterns among data professionals to identify factors associated with job change risk. The objective is to understand attrition signals that organizations can use to improve retention strategies, reduce replacement costs, and preserve institutional knowledge.

## Why this matters

Turnover in technical roles leads to hiring costs, productivity loss, and project delays. Identifying early indicators of job transition risk enables companies to take proactive retention measures and make better workforce planning decisions.

## Dataset

Source: Kaggle HR Analytics Job Change dataset.

The dataset includes demographic, education, experience, company, and training attributes used to predict whether a professional is likely to change jobs.

Target variable: target → 1 indicates job change, 0 indicates retention

## Key Questions

• Which factors most influence job change decisions
• How does experience level relate to mobility risk
• Does training participation correlate with job transitions
• What organizational characteristics influence retention

## Approach

Data Preparation: 
1. handled missing values
2. encoded categorical variables
3. standardized numerical features

Exploratory Analysis
1. distribution and trend analysis
2. correlation exploration
3. feature impact observations

Modeling
Multiple models were trained and compared:

1. Logistic Regression

a. Decision Tree
b. Random Forest
c. K Nearest Neighbors

LightGBM - Class imbalance was addressed using balanced class weights.

## Key Insights

1. Early and mid career professionals show higher mobility risk compared to highly experienced workers

2. Training participation correlates with increased likelihood of job transitions, suggesting skill growth enables mobility

3. Company size and experience level strongly influence retention patterns

4. Education specialization and experience distribution contribute to transition probability

## Model Performance

1. Models were evaluated using classification accuracy and comparative performance.

2. Model	Accuracy
Decision Tree	Competitive baseline
Random Forest	Improved stability
Logistic Regression	Interpretable baseline
LightGBM	Strong predictive performance
KNN	Lower generalization performance

Future iterations should incorporate F1 score and ROC AUC for deeper evaluation.

## Business Implications

Organizations can use attrition risk indicators to:

a. identify high risk employee segments
b. refine retention and engagement strategies
c. align training programs with retention goals
d. improve workforce planning and talent investment

## How to Run
1. Install dependencies
pip install -r requirements.txt

2. Launch notebook
jupyter notebook notebooks/job_change_analysis.ipynb

3. Dataset
Download the dataset from Kaggle and place it in the data/ directory.
