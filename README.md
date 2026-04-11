# Data Binning and Formatting using Python

## Project Overview
This project demonstrates essential data preprocessing techniques—**Data Binning** and **Data Formatting**—using the Python `pandas` and `numpy` libraries. These techniques are crucial for transforming raw data into a structured format suitable for statistical analysis and machine learning.

## Key Concepts Covered

### 1. Data Binning (Discretization)
Binning is used to group continuous numerical values into discrete "bins" or categories. 
- **Price Categorization**: Segmenting product prices into 'Low', 'Medium', and 'High' ranges.
- **Sales Performance**: Categorizing units sold into 'Low Sales', 'Medium Sales', and 'High Sales'.
- **Logistics Analysis**: Grouping delivery times into 'On Time', 'Delayed', and 'Critical' categories to monitor efficiency.

### 2. Data Formatting
Formatting ensures that data types and strings are consistent across the dataset.
- **Type Conversion**: Converting integer columns to float for precise mathematical operations.
- **String Manipulation**: Normalizing text data by converting product names to uppercase.
- **Numerical Precision**: Rounding numerical values to specific decimal places for cleaner reporting.

### 3. Data Manipulation
- **Sorting**: Organizing data based on price in both ascending and descending order to identify extremes.
- **Unique Value Inspection**: Identifying distinct categories created during the binning process.

## Technical Procedure
1. **Import Libraries**: Load `pandas` and `numpy`.
2. **DataFrame Creation**: Initialize datasets containing product info (Price, Units) and order info (Value, Delivery Time, Distance).
3. **Applying pd.cut()**: Define custom bin edges and labels to transform continuous variables into categorical factors.
4. **Data Cleaning**: Standardize text and numeric formats using `.str.upper()`, `.astype()`, and `.round()`.
