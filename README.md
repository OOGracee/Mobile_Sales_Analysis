# Mobile_Sales_Analysis
## Overview:
__This is a sales report for Mobile Sales products__ 

---
## Content
Project Overview| Data Source| Tools Used| Table Outlay| Query Languages (SQL)| Visualization

---

## Project Overview:
> > This project analyze all the sales of Mobile Sales products and shows various attributes such as Brands,Customer Gender,
Payment Method Using Pivot table. This analysis helps to understand the ky factors of sales in dataset.

---

## Data Source:
www.kaggle.com/dataset

---

## Tools Used:
+ Pivot table / charts
+ Power BI 
+ SQL
  
---

## Table Outlay:
First Three Columns

|TransactionID|	Date|	MobileModel|	Brand|	Pric|	UnitsSold|	TotalRevenue|	CustomerAge|	CustomerGender|	Location|	PaymentMethod|
|------|------|------|------|------|-----|------|------|------|------|------|

|79397f68-61ed-4ea8-bcb2-f918d4e6c05b|	1/6/2024|	direction|	Green Inc|	1196.95|	85|	28002.8|	32|	Female|	Port Erik|	Online|
|4f87d114-f522-4ead-93e3-f336402df6aa|	4/5/2024|	right|	Thomas-Thompson|	1010.34|	64|	2378.82|	55|	Female|	East Linda|	Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1|	2/13/2024|	summer|	Sanchez-Williams|	400.8|	95|	31322.56|	57|	Male|	East Angelicastad|	Online|

## Query Languages: (SQL)
The Query Language to retrieve record is displayed below

```SQL
SELECT * FROM [dbo].[mobile_sales]

---1.CATEGORIZE THE DATA INOT GOLD,SILVER AND DIAMOND
SELECT *,
CASE
WHEN PRICE < 500 THEN 'silver'
WHEN PRICE BETWEEN 500 AND 999 THEN 'gold'
ELSE 'diamond'
END AS category
FROM mobile_sales;

---2.RETRIEVE ALL FEMALE CUSTOMERS THAT BOUGHT GOODS ABOVE 900---
SELECT * FROM mobile_sales
WHERE customergender = 'female'
AND price >900;

---3.RETRIEVE THE SALES BY PAYMENT METHOD ARRANGING FROM LARGEST TO SMALLEST AMOUNT---
SELECT * FROM mobile_sales
ORDER BY paymentMethod;

---4.RETRIEVE THE MOST EXPENSIVE BRAND---
SELECT MAX (price) AS price, Brand FROM mobile_sales
GROUP BY Brand
ORDER BY price DESC;

---5.HOW MANY BRAND SRE THERE---
SELECT COUNT (DISTINCT Brand) AS 'Distint Brand' FROM mobile_sales;
```
## Visualization:
__Pivot Tables__

## Charts






















