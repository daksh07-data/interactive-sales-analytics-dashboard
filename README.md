# interactive-sales-analytics-dashboard
Interactive Power BI dashboard built using the Superstore dataset to analyze sales performance, profit trends, regional insights, and top-selling products. The project includes KPI cards, dynamic slicers, maps, trend analysis, and interactive visualizations for business decision-making.

── SQL Queries/


SELECT COUNT(*) AS total_rows
FROM sales_project;
SELECT
    `Order ID`,
    `Order Date`,
    Category,
    Sales,
    Profit,
    Region
FROM sales_project


LIMIT 10;
SELECT
    ROUND(SUM(Sales),2) AS total_sales
FROM sales_project;
SELECT
    ROUND(SUM(Profit),2) AS total_profit


FROM sales_project;
SELECT
    Category,
    ROUND(SUM(Sales),2) AS total_sales
FROM sales_project
GROUP BY Category
ORDER BY total_sales DESC;

SELECT
    Region,
    ROUND(SUM(Profit),2) AS total_profit
FROM sales_project
GROUP BY Region
ORDER BY total_profit DESC;


SELECT
    `Product Name`,
    ROUND(SUM(Sales),2) AS total_sales
FROM sales_project
GROUP BY `Product Name`
ORDER BY total_sales DESC
LIMIT 10;

── Dashboard Screenshots/
<img width="1482" height="802" alt="Screenshot 2026-05-15 122515" src="https://github.com/user-attachments/assets/76e2d206-8c33-4e5e-8c61-b0414a657d11" />




