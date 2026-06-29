# E-Commerce Customer Intelligence & Revenue Optimization Analysis

---

## Project Overview

This project analyzes customer purchasing behavior to uncover actionable business insights that support revenue growth, customer segmentation, and marketing decision-making. Using Python, SQL, and Power BI, the project explores customer demographics, spending patterns, subscription behavior, product performance, and promotional effectiveness to help an e-commerce business better understand its customers.

---

## Business Problem

E-commerce businesses generate large volumes of customer data, but without proper analysis it is difficult to identify:

- High-value customer segments
- Customer purchasing behavior
- Revenue-generating product categories
- Effectiveness of discounts and promotions
- Subscription impact on customer spending
- Opportunities for improving customer retention and revenue

This project aims to transform raw customer data into meaningful business insights that support data-driven decision making.

---

## Objectives

- Analyze customer purchasing behavior.
- Identify high-value customer segments.
- Evaluate the effectiveness of discounts and promotional campaigns.
- Compare spending patterns across different customer demographics.
- Examine subscription behavior and its relationship with customer spending.
- Build an interactive dashboard for business stakeholders.

---

## Dataset Information

| Attribute | Value |
| --------- | ----- |
| Records   | 3,900 |
| Features  | 18    |
| Domain    | E-Commerce Customer Behavior |

### Data Quality

- Handled **37 missing values** in `Review Rating` using category-wise median imputation.
- Removed inconsistencies in categorical values and standardized column names to lowercase.
- Discovered `promo_code_used` and `discount_applied` were 100% identical — redundant column dropped.
- Performed feature engineering to improve business analysis.

---

## Tools & Technologies

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **PostgreSQL / SQL** — Business queries and aggregations
- **Power BI** — Interactive dashboard development
- **Jupyter Notebook** — EDA and analysis workflow

---

## Project Workflow

1. Data Collection
2. Data Cleaning & Validation
3. Feature Engineering
4. Exploratory Data Analysis (EDA)
5. SQL Business Analysis
6. Power BI Dashboard Development
7. Business Insights
8. Business Recommendations

---

## Feature Engineering

New columns created to enrich the analysis:

| New Column | Description |
| ---------- | ----------- |
| `age_group` | Customers grouped into Young Adult / Adult / Middle Aged / Senior using quartile cuts |
| `purchase_category` | Purchase amount bucketed into Low / Medium / High / Premium tiers |
| `High_Value_Customer` | Customers at or above the median purchase amount flagged as high-value |
| `rating_category` | Review ratings mapped to Poor / Average / Good / Excellent |
| `purchase_frequency_days` | Frequency of purchase converted to numeric days (Weekly=7, Monthly=30, etc.) |

---

## SQL Business Questions Answered

1. Which age groups have the highest average order value and subscription rate?
2. Which product categories require discounts to generate higher revenue, and which sell well without discounts?
3. Which are the top products with the highest review rating but still low revenue?
4. Compare the average purchase amounts between Standard and Express Shipping.
5. Do subscribed customers spend more? Compare average spend and total revenue between subscribers and non-subscribers.
6. Which 5 products have the highest percentage of purchases with discounts applied?
7. Segment customers into New, Returning, and Loyal based on total previous purchases.
8. What are the top 3 most purchased products within each category?
9. Are customers who are repeat buyers (more than 5 previous purchases) also likely to subscribe?
10. What is the revenue contribution of each age group?
11. Top revenue-generating customer in each location.

---

## Key Insights

| Area | Insight |
| ---- | ------- |
| **Gender** | 68% male (2,652) vs 32% female (1,248) — significant gender imbalance in a fashion-focused domain |
| **Subscriptions** | Only 27% of customers are subscribed, yet subscribers spend 28% more than non-subscribers |
| **Repeat Behavior** | Average of 25 previous purchases per customer, indicating strong retention without a formal loyalty program |
| **Satisfaction** | Average review rating of 3.75/5 — below the 4.0 threshold competitive in e-commerce |
| **Top Category** | Clothing leads revenue with 1,737 transactions; Outerwear is the lowest performer |
| **Discounts** | 57% of customers buy at full price — blanket discounting is unnecessary for the majority |
| **Seasonality** | Spring is peak demand season (999 orders); off-peak seasons show notable drop-off |
| **Size Distribution** | Size M dominates at 45% of all orders (1,755 of 3,900) |
| **Geography** | Customers spread across all 50 US states; Montana is the top location (96 customers) |
| **Top Item** | Blouse is the most purchased single product across all 25 product types |

---

## Business Recommendations

### 1. Grow the Female Customer Segment `HIGH PRIORITY`

**Finding:** Female customers are only 32% of the base despite being the dominant demographic in fashion e-commerce.

**Action:** Allocate 30–40% of the marketing budget to female-targeted acquisition. Launch female-centric product lines and partner with women's lifestyle influencers.

---

### 2. Launch a Structured Loyalty and Subscription Program `HIGH PRIORITY`

**Finding:** Only 27% are subscribed, yet customers average 25 purchases. Strong repeat behavior exists without a formal retention vehicle.

