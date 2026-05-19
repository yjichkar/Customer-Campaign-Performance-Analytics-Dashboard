# Customer Campaign Performance Analytics Dashboard
## 🛠 Tech Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-025E8C?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
</p>
## Project Overview
The Customer Campaign Performance Analytics Dashboard is an end-to-end business intelligence project developed using SQL, Python, and Power BI to analyze customer behavior, campaign effectiveness, and marketing performance.

The project simulates a real-world marketing analytics workflow where raw campaign and customer interaction data is transformed into actionable business insights.

This dashboard helps stakeholders:
- Monitor campaign performance metrics
- Analyze customer response behavior
- Track conversion and engagement trends
- Measure marketing effectiveness
- Identify customer segments
- Optimize campaign strategies using data-driven insights

---

# Business Problem

Marketing teams often run multiple campaigns across different channels, making it difficult to:
- measure campaign effectiveness,
- identify high-performing customer segments,
- monitor conversion rates,
- and optimize marketing spend efficiently.

The objective of this project was to build a centralized analytics solution that transforms campaign data into interactive dashboards and actionable insights for business decision-making.

---

# Objectives

The project focuses on:

- Monitoring customer campaign performance
- Tracking conversion and engagement metrics
- Analyzing customer response trends
- Segmenting customers based on behavior
- Measuring campaign ROI and effectiveness
- Building KPI-driven dashboards
- Generating actionable marketing insights

---

# Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data cleaning & transformation |
| SQL | Data analysis & KPI extraction |
| Power BI | Dashboard development & visualization |
| Pandas | Data preprocessing |
| DAX | KPI calculations |
| Excel / CSV | Source datasets |

---

# Dataset

The project uses customer marketing campaign datasets containing:
- Customer demographics
- Campaign response data
- Conversion metrics
- Marketing channels
- Purchase behavior
- Customer engagement
- Campaign performance indicators

Dataset Source:
- Marketing Campaign datasets from Kaggle

Reference Project:
- :contentReference[oaicite:0]{index=0}

---

# Project Workflow

The project follows an industry-standard end-to-end analytics workflow:

1. Data Collection
2. Data Cleaning & Transformation
3. Exploratory Data Analysis
4. SQL-Based Business Analysis
5. KPI Development
6. Dashboard Visualization
7. Insight Generation
8. Reporting & Documentation

---

# Data Cleaning & Preparation (Python)

Data preprocessing was performed using Python and Pandas.

## Key Data Cleaning Steps
- Removed duplicate records
- Handled missing/null values
- Standardized categorical data
- Converted date columns
- Cleaned customer demographic information
- Validated campaign response fields
- Created calculated marketing metrics

---

# Exploratory Data Analysis (EDA)

EDA was performed to identify:
- customer purchasing behavior,
- campaign engagement patterns,
- high-performing customer segments,
- and conversion trends.

## Key Analysis Areas
- Customer demographics
- Campaign acceptance rates
- Purchase frequency
- Spending patterns
- Channel performance
- Customer segmentation

---

# SQL Analysis

SQL was used to:
- extract campaign KPIs,
- analyze customer behavior,
- measure campaign performance,
- and generate business insights.

## SQL Concepts Used
- Aggregations
- GROUP BY
- JOINS
- Common Table Expressions (CTEs)
- Window Functions
- Subqueries
- Data Validation Queries

---

# Sample SQL Query

```sql
SELECT
    Campaign_Channel,
    COUNT(Customer_ID) AS Total_Customers,
    SUM(CASE WHEN Response = 'Accepted' THEN 1 ELSE 0 END) AS Converted_Customers,
    ROUND(
        SUM(CASE WHEN Response = 'Accepted' THEN 1 ELSE 0 END) * 100.0
        / COUNT(Customer_ID),2
    ) AS Conversion_Rate
FROM marketing_campaign_data
GROUP BY Campaign_Channel
ORDER BY Conversion_Rate DESC;
```

---

# Dashboard Features

## 1. Executive Campaign Summary

Provides a high-level overview of campaign performance.

### KPIs
- Total Customers
- Campaign Reach
- Conversion Rate %
- Customer Response Rate
- Revenue Generated
- ROI %
- Customer Retention %

