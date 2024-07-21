# SMart-Store-Sales-PowerBI-Dashboard-

### Project Objective
	To successfully contribute to SMart Store's business by utilizing the past 2 years' data and applying
	data analysis techniques, specifically focusing on time series analysis, to provide valuable
	insights and accurate sales forecasting.

### Project Overview
	1. Used 2 years' data to build a dashboard and analyze historical data
 	2. KPIs - Orders, Sales, Profit, Avg Ship Days, Return orders percentage
	3. Slicer for filtering data based on West, East, North, and South zones
	4. Compare sales and profit data YoY months
	5. Donut chart to compare Sales against different parameters
	6. Stacked Horizontal Bar Charts to compare Sales by categories
	7. Map to visualize zones better

### Steps
	1. Dashboard Creation
	Identify the KPIs, design an intuitive and visually appealing dashboard, add interactive visualizations
	and filtering capabilities to allow users to explore the data at various levels of granularity.
	2. Data Analysis
	Provide valuable insights to business entities regarding the effectiveness of their sales strategies 
	through visualization and charts.
	 3. Sales Forecasting with 90% Confidence Interval
	Leverage historical data and apply time series analysis to generate sales forecast for the next 15 days
	 4. Actionable insights and recommendations
	The end goal is to share valuable insights and actionable information that can drive strategic decision-making
	and support the supermarket's growth, efficiency, and customer satisfaction goals.

### Data Cleaning
	1. Check the datatypes of each column
	2. Check NULL values by VIEW-> Column Quality
	3. May remove unwanted columns
DAX Queries used
	To calculate Average Ship days <br/> 
	--> Measure_returns = <br/> 
	DIVIDE( <br/> 
    	COUNTROWS(FILTER('Sheet1', 'Sheet1'[Returns] = 1)), <br/> 
    	COUNTROWS(ALLSELECTED('Sheet1')) <br/> 
	) <br/> <br/> 
 	To create a new sheet <br/> 
  	SalesForecast = SUMMARIZE('Sheet1','Sheet1'[Order Date], "Total_Sales",SUM(Sheet1[Sales])) <br/> 

### Insights
	1. The most popular payment mode is COD
	2. Maximum sales came from the West Region generating $522.4K in sales. California generated the highest sales in this region.
	3. The Most Popular Ship Mode was Standard Class
	4. Out of every 100 orders 4.86 were returned
	5. Office supplies formed the most popular category by sales
	6. Average shipping time over 2 years is 4 days
	7. Significant spike in Sales and Profit in September and December months.
