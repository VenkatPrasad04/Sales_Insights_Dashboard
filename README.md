
# Sales Insights Data Analysis Project

This is the data analysis project using Microsoft Power BI.

## Steps involved in this project are:
1. Load the Data and Organise it.
2. Clean the Data i.e removing duplicates,unwanted data etc.
3. Reconstruct Data i.e all the data is in the same format or other format.
4. Construct the star schema.
5. Construct Dashboard using DAX expressions in Power BI.


### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

![image](https://github.com/VenkatPrasad04/Data_Analysis_Sales_Insights/assets/106549950/566a3e5a-d076-4ed0-b0a0-3d5406dc5c88)

Performance Dashboard

![image](https://github.com/VenkatPrasad04/Data_Analysis_Sales_Insights/assets/106549950/15714423-56f3-4553-b793-091deb848e20)

Profit Analysis

![image](https://github.com/VenkatPrasad04/Data_Analysis_Sales_Insights/assets/106549950/97988d35-d2e1-49be-bd42-262edb9d7936)

Key Insights






