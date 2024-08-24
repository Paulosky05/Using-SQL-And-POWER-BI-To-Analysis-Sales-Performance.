## Bike-Sales Analysis

### Project Overview
This data analysis projects aims to provide insightd into the sales performance of a bike sales company between 2021-2022. By analysing various aspects of the sales data, we seek to identify trends, make data driven recommendations and gain a deeper understanding of the company's performance.This project involves setting up a database ,joining the tables in microsoft sql management sudio and  connecting to powerBi to building a dashoard.

![Screenshot 2024-08-24 063659](https://github.com/user-attachments/assets/6d29559a-33ac-41d2-820c-ffc23ef373e2)


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

   ### Data Base Creation

```sql
CREATE DATABASE Bike-sales;
USE Bike-sales;
```
### Data Analysis
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
- Market Analysis: Conduct further market research to understand customer satisfaction, potential
competitive changes, and the overall economic environment. This can guide whether leaning towards the
lower or higher end of the suggested increase.
- Segmented Pricing Strategy: Consider different pricing for casual versus registered users, as they may
have different price sensitivities.
- Monitor and Adjust: Implement the new prices but be ready to adjust based on immediate customer
feedback and sales data, Monitoring closely will allow you to fine-tune your pricing strategy without
committing fully to a price that might turn out to be too high.

### How to Use 
1. clone the repository: Clone the project repository from github
2. Set up the database: Run the Sql scripts provided in the database creation to ctrate and populate the database
3. Run the queries: Use the sql queries provided in the analysis section toperform your analysis
4. Connect to a powerbi or any visualisation tool to build a dashboards
5. Modifty and Explore

   ### Author PAUL THE ANALYST
   This project is part of my portfolio,showcasing my SQL and powerbi skills essential for data analyst roles.. if you have any feedback,questions or would like to collaborate feel free to get in touch!
   
   ** REACH ME ON LINKEDIN** [click-here](https://www.linkedin.com/in/paul-muoghalu-2b8a3b272?utm)
   😄
   🖥️

     
     
     

     
