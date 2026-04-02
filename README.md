# FinPulse 💳
### A Personal Financial Health Analytics Platform

FinPulse analyzes real credit card transaction data to generate a dynamic **Financial Health Score (0–100)** across 5 weighted KPIs — giving users a clear, data-driven picture of their spending habits and financial wellbeing.

---

## 🔗 Live Dashboard
👉 **[View the Tableau Dashboard](https://public.tableau.com/views/FinPulse-FinancialHealthDashboardJonahT/FinPulse-FinancialHealthDashboard-JonahT?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

---

## 📌 Project Overview

Most people have no idea how healthy their finances actually are. FinPulse solves that by treating personal finance like a vital sign — processing real transaction data through a custom scoring model and visualizing the results in an interactive dashboard.

This project covers the full data analyst workflow:
- Real-world data sourcing and cleaning
- SQL-style aggregations and KPI engineering in Python
- Custom weighted scoring model
- Interactive business intelligence dashboard in Tableau Public

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas, NumPy) | Data cleaning, KPI calculation, scoring model |
| Jupyter Notebook | Interactive analysis environment |
| Tableau Public | Dashboard and data visualization |
| GitHub | Version control and portfolio hosting |

---

## 📂 Project Structure

```
finpulse/
│
├── data/
│   ├── finpulse_transactions_clean.csv   # Cleaned transaction data
│   ├── finpulse_monthly_scores.csv       # Month-by-month health scores
│   └── finpulse_category_summary.csv     # Spending breakdown by category
│
├── finpulse_cleaning.ipynb               # Data cleaning pipeline
├── finpulse_score_model_v2.ipynb         # Financial Health Score model
└── README.md
```

---

## 📊 The Financial Health Score

The score (0–100) is calculated monthly using 5 weighted KPIs, each scored independently using only that month's transaction data:

| KPI | Weight | What it measures |
|-----|--------|-----------------|
| Savings Rate | 30% | % of estimated income not spent |
| Spending Stability | 20% | Low month-to-month variance (rolling 3-month CV) |
| Essential Ratio | 20% | Share of spend on needs vs wants |
| Avg Transaction Size | 15% | Spending discipline per purchase |
| Category Diversity | 15% | No single category dominates total spend |

**Grading scale:**
- 🟢 A: 80–100 — Excellent
- 🟢 B: 65–79 — Good
- 🟡 C: 50–64 — Fair
- 🔴 D: 35–49 — Poor
- 🔴 F: 0–34 — Critical

---

## 🔍 Key Findings

- Average Financial Health Score across all months: **87+/100 (Grade A)**
- The dataset reflects a consistently financially healthy customer profile with stable month-to-month spending patterns
- Spending is heavily concentrated in essential categories (groceries, health, transport), driving strong Essential Ratio scores
- Income was estimated as 1.3x peak monthly spend — a conservative assumption given the dataset contains transaction data only. A production version would ingest actual income data for a more precise savings rate calculation.

---

## 📈 Dashboard Features

- **Score Gauge** — dynamic circle showing the current month's health score, colored by score value
- **KPI Breakdown** — horizontal bar chart showing all 5 KPI scores side by side
- **Monthly Trend** — line chart tracking health score over time with a reference line at 65 (Good threshold)
- **Category Treemap** — visual breakdown of spending by category with % of total spend
- **Income vs Spend** — dual line chart showing the gap between estimated income and actual spending
- **Month Slider** — interactive filter applying to all sheets simultaneously

---

## 📁 Data Source

**Credit Card Transactions Dataset** — Kaggle  
1.8M+ real transaction records including date, amount, merchant, and spending category.  
🔗 [kaggle.com/datasets/priyamchoksi/credit-card-transactions-dataset](https://www.kaggle.com/datasets/priyamchoksi/credit-card-transactions-dataset)

---

## 👤 Author

**Jonatan Tepale**  
[LinkedIn](https://www.linkedin.com/in/jonatan-tepale-9175a5224/) · [Tableau Public](https://public.tableau.com/app/profile/jonatan.tepale/vizzes)