### Visualizations
- KPI Cards
- Campaign Performance Trends
- Monthly Conversion Trends
- Revenue Analysis
- ROI Monitoring

---

## 2. Customer Segmentation Dashboard

Analyzes customer groups and behavioral patterns.

### Metrics
- Customer Segments
- Purchase Frequency
- Customer Spending
- Engagement Levels
- Demographic Analysis

### Insights Generated
- High-value customers
- High-conversion customer groups
- Low-engagement segments
- Purchase behavior trends

---

## 3. Campaign Effectiveness Dashboard

Focused on marketing performance evaluation.

### Metrics
- Conversion Rate
- Click-through Performance
- Campaign ROI
- Response Rate
- Channel Effectiveness

### Insights
- Best-performing campaigns
- Most effective channels
- Customer acquisition trends
- Campaign optimization opportunities

---

## 4. Customer Response Analysis

Tracks customer interaction and engagement trends.

### KPIs
- Positive Responses
- Negative Responses
- Engagement Rate
- Retention Rate

### Visualizations
- Response Trend Analysis
- Customer Activity Heatmaps
- Channel Engagement Charts

---

# DAX Measures Used

## Key KPIs
- Conversion Rate %
- ROI %
- Customer Response Rate
- Revenue Growth %
- Customer Retention %
- Campaign Effectiveness Score
- Running Totals

---

# Example DAX Measures

## Conversion Rate
```DAX
Conversion Rate % =
DIVIDE(
[Converted Customers],
[Total Customers],
0
) * 100
```

## ROI
```DAX
ROI % =
DIVIDE(
[Revenue Generated] - [Campaign Cost],
[Campaign Cost],
0
) * 100
```

## Customer Response Rate
```DAX
Response Rate % =
DIVIDE(
[Positive Responses],
[Total Customers],
0
) * 100
```

---

# Power BI Dashboard

The interactive dashboard includes:
- Dynamic filters & slicers
- KPI cards
- Drill-through analysis
- Trend visualizations
- Customer segmentation analysis
- Marketing performance reporting

The dashboard enables business users to:
- monitor campaign performance,
- identify growth opportunities,
- and optimize customer targeting strategies.

---

# Business Insights Generated

The project identified:
- High-performing marketing channels
- Customer groups with highest conversion potential
- Campaigns generating strongest ROI
- Seasonal engagement trends
- Customer retention opportunities

---

# Documentation & Reporting

The project includes:
- Data preparation documentation
- SQL query documentation
- KPI logic explanation
- Dashboard reporting logic
- Business recommendations

---

# Project Structure

```bash
customer-campaign-performance-analytics/
│
├── dataset/
│   └── marketing_campaign_data.csv
│
├── notebooks/
│   └── campaign_analysis.ipynb
│
├── sql/
│   └── campaign_queries.sql
│
├── dashboard/
│   └── campaign_dashboard.pbix
│
├── screenshots/
│   ├── executive_dashboard.png
│   ├── segmentation_dashboard.png
│   ├── campaign_dashboard.png
│   └── customer_response_dashboard.png
│
├── reports/
│   └── project_report.pdf
│
├── README.md
└── requirements.txt
```

---

# Dashboard Preview

## Executive Campaign Dashboard
(Add Screenshot Here)

## Customer Segmentation Dashboard
(Add Screenshot Here)

## Campaign Performance Dashboard
(Add Screenshot Here)

## Customer Response Dashboard
(Add Screenshot Here)

---

# Business Impact

This project helped:
- improve campaign monitoring,
- identify customer conversion trends,
- optimize marketing effectiveness,
- reduce manual reporting effort,
- and support data-driven marketing decisions.

---

# Future Enhancements

- Real-time campaign tracking
- Machine learning-based customer prediction
- Customer churn prediction
- Marketing recommendation system
- Automated reporting workflows

---

# Conclusion

This project demonstrates practical experience in:
- Marketing analytics
- SQL-based business analysis
- Python data preprocessing
- Power BI dashboard development
- KPI reporting
- Customer segmentation
- Campaign performance analysis
- Data storytelling

The dashboard provides actionable insights into customer behavior and campaign effectiveness through interactive analytics and visualization.
