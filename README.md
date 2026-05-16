# NovaMart Retail Analytics & Business Intelligence Project

## Overview

NovaMart Retail Analytics is an end-to-end Business Intelligence and Data Analytics project developed to analyze retail business performance, customer behavior, sales trends, product profitability, and customer segmentation between 2023–2025.

The project combines:

* PostgreSQL for data cleaning, transformation, feature engineering, and analytical SQL modeling
* Microsoft Power BI for dashboard development, KPI monitoring, and interactive business reporting
* RFM (Recency, Frequency, Monetary) Analysis for customer segmentation and churn-risk evaluation

The goal of the project was not only to build dashboards, but to generate actionable business insights and strategic recommendations from data.

---

# Business Problem

Retail businesses often struggle with:

* understanding revenue and profit drivers,
* identifying high-value customers,
* evaluating discount effectiveness,
* detecting churn risks,
* optimizing product performance,
* and transforming raw transactional data into strategic decision-making.

This project was designed to answer critical business questions such as:

* What drives revenue and profitability?
* Which customer segments generate the most value?
* Are discounts actually increasing revenue?
* Which products and categories perform best?
* Are customers becoming inactive or at risk of churn?
* Is business growth driven by acquisition or repeat purchases?

---

# Project Objectives

The project focused on:

* Analyzing overall business performance
* Evaluating sales and profit trends
* Measuring customer purchasing behavior
* Performing customer segmentation using RFM analysis
* Identifying high-value and at-risk customers
* Evaluating discount impact on revenue
* Building interactive executive dashboards
* Delivering business-focused recommendations

---

# Tools & Technologies Used

## Data & Database

* PostgreSQL
* SQL

## Business Intelligence & Visualization

* Microsoft Power BI
* DAX
* Power Query

## Analytics Techniques

* RFM Analysis
* Customer Segmentation
* KPI Analysis
* Trend Analysis
* Revenue & Profitability Analysis
* Churn Analysis
* Data Modeling

---

# Data Modeling

A star-schema-inspired relational model was implemented for optimized reporting and dashboard interactivity.

## Fact Table

* Transactions

## Dimension Tables

* Customers
* Products
* Stores
* Date Table

Custom SQL views were developed to support advanced analytics and segmentation workflows.

---

# Feature Engineering & SQL Work

Several analytical SQL views were created using PostgreSQL, including:

* Sales analysis views
* Customer analysis views
* RFM base calculations
* RFM scoring models
* Customer segmentation logic
* Revenue & profitability calculations
* Churn-focused recency analysis

RFM scoring was implemented using PostgreSQL window functions:

```sql
NTILE(5) OVER (ORDER BY recency)
NTILE(5) OVER (ORDER BY frequency)
NTILE(5) OVER (ORDER BY monetary)
```

During the project, deeper business analysis revealed an important analytical insight:

> Technical correctness does not always equal analytical correctness.

The project uncovered that:

* RFM scores are relative, not absolute
* Customers with high purchase frequency could still receive low frequency scores depending on population distribution
* Business logic validation is just as important as SQL implementation

This led to refinement of customer segmentation logic and improved business interpretation.

---

# Dashboard Pages

## 1. Executive Overview

Provides a high-level business performance summary including:

* Total Revenue
* Total Profit
* Average Order Value (AOV)
* Churn Rate
* Total Active Customers
* Revenue & Profit Trends
* Revenue by Customer Segment
* Revenue by Store
* Discount vs Revenue Trend

### Key Business Insights

* Revenue remained relatively stable across years
* Profit margins remained healthy (~26–27%)
* Customer acquisition growth appeared limited
* Revenue was concentrated among repeat customers and high spenders
* Discounts did not consistently drive proportional revenue growth

---

## 2. Sales & Product Performance

Focused on category, product, and payment analysis.

### Key Visualizations

* Revenue & Profit by Category
* Revenue by Product
* Profit by Product
* Payment Method Analysis
* Quantity vs Revenue by Subcategory
* Revenue by Region & Store

### Key Findings

* Fashion and Electronics dominated revenue generation
* Fashion emerged as the strongest growth category in 2025
* Product profitability differed significantly from revenue performance
* Mobile payments increased in adoption over time
* Some products relied heavily on pricing power while others depended on sales volume

---

## 3. Customer & RFM Analysis

Focused on customer behavior and segmentation.

### Key Visualizations

* Revenue by Age Group
* Customer Distribution by Gender
* Recency Distribution Analysis
* RFM Segment Bubble Analysis
* Top Customers Analysis

### RFM Segments

* VIPs
* Big Spenders
* Loyal Customers
* Potential Loyalists
* Regular Customers
* At Risk Customers
* Lost Customers

### Key Findings

* Big Spenders generated the highest monetary contribution
* Customer activity was strongest within the most recent 30-day period
* Top customers contributed a disproportionately large share of revenue
* At-risk and lost customers represented meaningful revenue leakage
* Younger customer demographics were underrepresented

---

# Key Business Insights

## Revenue & Profitability

* NOVAMART generated approximately $14.3M in revenue and $3.83M in profit
* Profit margins remained stable at ~26–27%
* Revenue trends were operationally stable across years

## Customer Insights

* Growth relied more on repeat purchases than customer acquisition
* Customer retention remained relatively healthy
* Revenue concentration created dependency risk on top customers

## Product Insights

* Fashion showed the strongest growth momentum
* Electronics remained a stable high-revenue category
* Groceries significantly underperformed relative to other categories

## Strategic Insights

* Discounts were not consistently effective in driving revenue spikes
* VIP customer contribution was weaker than expected
* Strong opportunities existed in customer retention and segmentation strategies

---

# Recommendations

The analysis produced several strategic recommendations:

* Strengthen customer acquisition strategy
* Improve VIP conversion and retention
* Optimize discount targeting and ROI analysis
* Expand high-performing product categories
* Reassess low-performing category profitability
* Increase customer personalization and loyalty campaigns
* Implement proactive churn prevention initiatives

---

# Challenges & Limitations

During analysis, a data quality issue was identified:

* Customer JoinDate values contained inconsistencies
* Some customers had 2025 join dates despite transactions existing in 2023

As a result:

* JoinDate was excluded from lifecycle-based analysis
* Business conclusions were adjusted to avoid misleading interpretations

This reinforced the importance of:

* validating data quality,
* validating business logic,
* and not relying solely on technical implementation.

---

# What This Project Demonstrates

This project demonstrates practical skills in:

* SQL analytics
* PostgreSQL querying
* Data cleaning & transformation
* Data modeling
* DAX calculations
* Power BI dashboard development
* RFM customer segmentation
* Business intelligence reporting
* KPI development
* Data storytelling
* Strategic business analysis

---

# Project Outcome

This project evolved beyond dashboard development into a complete business intelligence case study focused on:

* transforming raw transactional data into business insights,
* identifying operational opportunities,
* evaluating customer behavior,
* and supporting strategic decision-making through analytics.

---

# Author

Adeoti Oluwanifemi

Data Analyst | Business Analyst | SQL & Power BI Developer

