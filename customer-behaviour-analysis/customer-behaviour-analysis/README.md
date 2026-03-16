# Customer Behaviour Analysis – E-Commerce Dataset

An exploratory data analysis project looking at how customers shop, spend, and engage with an e-commerce platform. The dataset has 350 customers with information on their spending, membership tier, satisfaction, and purchase recency.

I did this project to practice working with customer-level data rather than transaction-level data — it's a different kind of EDA where you're trying to understand *who* the customers are rather than *what* they bought.

---

## Questions I wanted to answer

- Do Gold/Silver/Bronze members actually spend differently?
- Does applying a discount lead to higher spending?
- What does the gap between repeat and one-time buyers look like?
- Is there a relationship between age and spending?
- Which cities have the highest value customers?
- How does satisfaction level connect to spending and membership?

---

## Dataset

**Source:** [E-Commerce Customer Behavior Dataset – Kaggle](https://www.kaggle.com/datasets/uom190346a/e-commerce-customer-behavior-dataset)  
**File:** `data/customer_behavior.csv`  
**Size:** 350 rows × 11 columns

Columns: `Customer ID`, `Gender`, `Age`, `City`, `Membership Type`, `Total Spend`, `Items Purchased`, `Average Rating`, `Discount Applied`, `Days Since Last Purchase`, `Satisfaction Level`

---

## Project structure

```
customer-behaviour-analysis/
│
├── data/
│   └── customer_behavior.csv
│
├── notebooks/
│   └── customer_behaviour_analysis.ipynb
│
├── outputs/
│   └── (charts saved here when you run the notebook)
│
├── requirements.txt
└── README.md
```

---

## Key findings

1. **Membership tier is the strongest predictor of spend** — Gold members spend an average of $1,311 vs $473 for Bronze. That's nearly a 3x difference.

2. **Discounts don't increase spending** — customers who received a discount actually spent *less* on average ($787) than those who didn't ($903). Discounts may be attracting lower-value customers.

3. **64% of customers purchased within the last 30 days** — a healthy retention rate, but the remaining 36% haven't bought in over a month and may need re-engagement.

4. **Satisfaction is strongly tied to membership tier** — Gold members are mostly Satisfied, Bronze members skew Unsatisfied. This could mean the membership benefits aren't delivering equal value.

5. **No strong age effect on spending** — customers range from 26 to 43 years old and age alone doesn't predict how much they spend.

6. **San Francisco and New York have the highest average spend per customer** — Houston and Miami trail behind significantly.

---

## How to run

```bash
git clone https://github.com/kenisha-ranawat/customer-behaviour-analysis
cd customer-behaviour-analysis
pip install -r requirements.txt
jupyter notebook notebooks/customer_behaviour_analysis.ipynb
```

---

## Requirements

```
pandas
matplotlib
seaborn
jupyter
```

---

## What I'd explore next

- Build a simple customer segmentation using KMeans clustering on spend + items purchased
- Predict satisfaction level using logistic regression
- Look at whether discount strategy should be changed based on membership tier

---

*Learning project — part of my data science coursework practice.*
