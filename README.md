# ADVENTURE-WORKS-AW-SALES-ANALYSIS

## PROJECT OVERVIEW 

A Sales Analysis of Adventure works(AW) company taking into consideration sales of products, product categories and sub-categories, products returned, product costs, discounts and customer data seeking to gain insights into product sales, revenue and profit, best performing products, best performing product category and sub-category, best performing regions, return rate and KPI achievables(Dataset File and Visualization attached).

### DATA SOURCES

The Primary dataset used for this analysis is the "Adventure Works datasets" containing data across different units such as Customer information, poduct categories, Product subcategories, Returns data etc

### TOOLS
 - POWERBI - Data Cleaning [Download here](https://microsoft.com)
 - POWERBI - Data Analysis
 - PWER BI- Visualization

### DATA PREPARATION
In the data preparation phase, the following tasks were performed;
1. Data Loading and Inspection.
2. Data Modelling to create relationships between tables.
3. Creation of New Measures to suit the purpose of our analysis.
4. Creation of calculated columns to further suit the purpose of our analysis.

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

### RECOMMENDATIONS
Based on the findings of the analysis, the following are recommended:
1. Identify the Key factors that contributed to the high sales in 2022 e.g Marketing Campaigns and try to replicate and improve on such factors in the coming years.
2. Implement measures to monitor and further reduce the overall return rate such as enhancing product description, improving packaging etc. in order to reduce the return rate.
3. Identify the reasons behind the high return rat of HL-Mountain Tire and take corrective actions such as modifying the product design etc.
4. Identify factors that contributed to the 3.31% surplus in the target set for revenue and use this as a benchmark for replicating such success or even better in the coming years.
5. Identify reasons for the shortfall in the target set for orders and develop strategies for the improvement of order fulfillment e.g enhancing supply chain efficiency.
6. Expand product offerings for products within the Accessories Category and Tires and Tubes sub-category and create targeted marketing campaigns towards them.
7. Identify the factors contributing to the high orders and profit generated by the Water Bottle- 30oz and the Mountain-200 Black 46 and use the knowledge to inform product development and Marketing strategies.
8. Expand Marketing efforts and optimize logistics to further grow sales , revenue and profit in the US.
9.  Develop targeted strategies and explore opportunities to improve sales, revenue and profit performance in other countries.