**Action:** Introduce a tiered loyalty program (Bronze / Silver / Gold) with points per purchase, early sale access, and free shipping thresholds. Target the 73% non-subscribers with a conversion campaign highlighting the 28% spending advantage of subscribers.

---

### 3. Replace Blanket Discounts with Smart Targeted Promotions `MEDIUM PRIORITY`

**Finding:** 57% of customers purchase at full price. Uniform discounting erodes margin on customers who would buy anyway.

**Action:** Reserve discounts exclusively for lapsed customers and low-frequency buyers (Quarterly / Annual segments). Run A/B tests to find the minimum discount depth needed to re-activate dormant customers.

---

### 4. Improve Product Quality and Review Ratings `HIGH PRIORITY`

**Finding:** The average review rating is 3.75/5. Ratings below 4.0 hurt conversion rates in competitive markets. Several highly rated products remain underexposed in sales.

**Action:** Audit all SKUs rated below 3.5 and delist or improve them. Give 4.5+ rated products priority homepage and ad placement. Implement a post-purchase email flow to collect verified reviews.

---

### 5. Invest in Regional Inventory Optimisation `MEDIUM PRIORITY`

**Finding:** Customers span all 50 US states, with Montana emerging as the top location — a non-obvious rural market that may face shipping delays.

**Action:** Map top 10 states by order volume to the nearest fulfillment centers. Evaluate regional warehouse partnerships to reduce delivery time. Run geo-targeted promotions for high-performing states.

---

### 6. Double Down on Clothing; Grow Outerwear Seasonally `MEDIUM PRIORITY`

**Finding:** Clothing dominates with 1,737 transactions. Outerwear is the weakest category. Spring peaks at 999 orders — the strongest seasonal signal in the data.

**Action:** Increase Clothing inventory depth and ad spend ahead of Spring. Run dedicated Outerwear campaigns in March and September. Bundle Outerwear with Clothing or Accessories to lift average basket value.

---

### 7. Maximise Spring Seasonal Campaigns `QUICK WIN`

**Finding:** Spring is the peak demand season with 999 orders, significantly ahead of other seasons.

**Action:** Front-load Q1 advertising budgets. Plan exclusive Spring product drops and limited-edition collections. Use off-peak seasons to re-engage dormant customers with targeted offers.

---

### 8. Optimise Size-M Inventory and Enable Size-Based Cross-Sells `QUICK WIN`

**Finding:** Size M accounts for 45% of all orders (1,755 of 3,900), creating stockout risk across core product lines.

**Action:** Set M-size reorder points at 2x the threshold of other sizes. Use size-based personalisation in email and on-site recommendations to cross-sell accessories to M-size buyers.

---

### Executive Summary

The business has a strong repeat-purchase base (average 25 previous purchases) but three critical gaps are suppressing growth: a significant gender imbalance (only 32% female), a low subscription conversion rate (27%), and a mediocre average review rating (3.75/5). Fixing these three levers — through targeted female acquisition, a loyalty programme rollout, and product quality improvement — will deliver the highest compound impact on long-term revenue and customer lifetime value.

---

## Power BI Dashboard

The interactive dashboard provides:

- Revenue KPIs
- Customer demographics breakdown
- Product category performance
- Seasonal spending trends
- Subscription vs. non-subscriber analysis
- Discount effectiveness view
- Interactive filters for business exploration

> *(Add dashboard screenshots here.)*

---

## Project Structure

```text
├── data/
├── notebooks/
├── sql/
├── dashboard/
├── reports/
├── images/
├── README.md
└── requirements.txt
```

---

## Project Limitations

- The dataset contains one record per customer, preventing transaction-level analyses.
- RFM Analysis, Cohort Analysis, and Customer Lifetime Value (CLV) cannot be accurately calculated.
- Historical purchase timelines are unavailable, limiting customer retention analysis.
- Profitability analysis cannot be performed as operational costs are not included.
- Review ratings are numerical only — no written reviews available for sentiment analysis.

---

## Future Scope

- Perform RFM Analysis using transaction-level data.
- Build a Customer Churn Prediction model using historical customer behavior.
- Estimate Customer Lifetime Value (CLV) to identify high-value customers.
- Perform Cohort Analysis to measure customer retention over time.
- Develop a recommendation system for personalized product suggestions.
- Create a live Power BI dashboard connected to a production database.
- Incorporate marketing campaign and seasonal data for deeper business insights.

---

## Skills Demonstrated

- Data Cleaning & Validation
- Feature Engineering
- Exploratory Data Analysis (EDA)
- SQL for Business Analytics
- Customer Segmentation
- Data Visualization
- Dashboard Development
- Business Insight Generation
- Business Recommendation Framework

---

## Conclusion

This project demonstrates an end-to-end business analytics workflow — from data preparation and SQL analysis to dashboard development and actionable business recommendations. The analysis of 3,900 customers across 18 features reveals clear opportunities in gender-targeted marketing, subscription conversion, product quality improvement, and seasonal campaign planning. These insights provide a data-driven foundation for improving customer targeting, marketing optimisation, and long-term revenue growth.