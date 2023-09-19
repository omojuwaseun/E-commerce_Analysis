# E-commerce_Sales_Analysis
As a Data Analyst, I embarked on an engaging journey with a prominent US-based company that entrusted me with a pivotal task: crafting a comprehensive Sales Dashboard. This interactive dashboard was created to shed light on the complex world of Year-to-Date (YTD) sales statistics. I used my data visualization and analytical talents to turn the raw data into useful insights in this difficult but fun project. This initiative not only fueled my enthusiasm for data analysis, but it also highlighted the critical need to make well-informed decisions in the competitive corporate environment of today.

### Data Importation: 
Two datasets were provided (e-commerce and US state long lat codes). The data was then imported into an already-created database in SQL, where I changed some of the datatypes to the accurate ones. After which, I connected to Power BI and loaded it. Then I proceeded to model the data and create a connection between the two tables with the customer state column and name column from the tables.

The e-commerce table has several columns, like the customer id, customer first name, customer last name, category name, product name, customer segment, customer city, customer state, customer country, customer region, delivery status, order date, order id, ship date, shipping type, days for shipment scheduled, days for shipment real, order item discount, sales per order, order quantity, and profit per order. While the US state long lat codes have the state, latitude, longitude, and name columns.

### Problem Statement

Create different KPI banners showing year-to-date (ytd) sales, profit, quantity sold, and profit margin. Also, use the YTD sales to know the best and worst regions and shipping types to get the best shipping type percentage.

### Measures Created:

Year-to-date (YTD) sales, profit, quantity sold, and profit margin

YTD Sales = TOTALYTD(SUM('ecommerce_data (1)'[sales_per_order]),Calender[Date])
Previous year-to-date (PYTD) sales, profit, quantity sold, and profit margin

PYTD Sales = CALCULATE(SUM('ecommerce_data (1) [sales_per_order]), DATESYTD(SAMEPERIODLASTYEAR(Calender[Date]))))
Year over year (YOY) sales, profit, quantity sold, and profit margin

YoY Sales = [YTD Sales] - [PYTD Sales] / [PYTD Sales]
Sales, profit, quantity sold, and profit margin icon and color

Profit color = IF([YoY Profit]>0, "Green","Red")

Profit Icon = var positive_icon = UNICHAR (9650)
             var negative_icon = UNICHAR (9660)
                 var result = IF([YoY Profit]>0,positive_icon,negative_icon)
                 return result 

I started the next essential phase of the data analysis process after successfully developing the desired Key Performance Indicators (KPIs): turning those insightful discoveries into understandable graphics. I created various educational charts to accomplish this. These visual representations not only helped stakeholders better understand the meaning of the KPIs, but they also made complex data easier to understand. I successfully converted data into useful insights with these charts, enabling decision-makers to lead the business in the proper direction and make wise decisions for a better future.

### Insights:

Year-to-date sales have reached an impressive $11.53 million, demonstrating a consistent upward trend. In the same period, year-to-date profit stands at $1.34 million, with a healthy profit margin of 11.58%. However, the total quantity sold, at 107.2K units, shows a declining trend.

In terms of shipping types, standard class led the sales chart at 60.3%, followed by first class at 15.1% and second class at 19.2%.

Regarding regional sales, the West region took the top spot with 32.2%, closely followed by the East at 28.4%. The South region contributed 16.2%, while the Central region accounted for 23.2%.

Among the products, Stable Envelope achieved the highest sales volume, totaling 57,000 units, making it the top-selling product. In contrast, Rediform S.O.S. phone message books recorded the lowest sales, with only 0.18k units sold.

### Recommendations:

Improve Inventory Management: Improving inventory management is essential given the overall trend of diminishing sales volume. Cost-efficiency can be increased by reducing excess stock and matching inventory levels with actual demand.

Regional Expansion: Take advantage of the profitable sales trends in the West and East. Look for ways to strengthen and increase the company’s presence in these areas. This can entail launching niche marketing initiatives or creating regional alliances.

Analyze the South Region: Given the South region’s relatively lesser contribution, perform a thorough analysis to comprehend the elements influencing sales there. To better suit this market, adjust strategy accordingly, such as by customizing products or marketing initiatives.

Investigate sustainability measures given that consumers are becoming more aware of environmentally friendly goods and activities. This might expand the company’s market reach and improve its standing.

Continue investing in market research to find new trends and consumer preferences. By doing so, you’ll be able to stay one step ahead of the competition and adjust to shifting market dynamics.

![ecommerce dashboard](https://github.com/omojuwaseun/E-commerce_Analysis/assets/119857809/db80b2ac-2277-4b5e-b93d-bdf2a150ae93)

