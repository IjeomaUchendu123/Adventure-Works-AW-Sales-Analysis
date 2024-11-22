# ADVENTURE-WORKS-AW-SALES-ANALYSIS

## PROJECT OVERVIEW 

A sales Analysis of Adventure works(AW) company taking into consideration sales of products, product categories and sub-categories, products returned, product costs, discounts and customer data gining insights into sales revenue and profit, best performing products, best performing product category and sub-category, best performing regions, return rate and KPI achievables.

### DATA SOURCES

The Primary dataset used for this analysis is the "AW data set.csv" containing data of four different years which were appended together

### TOOLS
 - POWERBI - Data Cleaning [Download here](https://microsoft.com)
 - POWERBI - Data Analysis
 - PWER BI- Visualization

### DATA CLEANING
In the data cleaning phase, the following tasks were performed;
1. Data Loading and Inspection
2. thth
3. hththt
4. ththth

### EXPLORATORY DATA ANALYSIS

The EDA involved exploring the sales data to answer questions such as ;
 - What year had the highest sales revenue ?
 - What are the total orders, cumulative sales revenue and cumulative profit ?
 - What is the average return rate of products ?
 - What Product had the highest return rate ?
 - Were the KPI's set for total returns, total revenue and total orders met ?
 - What product category and sub-category has the highest orders ?
 - What product has the highest orders?
 - What product has the highest profit ?
 - What country has the highest orders, revenue and profit ?

### DATA ANALYSIS


```PowerBI
90 Days Rolling Revenue = CALCULATE([Total Revenue],DATESINPERIOD('AW Calendar'[Date],MAX('AW Calendar'[Date]),-90,DAY))
```
```PowerBI
PROFIT = 'AW sales'[Revenue] - RELATED('AW Product'[ProductCost])*'AW sales'[OrderQuantity]
```

```PowerBI
 SWITCH('AW Calendar'[Day Name], "Monday", "1", "Tuesday", "2", "Wednesday", "3", "Thursday", "4", "Friday", "5", "Saturday", "6", "Sunday", "7")
```
```PowerBI
IF(OR('AW Calendar'[DayNumber]="6", 'AW Calendar'[DayNumber]="7"), "Weekend", "WeekDays")
```
```PowerBI
 UPPER(LEFT('AW Calendar'[Month Name],3))
```

### FINDINGS
The results of the analysis are summarized as follows;
1. Year 2022 has the highest sales revenue while year 2020 had the least.
2. Cumulative Sales revenue was $24.91M, Cumulative profit was 10.46M and total orders was 25200
3. The products had an average return rate of 2.2%
4. HL- Mountain Tire is the product with the highest return rate
5. The target KPI set for total returns using the previous month return as a bench mark was met. The target was set at 169 returns but only 166 products were returned.
6. The target KPI set for total revenue using the previous month revenue as bench mark was surpased by 3.31%. A target of $1.77M was set but $1.83M was realized.
7. The target KPI set for the total number of orders using the previous month as target was not met. A target of 2165 orders was setfor the new month but only 2146 orders were realized.
8. "Accessories" had the highest orders by 'Product Category' and 'Tires and Tubes' had the highest orders by product sub-catgory.
9. Product "Water Bottle - 30oz" had the highest orders and Product "Mountain-200 Black 46" generated the most profit.
10. United States is the country with the highest Orders, Revenue and Profit.
