# Enterprise Retail Analytics: Sales and Profitability Insights

## Overview
An end-to-end retail analytics solution that tracks revenue and profitability
across channels, store formats and customer segments.

## Business Problem
A retail business sells through three store formats (Express, Hyper, Super)
and three channels (Offline, Online, Omnichannel), but its transaction data is
spread across separate tables with no single view of performance. Management
needs to know:
- How much revenue and profit is the business generating, and at what margin?
- Which product categories, store formats and channels perform best?
- Which customer age groups contribute the most revenue?
- How do customers pay, and how does revenue build up across the year?

This project builds a SQL Server star schema and a 2-page Power BI dashboard
(Executive Summary, Regional and Channel Performance) that answers these
questions in one place.

## Tools & Technologies
- Microsoft SQL Server, T-SQL
- Power BI, DAX
- Star Schema data modeling

## Dataset
- 100,000+ retail records
- Source: [Kaggle / company-provided / synthetic]

## What I Did
- Prepared data in SQL Server using modular T-SQL views with DENSE_RANK() surrogate keys
- Designed a Star Schema semantic model in Power BI
- Created a DAX-generated fiscal calendar for time-intelligence reporting
- Built a 2-page interactive executive dashboard

## Key Insights
- **Overall performance:** The business generated 39.34M in revenue and 28.85M
  in profit, a 73.34% margin, with an average order value of 393.60 across
  roughly 100K transactions.
- **Categories:** All 9 product categories contribute similar revenue, in the
  4M to 5M range. Fruits and Grocery lead, and Dairy is the lowest. Margins sit
  at about 73% across every category, so no category is a clear loss-maker.
- **Store formats:** Express (13.0M) and Hyper (13.2M) generate nearly equal
  revenue, with margins of 73.3% to 73.4%. No single format dominates.
- **Channels:** Offline (13.05M), Omnichannel (13.16M) and Online (13.12M)
  each contribute about one-third of revenue, so the business is not
  dependent on one channel.
- **Payment modes:** UPI (25.2%), Card (25.1%), Wallet (25.0%) and Cash
  (24.8%) are used almost equally. UPI is marginally the highest, and Cash
  the lowest.
- **Customer age groups:** The 41-60 group is the largest identified segment
  at 10.1M (about 26% of revenue), followed by 25-40 at 8.0M. Under-25
  (3.4M) and 60+ (2.0M) contribute the least.
- **Data quality finding:** About 15.8M (roughly 40% of revenue) comes from
  customers with an unknown age group, which limits how reliable the
  age-based analysis is. Capturing customer age at billing would improve it.
- **Trend:** Cumulative YTD revenue builds steadily across the 12 months to
  about 39M, with no sharp spikes or drops.

## How to Use
1. Run the scripts in the `sql/` folder on SQL Server.
2. Open `dashboard/retail_dashboard.pbix` in Power BI Desktop.
