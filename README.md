# Customer Churn Analysis - Telco 

## Overview 
A marketing focused churn analysis on a telecom customer dataset of 7,043 customers. The goal is to identify key churn drivers and produce an actionable risk-scored customer list that a marketing team can use to prioritize retention campaigns. 

This analysis approaches churn as a **business problem, not just a modeling exercise** — every finding is translated into a specific marketing recommendation. 

## Business Questions 
- What is the overall churn rate and what does it cost the business?
- Which customer segments are most at risk of churning?
- What factors drive churn — and which can marketing influence?
- Which specific customers should retention campaigns target first?

## Key Findings 
- Overall churn rate is **26.5%** - roughly 1 in 4 customers leaves
- Month-to-month contract customers churn at the highest rate
- Churn is most concentrated in the **first 12 months** of tenure
- Customers without TechSupport or OnlineSecurity churn at nearly double the rate of those with these services
- Churned customers paid higher average monthly charges, indicating pricing sensitivity

## Marketing Recommendations 
| Priority | Campaign | Target Segment |
|----------|----------|----------------|
|   High   | Contract Upgrade Campaign | Month-to-month customers, tenure < 12 months |
|   High   | 90-Day Onboarding Program | All new customers in months 1-3 |
| Medium-High | High-Value At-Risk Intervention | High Risk Tier, above-average charges |
| Medium | Support Services Upsell | Internet customers without TechSupport or OnlineSecurity |

## Model 
- **Algorithm:** Logistic Regression
- **Train/Test Split:** 80/20 with stratification
- **Evaluation:** Classification report + ROC-AUC score
- **Output:** Churn probability score for every customer

## Tools 
- Python 3.12
- Pandas — data manipulation
- Scikit-learn — modeling and evaluation
- Matplotlib - visualization

## Repository Structure 
customer-churn-analysis/

├── README.md

├── data/
│ └── (download dataset here — see Data Source below)
├── telco-customer-churn.ipynb
└── outputs/  
├── customer_churn_scores.csv
├── churn_by_contract.png
├── churn_by_tenure.png
├── churn_by_charges.png
├── churn_by_services.png
├── feature_importance.png
└── roc_curve.png

## Data Source 
IBM Sample Dataset - Telco Customer Churn 
Download from Kaggle and place in the '/data' folder:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn
