# Customer-Segmentation-Retention-Diagnostics

Overview

This project performs end-to-end customer retention analysis using SQL-driven segmentation and business-focused analytics.
The objective was to simulate a realistic ecommerce analytics scenario and identify retention risks through structured cohort analysis and RFM-based segmentation.

The project demonstrates how raw transactional data can be transformed into actionable business insights that inform marketing and retention strategies.

Business Objective

Many ecommerce teams lack clarity on:

Which customers are most valuable

Early warning signs of churn

Segment-specific engagement trends

This project aims to:

Define core retention metrics

Segment customers using RFM methodology

Identify engagement decay patterns

Provide data-backed retention recommendations

Dataset

A realistic synthetic retail dataset modeled after real ecommerce schemas.

Scale

6,500 customers

~10,000 transactions

Multi-year transactional timeline

Key Characteristics

Repeat purchase behavior

High-value customer skew (Pareto distribution)

Seasonal ordering patterns

Discount and return dynamics

Engineered engagement drop scenario

Data Schema
Transactions Table

transaction_id (UUID)

customer_id

order_date

product_category

channel (web/app/store)

payment_method

order_value

discount_applied

returned_flag

region

loyalty_member

signup_date

engagement_flag

Customers Table

customer_id

signup_date

acquisition_channel

region

loyalty_member

spend_propensity

initial_orders_estimate

high_value_flag

Tech Stack

SQL (MySQL) — data modeling, RFM segmentation, cohort analysis

Synthetic data engineering — controlled behavioral simulation

GitHub — version-controlled analytics workflow

(BI dashboard layer can be added using Power BI or Tableau)

Project Workflow
1. Data Ingestion

Imported raw CSV datasets into MySQL

Handled schema normalization

Resolved datatype inconsistencies (date parsing, numeric precision)

2. Data Validation

Row count verification

Null checks

Date sanity validation

Schema corrections using ALTER operations

3. Data Modeling

Raw → cleaned table transformation

Datatype normalization

Preparation for analytical queries

4. RFM Segmentation

Calculated:

Recency (last purchase gap)

Frequency (order count)

Monetary value (total spend)

Segmented customers into:

High Value

Loyal

At Risk

Low Engagement

5. Retention Analysis

Engagement trend monitoring

Segment-level behavioral analysis

Pre/post engagement comparisons

6. Insight Generation

Identified a significant engagement decline in high-value cohorts and explored potential business drivers through structured analysis.

Key Analytical Concepts Demonstrated

Customer lifetime segmentation

Retention diagnostics

Behavioral cohort analysis

SQL window functions

Data quality handling in real workflows

Business interpretation of analytical findings

Example Analytical Questions

Which customers contribute disproportionately to revenue?

How does engagement decay over time across segments?

Are high-value users showing early churn signals?

What behavioral signals indicate retention risk?

Repository Structure
customer-retention-rfm-analysis/
│
├── data/
│   ├── customers.csv
│   └── transactions.csv
│
├── sql/
│   ├── schema_setup.sql
│   ├── data_cleaning.sql
│   ├── rfm_segmentation.sql
│   └── retention_analysis.sql
│
├── notebooks/ (optional future layer)
│
└── README.md
Key Takeaways

Realistic customer data can be used to simulate production-grade analytics workflows

RFM segmentation remains a powerful baseline retention diagnostic

Early engagement decay in high-value cohorts is a critical business signal

Strong data foundations (schema + validation) are essential before insight generation

Future Improvements

Cohort retention curve visualization

Segment-level lifetime value modeling

Marketing intervention simulations

BI dashboard layer (Power BI / Tableau)

Channel attribution analysis
