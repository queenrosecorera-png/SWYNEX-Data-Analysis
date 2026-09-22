# Online Retail II - Data Cleaning

This is Task 1 of my Data Analyst Internship at SWYNEX Technologies. 
The goal was to pick a public dataset, find the data quality issues in it, and clean them up using Python, SQL, or Excel.

Dataset used: https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci

I cleaned the data using Python. Here's what I fixed:

A lot of rows had missing information in certain columns, so I either removed those rows or filled them in with a reasonable value, depending on what made sense. 
There were also repeated rows (the same entry showing up more than once), so I removed the extra copies. 
Some columns were stored in the wrong format, like dates that were saved as plain text instead of actual dates, so I converted those properly. 
Lastly, some entries were written inconsistently, like the same word spelled with different capitalization or extra spaces, so I made those consistent.
