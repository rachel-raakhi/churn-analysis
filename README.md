# churn-analysis
End-to-end customer churn analysis using Python, Power BI and Logistic Regression — 18% churn rate, ₹12L revenue impact
# 📦 Boxify Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> End-to-end customer churn analysis for Boxify — an online subscription box service. Built using Python, Power BI, and Logistic Regression to identify why customers leave and recommend data-driven retention strategies.

---

## 📌 Business Problem

Boxify observed a rise in customer churn — subscribers cancelling before completing 6 months. Management wanted to:
- Reduce churn rate by **5–10%** over the next 6 months
- Identify **high-risk customer segments**
- Recommend strategies to **retain subscribers**

---

## 📊 Key Findings

| Metric | Value |
|---|---|
| **Churn Rate** | 18.0% (216 of 1,200 customers) |
| **Revenue Lost** | ₹12,17,042 |
| **Avg CLV — Active** | ₹14,017 |
| **Avg CLV — Churned** | ₹5,634 |
| **Avg Tenure — Active** | 22.6 months |
| **Avg Tenure — Churned** | 7.2 months |
| **Model Accuracy** | 83.7% (Logistic Regression) |

### 🔍 Critical Insights
- **Monthly subscribers churn at 20.5%** vs just 10.1% for Annual plan customers
- **Chennai (24.4%) and Hyderabad (24.2%)** are highest-risk cities
- **36–45 age group** has the highest churn at 20.3%
- **Engagement score** is a leading indicator — churned customers score 52.8 vs 61.8 for active
- **Active customers generate 2.5x more revenue** than churned customers

---

## 🛠️ Tools & Tech Stack

| Tool | Purpose |
|---|---|
| Python (pandas, NumPy) | Data loading, cleaning, feature engineering |
| Matplotlib, Seaborn | Visualisations (7 professional charts) |
| scikit-learn | Logistic Regression churn prediction model |
| Power BI | Interactive 3-page dashboard |
| Jupyter Notebook | End-to-end analysis environment |
| PowerPoint | Executive summary report (10 slides) |

---

## 📁 Repository Structure

```
boxify-churn-analysis/
│
├── Boxify_Churn_Analysis.ipynb      # Main Python notebook (EDA + ML)
├── boxify_customers_.csv            # Raw dataset (1,200 customers)
├── Boxify_Churn_Analysis_Report.pptx # 10-slide executive report
├── requirements.txt                 # Python dependencies
├── images/                          # All chart outputs
│   ├── 01_churn_overview.png
│   ├── 02_churn_by_subscription.png
│   ├── 03_churn_by_city.png
│   ├── 04_churn_by_age.png
│   ├── 05_engagement_analysis.png
│   ├── 06_clv_analysis.png
│   └── 07_predictive_model.png
└── README.md
```

---

## 🔧 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/rachel-raakhi/boxify-churn-analysis.git
cd boxify-churn-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook Boxify_Churn_Analysis.ipynb
```

---

## 📈 Analysis Walkthrough

### Step 1 — Data Loading & Cleaning
- Loaded 1,200 raw customer records
- Derived `Churn Status` from `CancelDate` (null = Active, date = Churned)
- Calculated `Subscription Months` for every customer
- Created `Age Group` buckets for demographic analysis
- Handled 984 intentional nulls in CancelDate (active customers — not a data error)

### Step 2 — Exploratory Data Analysis
Analysed churn across 6 dimensions:

| Dimension | Key Finding |
|---|---|
| Subscription Type | Monthly: 20.5% churn vs Annual: 10.1% |
| Geography | Chennai 24.4%, Hyderabad 24.2% (highest) |
| Age Group | 36-45 age group: 20.3% (highest) |
| Gender | Female: 19.3%, Male: 17.3% |
| Engagement | Churned avg: 52.8 vs Active avg: 61.8 |
| CLV | Active: ₹14,017 vs Churned: ₹5,634 |

### Step 3 — Predictive Modelling
Built a **Logistic Regression** model to predict churn:
- **Initial accuracy: 100%** — identified data leakage from `Subscription Months` feature
- **Removed leaky feature** — realistic accuracy: **83.7%**
- Top predictors: TotalSpent, BoxesReceived, EngagementScore

---

## 💡 Recommendations

### Quick Wins (0–3 months)
1. **Engagement Alert System** — Flag customers with score below 55, trigger personalised re-engagement offer → Expected: 3–5% churn reduction
2. **Annual Plan Incentive** — 15% discount for Monthly subscribers switching to Annual → Expected: significant retention uplift
3. **City Campaigns** — Targeted retention offers in Chennai, Hyderabad, Lucknow

### Long-Term (3–6 months)
4. **90-Day Onboarding Programme** — Structured touchpoints at Week 1, 4, 8, 12
5. **Loyalty Rewards** — Milestone rewards at 3, 6, 12 months
6. **Predictive Churn Dashboard** — Monthly churn risk scoring, proactive outreach to top 30 at-risk customers

---

## 📊 Power BI Dashboard

The interactive dashboard has 3 pages:
- **Page 1 — Executive Summary**: KPI cards, churn distribution, subscription analysis
- **Page 2 — Segment Analysis**: City, age group, gender, engagement breakdowns
- **Page 3 — CLV & Recommendations**: Financial impact, payment analysis, strategy summary

---

## 📚 Dataset

- **Source:** Synthetic dataset generated for business analytics training
- **Size:** 1,200 customers × 11 columns
- **Period:** 3 years of subscription data
- **Columns:** CustomerID, JoinDate, CancelDate, Age, Gender, Location, SubscriptionType, TotalSpent, BoxesReceived, EngagementScore, PaymentMode

---

## 👩‍💻 Author

**Raakhi Rachel Jose**
[LinkedIn](https://linkedin.com/in/raakhiracheljose) · [GitHub](https://github.com/rachel-raakhi)
