# E-commerce Customer Churn & Behavior Analysis

## Overview
This project analyzes customer-level e-commerce behavior to identify churn risk drivers, loyalty patterns, and retention opportunities.  
The focus is on interpretability and business insight, rather than model complexity or production deployment.



## Dataset
The dataset contains aggregated customer behavior metrics.  
Each row represents a unique customer and includes:

- **Total spend**
- **Purchase frequency**
- **Days since last purchase (recency)**
- **Loyalty membership tier**
- **Discount usage**
- **Customer satisfaction rating**



## Business Questions
- **Which customers are at high risk of churn?**
- **What behavioral factors drive churn risk?**
- **How do loyalty programs and discounts affect retention?**
- **Which customers should be prioritized for retention actions?**



## Methodology

### Exploratory Data Analysis
- Analyzed distributions of spend, frequency, recency, and ratings
- Identified inactivity and discount dependency as key churn signals
- Used correlation analysis to guide feature selection



### Feature Engineering
- Created RFM-inspired features (Recency, Frequency, Monetary)
- Engineered a composite loyalty score
- Built behavioral segments for interpretation
- Defined a **proxy churn label** based on customer inactivity  
  *(explicit churn labels were not available)*



### Machine Learning
Two interpretable models were used:

**Logistic Regression**
- Used as the primary model to understand churn drivers through coefficients

**Decision Tree**
- Used as a comparison model to validate behavioral patterns

Models were used to support insight generation, not as production churn systems.



### Visualization (Tableau)
An interactive Tableau dashboard was built to:
- Monitor churn risk distribution
- Compare churn by loyalty tier
- Visualize key drivers such as recency and satisfaction
- Support CRM and retention decision-making



## Key Insights
- Customer inactivity (recency) is the strongest indicator of churn risk
- Discount-driven customers show higher churn risk
- Higher loyalty tiers significantly reduce churn risk
- High-spend and high-loyalty customers are more stable
- Consistent patterns across models increase confidence in insights



## Model Performance Note
High model performance is expected due to the recency-based churn proxy, which introduces known target leakage.  
The models are positioned as behavioral insight tools, not production-ready predictors.


## Tableau Dashboard

Customer Churn & Loyalty Dashboard  
Tableau Public Link:  
https://public.tableau.com/views/CustomerChurnLoyalty/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

---

## Tools
- Python (pandas, scikit-learn)
- Logistic Regression, Decision Tree
- Tableau Public
- Jupyter Notebook
