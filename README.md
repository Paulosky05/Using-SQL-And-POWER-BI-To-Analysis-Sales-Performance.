# Toman bike_sales Analysis

### Project Overview
This data analysis projects aims to provide insightd into the sales performance of a bike sales company between 2021-2022. By analysing various aspects of the sales data, we seek to identify trends, make data driven recommendations and gain a deeper understanding of the company's performance.This project involves setting up a database ,joining the tables in microsoft sql management sudio and  connecting to powerBi to building a dashoard.

### Obectives
1. Create a database
2. Develop Sql Queries
3. Connect Power BI To DB
4. Build a Dashboard in Power BI
5. Answer The Analysis Question
### Data sources
Toman-sales-Data: The primary dataset used for this analysis is the '(bike-share-yr-0,bike-share-yr1,cost-table)', containing detailed information about the company cost of goods, season and overall sales performance of the company.

### Tools
- SQL-Server- used for creating data base and perform join
   - [Download-here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- PowerBi- Creating dashboards
   - [Download-here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

  ### Data Cleaning/Preparation
  In the initial data prepation phase, we perform the following tasks:
  1. Data loading and inspection,
  2. checking for missing values.
  3. perform joins using union clause

 ### Exploratory Data Analysis(EDA)
 - hourly Revenue Analysis
 - Profit and Revenue trends
 - Seasonal Revenues
 - Rider Demographics

   ### Data analysis

```sql
CREATE DATABASE Bike-sales;
USE Bike-sales;
```
```
with CTE as (select *
from bike_share_yr_0
union
select *
from bike_share_yr_1)
select 
dteday,
season,
a.yr,
weekday,
hr,
rider_type,
riders,
price,
COGS,
riders*price as revenue,
riders*price - COGS*riders as profit
from cte  a
left join cost_table  b
on a.yr = b.yr
```

### Results?Findings

The anaalsis results are summarised as follows:
1. The company's sales have been steadily increasing over the pastyear,with a noticeable peak incre increase from the month of may to october.
2. The company made a 0.45% increase in sales in 2022 compared to 2021
3. customer registered should be targeted for marketting.

### Recommendation

Conservative Increase:Considering the substancial increase in last year, a move conservative increase might be prudent to avoid hitting a price ceiling where demand starts to drop.An increase in the range of 5-10% could test the market's reponse without risking a significant loss of customers.
Price Setting:
- If the price in 2022 was $4.99, a 5% increase would make the new price about $5.24
- A 10% increase would set the price at approximately 5.49.

 #### Recommended Strategy
  Market Analysis: Conduct further market research to understand
     
     
     

     
