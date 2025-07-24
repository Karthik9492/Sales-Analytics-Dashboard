# Sales Analytics Dashboard - Tableau
This project showcases a **Sales Analytics Dashboard** built in **Tableau**, powered by insights derived from SQL-based analysis on a structured relational database. The dashboard highlights key performance indicators (KPIs), product performance, customer behavior, and geographic trends based on multi-level SQL queries.
## 🚀 Project Overview
The primary goal of this project is to analyze and visualize business data across **sales, customers, products, and stores** to drive strategic insights.
The underlying data was initially processed and explored using **MySQL**, and then visualized through **Tableau Public**.

## Currency Conversion in Tableau
All sales and profit values are normalized to USD using dynamic exchange rates from the ExchangeRates table. A calculated field was used:
IF ISNULL([Exchange]) THEN
    NULL
ELSEIF [Currency Code] = 'USD' THEN
    [Quantity] * [Unit Price USD]
ELSE
    ([Quantity] * [Unit Price USD]) * [Exchange]
END
## ⏱ Delivery Time in Days
To handle missing delivery dates and calculate delivery duration:
IF ISNULL([Delivery Date]) THEN
    NULL
ELSE
    DATEDIFF('day', [Order Date], [Delivery Date])
END
used this field to compute: Average delivery time KPI
# Dataset
This dashboard is powered by a dataset originally used in my SQL Sales Analysis Project — where I explored, cleaned, and analyzed transactional sales data using MySQL.

📂 GitHub Dataset Link: 👉 https://github.com/Karthik9492/Sales-Analysis-with-Database-and-MYSQL/tree/main/Global%2BElectronics%2BRetailer 

## 🖼️ Dashboard Preview
Tableau Public: https://public.tableau.com/views/Dashboard_17519996788120/SalesAnalyticsDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

![Sales Analytics Dashboard ](https://github.com/user-attachments/assets/aacda868-aa17-49d4-9762-1637143ef203)

