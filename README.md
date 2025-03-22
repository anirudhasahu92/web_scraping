# Scraping Wikipedia Table using Pandas

## Problem Statement

This project aims to demonstrate how to scrape a table from a Wikipedia page using the Pandas library in Python. The specific table we'll extract is the list of largest companies by revenue.

## Steps

1. **Import Libraries:** We start by importing the necessary Pandas library for data manipulation.
2. **Specify URL:** The `url` variable stores the URL of the Wikipedia page containing the desired table.
3. **Read HTML Tables:** `pd.read_html(url)` reads all HTML tables from the specified URL and returns a list of DataFrames.
4. **Identify Target Table:** `len(tables)` helps determine the number of tables on the page. We then select the relevant table from the list based on its index (e.g., `tables[0]` for the first table).
5. **Inspect Table:** We examine the first few rows of the table using `req_table.head()`.
6. **Clean Column Names:** The table may have multi-level column headers. We can clean them using `req_table.columns = req_table.columns.droplevel(1)` to simplify column names.
7. **Explore Data:** `req_table.info()` provides information about the DataFrame's data types and missing values. `req_table.isnull().sum()` calculates the count of missing values in each column.
8. **Check Dimensions:** `req_table.shape` indicates the number of rows and columns in the table.

## Conclusion

This code successfully scrapes the "List of largest companies by revenue" table from Wikipedia using Pandas. It demonstrates basic data exploration techniques for cleaning and understanding the extracted data.

## Libraries Used

* **Pandas:** Used for data manipulation and analysis, including reading HTML tables.

## Acknowledgement

This project is inspired by various online resources and tutorials demonstrating web scraping with Pandas.

## Source of Data

The data is sourced from the Wikipedia page: [https://en.wikipedia.org/wiki/List_of_largest_companies_by_revenue](https://en.wikipedia.org/wiki/List_of_largest_companies_by_revenue)
