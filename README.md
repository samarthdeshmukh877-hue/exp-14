# Experiment 14: Data Binning and Data Formatting using Python

## Objective

The main objective of this experiment is to understand how raw data can be transformed into a more meaningful and structured form using **data binning** and **data formatting techniques** in Python.

This experiment focuses on:

* Converting continuous numerical data into categories
* Improving data readability and usability
* Preparing data for analysis and decision-making

---

## Introduction

In real-world datasets, raw data is often unorganized and difficult to interpret. To make data useful, we perform preprocessing steps such as:

### Data Binning

Data binning is the process of dividing continuous data into discrete intervals (bins). This helps in:

* Simplifying data analysis
* Reducing noise
* Making patterns easier to identify

### Data Formatting

Data formatting involves modifying data types and values to improve clarity and consistency.

---

## Dataset Description

### Product Dataset

This dataset includes:

* **Product Name** – Name of the product
* **Price** – Cost of the product
* **Units Sold** – Number of units sold
 This dataset helps in analyzing product performance.

---

### Order Dataset

This dataset contains:

* **Order ID** – Unique identifier for each order
* **Order Value** – Total value of the order
* **Delivery Time** – Time taken for delivery
* **Distance** – Distance covered for delivery

This dataset helps in analyzing delivery efficiency.

---

## Detailed Operations Performed

---

### 1. Data Binning (Categorization)

#### Price Binning

The price values are divided into categories:

* **Low** → 0 to 10,000
* **Medium** → 10,000 to 30,000
* **High** → 30,000 to 60,000

This helps in understanding which products fall into budget, mid-range, or premium categories.

---

#### Units Sold Binning

Units sold are grouped into:

* Low Sales
* Medium Sales
* High Sales

This helps identify product demand levels.

---

#### Order Value Binning

Orders are categorized into:

* Low Value Orders
* Medium Value Orders
* High Value Orders

Useful for analyzing customer spending patterns.

---

#### Delivery Time Binning

Delivery time is categorized into:

* **On Time**
* **Delayed**
* **Critical Delay**

Helps in evaluating logistics performance.

---

### 2. Data Formatting (Cleaning & Structuring)

#### Data Type Conversion

* Converted numerical columns like `Units_Sold` into float format
  Ensures compatibility with mathematical operations.

---

#### String Formatting

* Product names are converted to uppercase
  Improves consistency and avoids duplication issues.

---

#### Rounding Values

* Price values are rounded for better readability
  Makes reports cleaner and easier to interpret.

---

### 3. Data Sorting

* Data is sorted based on **Price** in:

  * Ascending order
  * Descending order

Helps quickly identify cheapest and most expensive products.

---

### 4. Extracting Unique Values

* Unique categories from binned data are extracted

Useful for understanding all possible classifications in the dataset.

---

## Sample Code Explanation

```python
df['Price_Category'] = pd.cut(
    df['Price'], 
    bins=[0,10000,30000,60000], 
    labels=['Low','Medium','High']
)
```

### Explanation:

* `pd.cut()` is used to divide continuous data into bins
* `bins` defines the range intervals
* `labels` assigns names to each category

This converts raw price values into meaningful categories.

---

## Results & Observations

* Data binning made it easier to identify trends in pricing and sales
* Formatting improved data clarity and usability
* Categorized data helped in better decision-making

---

## Conclusion

This experiment successfully demonstrates how:

* Raw data can be transformed into structured information
* Data binning simplifies analysis by grouping values
* Data formatting improves consistency and readability

These techniques are essential in **data preprocessing**, which is a critical step in:

* Data Science
* Machine Learning
* Business Analytics

---

## Real-World Applications

* Sales Analysis
* Customer Segmentation
* E-commerce Data Processing
* Logistics Optimization
