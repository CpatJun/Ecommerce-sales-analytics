# Ecommerce Sales Performance & Customer Analytics Dashboard (Power BI)

## 📌 Project Overview
This Power BI dashboard analyzes e-commerce sales performance, order trends, profit margins, and customer purchasing behaviors. Designed for sales managers and business analysts, it provides actionable insights into key product categories, regional distribution, and payment channel preferences to drive revenue growth and operational efficiency.

![Dashboard Preview](dashboard_preview.JPG)

---

## 🔑 Key Features & Business Insights

1. **Executive KPI Overview**:
   - Track key performance metrics including **Total Revenue**, **Total Orders**, **Total Profit**, and **Average Order Value (AOV)**.

2. **Sales & Profit Trend Analysis**:
   - Monthly and quarterly breakdown of revenue trajectory to identify seasonal peaks and growth opportunities.

3. **Product & Category Performance**:
   - Deep dive into top-performing product categories and high-margin SKUs to optimize inventory and sales strategies.

4. **Customer & Payment Insights**:
   - Analysis of customer distribution and payment method adoption (e.g., Credit Card, Digital Wallet, Cash on Delivery).

5. **Interactive Filtering**:
   - Dynamic slicers for filtering by date ranges, sales regions, product categories, and fulfillment channels.

---

## 🛠️ Data Model & DAX Measures

### Core Business Metrics (DAX)

```dax
// Total Revenue Calculation
Total Revenue = SUM('Sales'[Sales Amount])

// Total Profit Calculation
Total Profit = SUM('Sales'[Profit])

// Profit Margin Percentage
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

// Total Orders Count
Total Orders = DISTINCTCOUNT('Sales'[Order ID])

// Average Order Value (AOV)
Average Order Value = DIVIDE([Total Revenue], [Total Orders], 0)
