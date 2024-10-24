
- [1. Project: Cleaning Bank Marketing Campaign Data](#1-project-cleaning-bank-marketing-campaign-data)
  - [1.1. Overview](#11-overview)
  - [1.2. Actions Performed](#12-actions-performed)
  - [1.3. Python Concepts Used](#13-python-concepts-used)


# 1. Project: Cleaning Bank Marketing Campaign Data

## 1.1. Overview

This notebook performs data loading, cleaning, and analysis on a bank marketing dataset. It leverages Python's `pandas` library to manipulate and analyze data efficiently.

## 1.2. Actions Performed


1. **Exploratory Data Analysis**:

   - Printed the value counts for specific categorical columns (`credit_default`, `mortgage`, `previous_outcome`, `campaign_outcome`) to understand the distribution of values within these columns.
2. **Data Cleaning**:

   - Replaced periods (`.`) in the `job` and `education` columns with underscores (`_`) for standardization.
   - Replaced instances of `'unknown'` in the `education` column with `NaN` to handle missing data.
3. **Boolean Conversion**:

   - Created a function (later simplified) to convert specific columns (`credit_default`, `mortgage`, `campaign_outcome`) to boolean values where `'yes'` became `True` and all other values became `False`.
   - Converted the `previous_outcome` column to a boolean value where `'success'` became `True`.
4. **Date Handling**:

   - Constructed a `last_contact_date` column from separate `day` and `month` columns, combining them into a datetime format for further analysis.
5. **Data Subsetting**:

   - Created three subsets of the original DataFrame (`client`, `campaign`, and `economics`), each containing relevant columns for further analysis.

## 1.3. Python Concepts Used

1. **Pandas Library**:

   - Utilized `pandas` for data manipulation and analysis, taking advantage of its powerful DataFrame structure.
2. **DataFrame Operations**:

   - Performed operations on DataFrames, such as filtering columns, modifying values, and converting data types.
3. **String Methods**:

   - Used string manipulation methods (e.g., `.str.replace()`) to clean and standardize data.
4. **Boolean Logic**:

   - Used boolean comparisons (`eq()`) to convert categorical values to boolean types effectively.
5. **Datetime Handling**:

   - Used `pd.to_datetime()` to handle and format dates, allowing for time-series analysis and manipulation.
6. **Iteration and List Comprehension**:

   - Employed loops (e.g., `for` loops) to iterate through columns for value counts and conversion.
7. **Data Subsetting**:

   - Created new DataFrames from the original DataFrame by selecting specific columns for focused analysis.