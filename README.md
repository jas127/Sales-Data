# Data Cleaning and Preprocessing of Sample Sales Data

This document outlines the steps taken to clean and preprocess the dataset `sales_data_sample.csv` using Python and Pandas.

## Dataset Overview

- **Shape**: The dataset consists of a certain number of rows and columns, providing a comprehensive view of sales data.
- **Sample Data**: The first few rows of the dataset give a glimpse into the structure and types of data included.
- **Statistics**: Basic statistics such as mean, median, and standard deviation are calculated for numerical columns to understand the distribution and range of values.
- **Data Types**: The dataset includes various data types such as integers, floats, and strings, which are crucial for data processing and analysis.


## Steps

1. **Load the Dataset**: 
   - The CSV file is loaded using Pandas with a fallback encoding of `ISO-8859-1`.

2. **Convert Dates**:
   - The `ORDERDATE` column is converted to datetime format, with errors coerced to handle invalid dates.

3. **Remove Duplicates**:
   - Duplicate rows are removed from the dataset.

4. **Strip Whitespace**:
   - Whitespace is stripped from all string columns to ensure consistency.

5. **Standardize Column Names**:
   - Column names are standardized by stripping whitespace, converting to lowercase, and replacing spaces with underscores.

6. **Check and Handle Missing Values**:
   - Missing values are checked and printed.
   - The `addressline2` column is dropped.
   - Missing values in `state` and `territory` are filled with their mode (most common value).
   - Missing values in `postalcode` are filled using forward fill.

7. **Encode Categorical Variables**:
   - The categorical variable `dealsize` is encoded using `LabelEncoder`.

8. **Remove Outliers**:
   - Outliers in the `sales` column are removed using the Interquartile Range (IQR) method.

9. **Summary**:
   - The original uncleaned dataset information is printed.
   - The cleaned dataset information is printed for final review.

These steps ensure that the dataset is clean, consistent, and ready for further analysis or modeling.
