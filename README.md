Customer Shopping Behavior Analysis

End-to-end data analytics project exploring customer purchase patterns, segments, and product performance using Python, SQL, and Power BI.

## Overview

This project analyzes a retail dataset of 3,900 customer transactions to uncover spending patterns, customer segments, product performance, and subscription behavior. The workflow covers the full analytics pipeline: data cleaning in Python, business querying in SQL, dashboard building in Power BI, and a summarized report.

## Dataset

- **Size:** 3,900 rows · 18 columns
- **Features:** Customer demographics, purchase details, item/category info, shipping type, discount usage, subscription status, review ratings, and purchase frequency
- **Data quality:** 37 missing values in Review Rating, imputed using category median

## Tools Used

| Tool | Purpose |
|---|---|
| Python (pandas) | Data loading, cleaning, EDA, feature engineering |
| PostgreSQL | Business-question SQL querying |
| Power BI | Interactive dashboard and visualization |
| Gamma | PDF summary report |

## Steps

1. **Load & Explore** – Loaded the CSV into pandas; reviewed structure with `df.info()` and `df.describe()`
2. **Clean Data** – Imputed missing Review Ratings by category median; dropped the redundant `Promo Code Used` column
3. **Feature Engineering** – Created `age_group` and `purchase_frequency_days` for deeper segmentation
4. **Database Integration** – Standardized columns to snake_case and loaded the cleaned dataset into PostgreSQL
5. **SQL Analysis** – Wrote 10 business queries covering revenue by gender, discount behavior, top products, shipping comparison, subscriber spend, customer segmentation, and repeat-buyer trends
6. **Dashboard** – Built an interactive Power BI dashboard for visual exploration
7. **Reporting** – Compiled findings into a PDF report using Gamma

## Dashboard

The Power BI dashboard includes:
- Subscription split (donut chart): 27% subscribed vs. 73% not subscribed
- Revenue and sales by product category
- Revenue and sales by age group
- Key metrics: 3.9K customers, avg. purchase $59.76, avg. rating 3.75

## Key Results

- **Revenue by gender:** Male $157,890 vs. Female $75,191
- **High-spending discount users:** 839 customers spent above average despite using discounts
- **Top-rated products:** Gloves (3.86), Sandals (3.84), Boots (3.82)
- **Most discount-dependent products:** Hat (50%), Sneakers (49.66%), Coat (49.07%)
- **Shipping:** Express shipping customers spend slightly more on average ($60.48 vs. $58.46)
- **Customer segments:** Loyal 3,116 · Returning 701 · New 83
- **Repeat buyers:** More likely to subscribe (958 subscribed vs. 2,518 not subscribed)
- **Top category by revenue:** Clothing (~$100K), followed by Accessories (~$50K)

## Business Recommendations

- Promote subscription benefits to boost the 27% subscriber base
- Launch loyalty rewards to retain the large "Loyal" customer segment
- Review discount strategy on high-dependency products to protect margins
- Feature top-rated and best-selling items in marketing campaigns
- Target high-revenue age groups and express-shipping 
