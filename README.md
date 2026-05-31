# Business Analytics Capstone Project
### Foundations of Data Science | 2026

Synthetic Online Retail Dataset — Customer Behaviour and Sales Analysis

This project analyses 1,000 retail transactions to surface meaningful patterns in customer purchasing behaviour, product performance, and seasonal sales trends. The findings are intended to support data-driven decisions around inventory planning, pricing, and marketing.

---

## Author

Satvik Kesarwani

---

## Repository Structure

```
business-analytics-capstone-2025/
│
├── ds_assingment.ipynb                        # Main Jupyter Notebook — EDA and Visualizations
├── final_dataset.ipynb                        # Final cleaned dataset notebook
├── Business_Analytics_Presentation.pptx      # Project presentation slides
├── BUSINESS_ANALYTICS_REPORT_assingment.pdf  # Full written report (9 pages)
└── README.md                                  # Project overview
```

---

## Problem Statement

The objective of this analysis is to understand how customers behave across an online retail platform — what they buy, how much they spend, how they pay, and when they are most active. Working with a synthetic dataset of 1,000 transactions, the project applies data wrangling, visualisation, and insight generation to answer five core questions:

- Which product categories drive the most orders, and where should inventory be prioritised?
- How do customer demographics — age and gender — relate to spending behaviour?
- Does price influence how many items customers buy, or how they rate their experience?
- Which payment methods are most preferred, and what does that mean operationally?
- Are there seasonal patterns in sales that could inform promotional planning?

---

## Dataset Overview

| Attribute | Details |
|-----------|---------|
| Source | Kaggle — `synthetic_online_retail_data.csv` |
| Total Records | 1,000 rows |
| Original Features | 13 columns |
| Engineered Features | 1 (total_amount) |
| Product Categories | 5 |

### Feature Reference

| Category | Columns | Description |
|----------|---------|-------------|
| Customer | `age`, `gender` | Buyer demographics |
| Product | `category_name`, `product_name`, `price` | Item and pricing details |
| Order | `customer_id`, `product_id`, `order_date`, `quantity` | Transaction record |
| Payment | `payment_method` | Mode of payment used |
| Feedback | `review_score` | Customer satisfaction score (1–5) |
| Derived | `total_amount` | price x quantity — revenue per order |

---

## Data Wrangling

| Step | Action | Detail |
|------|--------|--------|
| Missing Values | Fill with mean | `review_score`: 103 null values filled with the column mean (3.99) |
| Missing Values | Fill with label | `gender`: null values replaced with "Unknown" — 103 records affected |
| Duplicates | Removed | All duplicate rows dropped to ensure data integrity |
| Data Type Conversion | Reformatted | `order_date` converted from object to datetime64 |
| Feature Engineering | New column created | `total_amount = quantity x price` — range: Rs.20.84 to Rs.2,437.65 |

---

## Visualizations

Eleven visualizations were produced across bar charts, pie charts, histograms, scatter plots, and a time-series line plot.

| No. | Chart | Type | Key Finding |
|-----|-------|------|-------------|
| 01 | Category Count | Bar Chart | Sports and Outdoors leads with 211 orders out of 1,000 |
| 02 | Gender Distribution | Pie Chart | Male 45.7%, Female 44.0%, Unknown 10.3% |
| 03 | Payment Method | Pie Chart | Cash on Delivery is dominant at 37.4% (374 orders) |
| 04 | Price Distribution | Histogram | Mean Rs.251.85 — most products fall in the Rs.100–Rs.400 range |
| 05 | Customer Satisfaction | Histogram | Mean rating 3.99 out of 5 — 75% of customers rated 5 stars |
| 06 | Quantity Distribution | Histogram | Average order size is 3 items — range of 1 to 5 |
| 07 | Price vs Quantity | Scatter Plot | No meaningful correlation — purchase quantity is price-independent |
| 08 | Age vs Total Spending | Scatter Plot | Age 30 averages Rs.1,013.60 — highest spending segment |
| 09 | Price vs Review Score | Scatter Plot | No correlation — higher price does not produce better ratings |
| 10 | Quantity vs Total Amount | Scatter Plot | Clear positive relationship — 5-item orders reach Rs.2,437.65 |
| 11 | Sales Over Time | Line Plot | Peak day: 12 August 2024 at Rs.8,788.71 — August is the strongest month |

---

## Key Findings

- **Most popular category:** Sports and Outdoors, with 211 orders — a narrow lead over the other four segments, reflecting broadly balanced demand across the catalogue.
- **Customer demographics:** The gender split is nearly even (45.7% male, 44.0% female), which argues against skewing marketing efforts toward either group.
- **Spending by age:** Customers aged 28–35 and 50–55 consistently outspend all other segments, with the highest average transaction values in the dataset.
- **Payment preferences:** Cash on Delivery accounts for 37.4% of transactions, but digital methods combined make up over 62% — indicating readiness to shift further toward cashless payments with the right incentives.
- **Price and quantity:** There is no evidence that higher prices discourage customers from buying more items. Purchase quantity appears to be driven by intent rather than price point.
- **Customer satisfaction:** The mean review score is 3.99 out of 5. While 75% of customers rated their experience at the maximum, isolated low scores represent a group worth following up with actively.
- **Seasonal trends:** August 2024 is the clearest peak period in the data, suggesting a consistent seasonal demand spike that should inform inventory and promotional decisions.

---

## Business Recommendations

| Priority | Area | Recommendation |
|----------|------|----------------|
| 01 | Inventory | Build up stock in Sports and Outdoors and Electronics ahead of August to prevent stockouts during peak demand |
| 02 | Pricing | Concentrate the product range within Rs.100–Rs.400, where customer demand is densest and conversion is highest |
| 03 | Payment | Offer cashback or discount incentives on UPI and digital wallet transactions to reduce Cash on Delivery operational overhead |
| 04 | Marketing | Direct higher spend toward the 28–35 and 50–55 age segments, which show the greatest revenue per customer |
| 05 | Retention | Reach out to customers who left a score of 3 or below — a targeted discount or support message can recover satisfaction and reduce churn |

---

## Tools and Technologies

- Python 3
- Jupyter Notebook
- Pandas
- Matplotlib and Seaborn
- NumPy

---

## Academic Context

This project was submitted as the Capstone Project for the Foundations of Data Science course, 2025. It is intended for academic evaluation purposes.

---

*Foundations of Data Science | Capstone Project 2025*
