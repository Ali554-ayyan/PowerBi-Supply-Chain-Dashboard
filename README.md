# SupplyChain Pro - Supply Chain Performance Dashboard

An interactive, two-page Power BI dashboard that analyzes sales, profitability, order fulfilment and delivery performance across global markets.

## Table of Contents

1. Project Overview
2. Business Objectives
3. Dashboard Structure
4. Page 1: Overview
5. Page 2: Logistics
6. KPI Definitions
7. Interactive Features
8. Key Insights
9. Recommendations
10. Tools and Technologies
11. Data Preparation and Workflow
12. How to Use
13. Repository Structure
14. Future Enhancements

## 1. Project Overview

SupplyChain Pro is a business intelligence project built in Microsoft Power BI. It combines order, sales, customer and shipping data into a single decision-support dashboard.

The report is divided into two pages:

- Overview: commercial performance, covering sales, profit, customers, regional and market contribution, and monthly trends.
- Logistics: operational performance, covering shipping days, scheduled days, late and on-time deliveries, shipping modes and order status.

The dashboard helps answer questions such as:

- How much revenue and profit is the business generating?
- Which regions and markets contribute the most to sales?
- How reliable are deliveries, and how many orders arrive late?
- How does actual shipping time compare with scheduled time?
- What share of orders are complete, pending, on hold or canceled?

## 2. Business Objectives

- Create one source of truth for sales and logistics metrics.
- Monitor delivery performance across late, on-time, advance and canceled shipments.
- Compare actual and scheduled shipping days for each shipping mode.
- Identify top-performing regions and markets by sales.
- Track monthly sales, profit and late-delivery trends.
- Allow users to explore the data on their own using filters and cross-filtering.

## 3. Dashboard Structure

Both pages share the same layout: a branded header, four global filters, a row of KPI cards, the main charts, and navigation buttons at the bottom to switch between pages.

Global filters (apply to every visual on the page):

- Order Date
- Market
- Order Region
- Product Category

## 4. Page 1: Overview

Purpose: a high-level view of commercial performance.

### KPI Cards

| KPI | Value |
|-----|-------|
| Total Sales | 36.78M |
| Total Orders | 66K |
| Total Profit | 3.97M |
| Total Customers | 21K |
| Avg Shipping Days | 3.50 |
| Category Selected | All (changes with the Product Category filter) |

### Visuals

| Visual | Chart Type | Description |
|--------|-----------|-------------|
| Late Delivery % by Month | Line chart | Shows how the late-delivery rate changes from January to December and highlights months with spikes. |
| Total Sales by Region | Column chart | Ranks regions by total sales: Western Europe, Central America, South America, Northern Europe, Southern Europe and Oceania. |
| Total Orders by Delivery Status | Pie chart | Shows the share of orders that are late, advance-shipped, shipped on time or canceled. |
| Total Sales and Total Profit by Month | Clustered column chart | Compares monthly sales with monthly profit. |
| Sales and Product Price Summary by City | Scatter plot | Shows the relationship between product price and sales at city level and helps spot outlier cities. |
| Total Sales by Market | Waterfall chart | Shows how each market (Europe, LATAM, Pacific Asia, USCA, Africa) adds up to total sales. |

## 5. Page 2: Logistics

Purpose: a detailed view of delivery performance and order fulfilment.

### KPI Cards

| KPI | Value |
|-----|-------|
| Avg Shipping Days | 3.50 |
| Avg Scheduled Days | 2.93 |
| Late Delivery % | 0.55 (about 55%) |
| On-Time % | 0.18 (about 18%) |
| Total Orders | 66K |
| Canceled Orders | 1K |

### Visuals

| Visual | Chart Type | Description |
|--------|-----------|-------------|
| Total Sales by Region | Map | Shows the geographic spread of sales across the world. |
| Total Orders by Shipping Mode and Delivery Status | 100% stacked bar chart | Compares delivery outcomes (advance shipping, late delivery, shipping canceled, shipping on time) across Standard Class, Second Class, First Class and Same Day. |
| Late Delivery % | Gauge | Shows the current late-delivery rate on a scale from 0 to 1.10. |
| Total Orders by Delivery Status | Pie chart | Shows the overall share of each delivery status. |
| Total Orders by Order Status | Treemap | Shows the order pipeline: Complete, Pending Payment, Processing, Pending, Closed, On Hold, Suspected Fraud, Canceled and Payment Review. |
| Avg Shipping Days and Scheduled Days | Column and line combo chart | Compares actual shipping days with scheduled days for each shipping mode. |

