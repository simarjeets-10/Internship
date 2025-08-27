Housing Data Analysis

This Python script performs data analysis on a housing dataset to extract insights related to average prices, dates, and crime rates across areas in England.

Features:

Converts the Date column to datetime format.

Adds new columns for year and month.

Removes the temporary year and month columns after use.

Finds and counts records where the number of crimes is zero.

Calculates the minimum and maximum average prices per year.

Finds the minimum and maximum number of crimes recorded per area.

Displays the total count of records for each area where the average price is less than £100,000.

Requirements:

Python

pandas

numpy

matplotlib

seaborn

How to Run:

Make sure the Housing_data.csv file is downloaded on your system.

Update the file path in the script to match the location of the dataset. For example: df = pd.read_csv("C:/Users/YourName/Downloads/Housing_data.csv")

Run the script using Python: python housingdata.py

Notes: This script uses datetime conversion, data grouping, filtering, and aggregation to analyze trends in housing prices and crime rates. It is designed to provide real-world insights based on simple data operations
