# Customer Churn Prediction & Analytics
 
**Tools:** Python · scikit-learn · Pandas · Matplotlib · Seaborn · Power BI  
**Domain:** Product Analytics · Customer Intelligence · Predictive Modeling  
**Dataset:** IBM Telco Customer Churn · 7,032 customers · 21 features  
 
---
 
## Business Problem
 
A telecom company is losing 26.6% of its customers annually — $2.86M in revenue at risk. The goal of this project is to identify which customers are most likely to churn, understand why they leave, and provide data-driven retention recommendations that leadership can act on immediately.
 
---
 
## What I Built
 
### 1. Exploratory Data Analysis (`01_eda.ipynb`)
- Overall churn rate breakdown across 7,032 customers
- Churn rate by contract type — uncovering the headline insight
- Revenue at risk quantification: $2,862,927 (17.8% of total revenue)
- Tenure cohort analysis — identifying the first-year dropout pattern
- Customer stickiness analysis by number of services subscribed
- Correlation heatmap to check for multicollinearity before modeling
### 2. Predictive Model (`02_churn_model.ipynb`)
- Random Forest classifier trained on 5,625 customers, tested on 1,407
- TotalCharges excluded intentionally to prevent data leakage
- Threshold tuning from 0.50 → 0.35 to prioritise churn recall
- ROC curve and confusion matrix evaluation
- Feature importance analysis identifying top business drivers
- Dollar impact quantification: $1,754,422 net business value
- Exported scored CSV with churn risk labels for every customer
### 3. Power BI Dashboard (`dashboard.pdf`)
- 4 KPI cards: Total Customers, Churn Rate, Revenue at Risk, Net Value Saved
- Bar chart: Churn rate by contract type
- Donut chart: Customer risk segments (High / Medium / Low)
- Scatter plot: Monthly charges vs tenure coloured by risk level
### 4. Business Memo (`business_memo.docx`)
- Executive summary with at-a-glance KPI table
- 4 key findings with business context
- Model performance comparison (default vs tuned threshold)
- 3 strategic recommendations with expected impact
---
 
## Key Results
 
| Metric | Value |
|--------|-------|
| Overall churn rate | 26.6% |
| Model accuracy | 78% |
| ROC-AUC score | 0.809 |
| Churn recall (tuned) | 66.3% |
| Revenue at risk | $2,862,927 |
| Revenue model saves | $1,800,872 |
| Outreach cost | $46,450 |
| **Net business value** | **$1,754,422** |
 
---
 
## Key Findings
 
**1. Contract type is the single strongest churn driver**  
Month-to-month customers churn at 42.7% — 15 times higher than 2-year contract holders (2.8%). With 3,875 customers on month-to-month contracts, this is the highest-priority retention segment.
 
**2. First-year customers are the highest-risk cohort**  
Customers in their first 12 months churn at significantly higher rates. The model confirms tenure as a top feature — early engagement and onboarding investment directly reduces churn.
 
**3. High monthly charges + low tenure = highest churn probability**  
Customers paying above $65/month who are also in their first year represent the most at-risk combination. The scatter plot in the dashboard visualises this cluster clearly.
 
**4. The model flags 1,537 high-risk customers for immediate action**  
These customers have a predicted churn probability above 66%. Proactive outreach to this segment this quarter, at an estimated cost of $46,450, is projected to save $1.8M in revenue.
 
---
 
## Strategic Recommendations
 
1. **Contract upgrade incentive** — offer month-to-month customers a discount to switch to annual contracts at the 6-month mark. Converting 20% reduces base churn rate by ~6 percentage points.
2. **First-year retention program** — structured touchpoints at day 7, month 3, and month 6 for all new customers. This is where the churn is happening and where early intervention has the highest ROI.
3. **Proactive outreach to 1,537 high-risk customers** — prioritise those with highest risk scores + highest monthly charges. Estimated 38x ROI on outreach cost.
---
 
## Dashboard Preview
 
[![Dashboard](dashboard_screenshot.png)](https://github.com/AnukratiR/customer-churn-prediction/blob/main/dashboard_customer.png)
 
---
 
## Top Churn Drivers (Feature Importance)
 
1. Monthly charges
2. Tenure
3. Contract type
4. Internet service type
---
 
## Project Structure
 
```
customer-churn-prediction/
├── 01_eda.ipynb                  # Exploratory data analysis
├── 02_churn_model.ipynb          # Random Forest model + evaluation
├── churn_scored_final.csv        # All customers with risk scores
├── business_memo.docx            # Executive memo with recommendations
├── dashboard.pdf                 # Power BI dashboard export
├── dashboard_screenshot.png      # Dashboard preview
├── churn_by_contract.png         # EDA chart
├── tenure_churn.png              # EDA chart
├── feature_importance.png        # Model chart
├── confusion_matrix.png          # Confusion matrix
├── roc_curve.png                 # ROC curve
├── threshold_tuning.png          # Recall vs accuracy tradeoff
└── README.md
```
 
---
 
## Resume Bullet
 
> Built end-to-end customer churn prediction system (Python, Random Forest, ROC-AUC 0.811) on 7,032 records; identified $2.86M revenue at risk; tuned classification threshold to improve churn recall to 66%; built Power BI dashboard with risk segments and delivered 3 retention strategy recommendations with projected $1.75M net business value.
 
---
 
## Dataset
 
IBM Telco Customer Churn · [kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