## 6. KPI Definitions

- Total Sales: sum of the sales amount of all filtered orders.
- Total Profit: sum of the profit of all filtered orders.
- Total Orders: number of unique orders.
- Total Customers: number of distinct customers.
- Avg Shipping Days: average number of days actually taken to ship an order.
- Avg Scheduled Days: average number of days planned for shipping an order.
- Late Delivery %: late-delivery orders divided by total orders.
- On-Time %: on-time orders divided by total orders.
- Canceled Orders: number of orders with a canceled status.
- Profit Margin: total profit divided by total sales (about 10.8% in the unfiltered view).

## 7. Interactive Features

- Four global filters (Order Date, Market, Order Region, Product Category) update every visual on the page.
- Cross-filtering: selecting an element in one chart filters the other charts on the page.
- KPI cards update dynamically with every filter selection.
- Navigation buttons allow quick switching between the Overview and Logistics pages.
- Zoom sliders on the trend and scatter charts allow detailed exploration.
- Tooltips show exact values on hover.
- A consistent blue theme keeps the report clean and easy to read.

## 8. Key Insights

The following insights are based on the unfiltered view of the dashboard and will change as filters are applied.

1. Late delivery is the main operational problem. About 55% of orders are delivered late, and only about 18% arrive on time.
2. Actual shipping is slower than planned. Average shipping time is 3.50 days against 2.93 scheduled days, a gap of about 0.57 days.
3. Delays occur across all shipping modes. First Class has the highest share of late deliveries, so the faster shipping options are not meeting expectations.
4. The late-delivery rate stays within a narrow range through the year, with peaks around March and August-September and a dip around July.
5. Sales are concentrated in a few regions. Western Europe and Central America lead by a clear margin, followed by South America, Northern Europe, Southern Europe and Oceania.
6. Europe and LATAM are the largest markets, followed by Pacific Asia, USCA and Africa.
7. Profit is steady from month to month. Total profit is 3.97M on 36.78M in sales, a margin of about 10.8%.
8. Most orders are complete, but a notable share is still in Pending Payment, Processing, Pending or On Hold. About 1K orders are canceled, and a small number are flagged as Suspected Fraud.
9. Sales grow with product price across cities, and a few high-value cities stand out in the scatter plot.

## 9. Recommendations

- Review shipping-mode commitments, especially First Class and Same Day, which are frequently late.
- Adjust scheduled days or improve carrier performance to close the gap between planned and actual shipping time.
- Investigate the months with higher late-delivery rates for capacity or carrier issues.
- Reduce the number of Pending Payment and On Hold orders through payment reminders and faster order review.
- Focus growth on the strongest regions while building up smaller ones such as Oceania and the Africa market.
- Apply stricter validation on orders flagged as Suspected Fraud.

## 10. Tools and Technologies

- Microsoft Power BI Desktop: report design and visualization
- Power Query: data cleaning and transformation
- DAX: measures and KPI calculations
- Data modelling: relationships between fact and dimension tables

## 11. Data Preparation and Workflow

1. Data collection: load order, customer, product and shipping data into Power BI.
2. Data cleaning: fix data types, remove duplicates and null values, and standardize text fields in Power Query.
3. Date preparation: create date columns such as Year and Month for time-based analysis.
4. Data modelling: connect the data tables through relationships.
5. Measures: create DAX measures for sales, profit, orders, customers, shipping days, late-delivery % and on-time %.
6. Visualization: build the Overview and Logistics pages with a consistent design.
7. Interactivity: add filters, navigation buttons, tooltips and cross-filtering.
8. Validation: check KPI values against the source data.

## 12. How to Use

1. Clone or download this repository.
2. Install Power BI Desktop, which is free from Microsoft.
3. Open the .pbix file in Power BI Desktop.
4. If asked, update the data source path under Home > Transform data > Data source settings.
5. Click Refresh to load the data.
6. Use the filters and the Overview / Logistics buttons to explore the dashboard.

## 13. Repository Structure

- SupplyChain_Dashboard.pbix : Power BI report file
- data/ : source dataset files
- README.md : project documentation

## 14. Future Enhancements

- Add a Customer and Product performance page.
- Add forecasting for sales and late-delivery trends.
- Add drill-through pages for city-level and order-level analysis.
- Add row-level security for regional managers.
- Publish to Power BI Service with scheduled data refresh.
- Add alerts when the late-delivery rate crosses a set threshold.
