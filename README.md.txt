🚀 Overview

This project demonstrates an end-to-end Supply Chain Analytics pipeline integrating database management, workflow automation, AI-assisted analysis, and KPI dashboarding.

The objective was to analyze order fulfillment performance and generate business insights using real-world supply chain KPIs such as Line Fill Rate, Volume Fill Rate, On-Time %, In-Full %, and OTIF %.

The project combines:

PostgreSQL (Supabase) for data storage

n8n for workflow automation

Python for data cleaning & transformation

AI-assisted spreadsheet analytics (Quadratic)

Business KPI dashboarding

🎯 Problem Statement

Supply chain teams often struggle with:

Partial order fulfillment

Delayed deliveries

Low OTIF (On-Time In-Full) performance

Limited visibility into customer-level performance

The goal of this project was to:

Consolidate multi-source data into a structured analytical dataset

Calculate key operational KPIs

Identify top-performing and underperforming customers

Provide insights to improve order reliability

🏗 Technical Architecture

Data Flow:

Gmail Trigger → n8n Automation → PostgreSQL (Supabase) → Python Cleaning & Merging → KPI Calculation → Dashboard Insights

🛠 Tools & Technologies Used

PostgreSQL (Supabase) – Database setup & storage

n8n – Automated data migration workflows

Python (Pandas) – Data cleaning & transformation

Quadratic (AI Spreadsheet) – Business analysis

Exchange Rate API – Currency conversion

SQL – Table joins and structured querying

📂 Dataset Structure
Fact Tables

fact_order_line

fact_aggregate

Dimension Tables

dim_products

dim_customers

exchange_rate

🧹 Data Processing Steps

Converted product_id and customer_id to numeric

Removed null and malformed records

Converted dates to datetime format

Merged fact & dimension tables

Converted USD prices to INR using historical exchange rates

Created consolidated fact_summary table

Calculated total order value in INR

📊 Key Supply Chain KPIs
KPI	Value
Total Orders	7,273
Total Order Lines	12,978
Line Fill Rate	65.96%
Volume Fill Rate	96.61%
On-Time Delivery %	70.29%
In-Full Delivery %	65.96%
OTIF %	47.26%
📈 Business Insights

Volume Fill Rate (96.6%) indicates strong quantity fulfillment performance.

Line Fill Rate (65.9%) suggests frequent partial order fulfillment at line level.

OTIF performance is only 47.3%, meaning less than half of orders are delivered both on time and in full.

Indicates reliability gap at order level despite strong volume performance.

Improvement focus required in coordinated delivery timing and complete fulfillment.

🧠 Supply Chain Concepts Used

Order vs Order Line

Line Fill Rate – % of order lines fully shipped

Volume Fill Rate – % of quantity shipped

On-Time % – Delivered within agreed timeline

In-Full % – Delivered complete quantity

OTIF % – Delivered On-Time AND In-Full

🔄 Workflow Automation

Using n8n:

Gmail API OAuth configured

Automated data ingestion into PostgreSQL

Reduced manual data transfer

📊 Dashboard

The project includes a KPI dashboard summarizing:

Core operational metrics

Top 5 customers (Global)

Top 5 customers (India)

Order fulfillment performance

📌 Key Takeaways

Built complete data pipeline from ingestion to insights

Applied structured data cleaning & transformation

Demonstrated real-world supply chain KPI understanding

Integrated automation with analytics

👨‍💻 Author

Fahar Ahmad

