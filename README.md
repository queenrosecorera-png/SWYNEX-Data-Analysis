# Online Retail II - Data Cleaning

#TASK 1 - DATA CLEANING

This is Task 1 of my Data Analyst Internship at SWYNEX Technologies. 
The goal was to pick a public dataset, find the data quality issues in it, and clean them up using Python, SQL, or Excel.

Dataset used: https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci

I cleaned the data using Google Colab(Python). Here's what I fixed:

A lot of rows had missing information in certain columns, so I either removed those rows or filled them in with a reasonable value, depending on what made sense. 
There were also repeated rows (the same entry showing up more than once), so I removed the extra copies. 
Some columns were stored in the wrong format, like dates that were saved as plain text instead of actual dates, so I converted those properly. 
Lastly, some entries were written inconsistently, like the same word spelled with different capitalization or extra spaces, so I made those consistent.

#TASK 2 - EXPLORATORY DATA ANALYSIS

What I did:
After cleaning the Online Retail II dataset in Task 1, I explored it to find useful patterns in sales, products, customers and countries.
I used Python (pandas and matplotlib) for all the analysis and charts.

Dataset used:
online_retail_cleaned.csv (the file I cleaned in Task 1), around 1,027,022 rows.
I cant upload it because the dataset is large.

How I approached it:
I first added a Revenue column (Quantity x Price), since it wasn't already in the data.
Then I grouped the data in different ways - by month, by product, by country, by customer and by cancellation status - to answer specific business questions.

## Insights

1. Monthly revenue Trend:
Revenue goes up every November (1.42M in 2010, 1.46M in 2011), most likely because of Christmas shopping.
It's lowest in February both years.
December 2011 looks very low in the chart, but that's just because the data stops on 9 December, not because sales actually dropped.

2. Best-selling product:
WORLD WAR 2 GLIDERS ASSTD DESIGNS sold the most units (104,435), but it's not the top earner.
REGENCY CAKESTAND 3 TIER made the most revenue (314,045.02), even with far fewer units sold, since it costs more per item.
WHITE HANGING HEART T-LIGHT HOLDER did well on both.

3. Most revenue comes from the UK:
84.8% of total revenue comes from the United Kingdom.
The next biggest, EIRE, is only 3.2%.
This shows the business barely sells outside the UK.

4. A small group of customers brings in most of the money:
Looking only at customers with a known ID, the top 10% of them make up 55% of that revenue.
This makes sense since the company description says many customers are wholesalers.
I also noticed 78% of all rows have no Customer ID at all, so a lot of revenue can't actually be linked to any customer.

5. Cancellations are a real loss:
About 7.75% of revenue (around 1.46 million) comes from cancelled orders.
That's a decent chunk of money that never actually stayed as real sales.
