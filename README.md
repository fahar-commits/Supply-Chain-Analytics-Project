# Supply-Chain-Analytics-Project
🚀 Overview

This project demonstrates an end-to-end Supply Chain Analytics pipeline integrating database management, workflow automation, AI-assisted analysis, and executive dashboard design.

The objective was to analyze order fulfillment performance and generate business insights using real-world supply chain KPIs such as Line Fill Rate, Volume Fill Rate, On-Time %, In-Full %, and OTIF %.

The project combines:

PostgreSQL (Supabase) for structured data storage

n8n for workflow automation

Python for data cleaning & transformation

AI-assisted spreadsheet analytics (Quadratic)

Executive BI dashboard wireframing using Mokkup

🎯 Problem Statement

Supply chain teams often struggle with:

Partial order fulfillment

Delivery delays

Low OTIF (On-Time In-Full) performance

Limited visibility into customer-level performance

The goal of this project was to:

Consolidate multi-source datasets into a structured analytical model

Calculate operational KPIs at order and line levels

Identify top customers by order value and reliability metrics

Provide insights to improve supply chain reliability and fulfillment efficiency

🏗 Technical Architecture

Data Flow:

Gmail Trigger → n8n Workflow Automation → PostgreSQL (Supabase) → Python Cleaning & Merging → KPI Calculation → Executive Dashboard Wireframe

🛠 Tools & Technologies Used

PostgreSQL (Supabase) – Database setup & structured storage

n8n – Automated data ingestion and workflow orchestration

Python (Pandas) – Data cleaning, transformation & merging

SQL – Structured joins and querying

Quadratic (AI Spreadsheet) – Business KPI generation

Mokkup – BI dashboard wireframe creation

Exchange Rate API – Historical currency conversion

📂 Dataset Structure
Fact Tables

fact_order_line

fact_aggregate

Dimension Tables

dim_products

dim_customers

exchange_rate

🧹 Data Processing & Modeling

Converted product_id and customer_id to numeric format

Removed null and malformed records

Converted dates to datetime format

Merged fact & dimension tables

Applied historical USD to INR currency conversion

Created consolidated fact_summary table

Computed order-level and line-level KPIs

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

High Volume Fill Rate (96.6%) indicates strong overall quantity fulfillment.

Lower Line Fill Rate (65.9%) suggests partial SKU-level fulfillment.

OTIF at 47.3% highlights order-level reliability gaps.

Performance indicates coordination challenges between supply planning and distribution teams.

📊 Executive Dashboard

Designed an executive-ready supply chain performance dashboard including:

Core KPI summary cards

OTIF highlighted as reliability metric

Line vs Volume Fill comparison gauges

Top 5 customers (Global)

Top 5 customers (India Region)

Region & customer filters

The dashboard was wireframed using Mokkup for BI-ready export.

📌 Key Takeaways

Built full data pipeline from ingestion to insight generation

Applied structured data modeling principles

Demonstrated operational KPI interpretation capability

Integrated automation with analytics workflow

👨‍💻 Author

Fahar Ahmad
👨‍💻 Author

Fahar Ahmad
