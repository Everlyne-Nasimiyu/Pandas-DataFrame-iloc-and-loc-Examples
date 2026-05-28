# Pandas DataFrame `iloc` and `loc` Examples

## Overview
This repository contains a Google Colaboratory notebook demonstrating fundamental data selection techniques in the pandas library using `iloc` and `loc` methods. It's designed to provide clear examples of how to effectively retrieve subsets of data from a pandas DataFrame based on integer-location indexing and label-based indexing.

## Contents
The notebook `pandas_iloc_loc_examples.ipynb` includes:
-   Creation of a sample pandas DataFrame (`employee_df`).
-   Examples of using `iloc` to select rows and columns by integer position.
-   Examples of using `loc` to select rows and columns by labels and boolean conditions.

## Getting Started

### Prerequisites
-   Python 3.x
-   pandas library

### Running the Notebook

#### Google Colaboratory
1.  Open the `pandas_iloc_loc_examples.ipynb` file in Google Colab.
2.  Run all cells sequentially to see the DataFrame creation and data selection examples in action.

#### Local Environment (Jupyter Notebook/Lab)
1.  Ensure you have pandas installed: `pip install pandas`
2.  Launch Jupyter Notebook or JupyterLab.
3.  Navigate to the directory where you saved the notebook and open `pandas_iloc_loc_examples.ipynb`.
4.  Run all cells to execute the code.

## Examples Covered

### 1. Creating the DataFrame
```python
import pandas as pd

data = {'Name': ['John', 'Mary', 'Bob', 'Sarah', 'Tom', 'Lisa'],
        'Department': ['IT', 'Marketing', 'Sales', 'IT', 'Finance', 'Marketing'],
        'Age': [30, 40, 25, 35, 45, 28],
        'Gender': ['Male', 'Female', 'Male', 'Female', 'Male', 'Female'],
        'Salary': [50000, 60000, 45000, 55000, 70000, 55000],
        'Experience': [3, 7, 2, 5, 10, 4]}

employee_df = pd.DataFrame(data)
print(employee_df)
```

### 2. Selecting Rows with `iloc`
-   Selecting the first 3 rows:
    ```python
    print(employee_df.iloc[:3])
    ```

### 3. Selecting Rows with `loc`
-   Selecting all rows where `Department` is 'Marketing':
    ```python
    print(employee_df.loc[employee_df['Department'] == 'Marketing'])
    ```

### 4. Selecting Columns with `iloc`
-   Selecting `Age` and `Gender` columns for the first 4 rows:
    ```python
    print(employee_df.iloc[:4][['Age', 'Gender']])
    ```

### 5. Selecting Columns with `loc`
-   Selecting `Salary` and `Experience` columns for all rows where `Gender` is 'Male':
    ```python
    print(employee_df.loc[employee_df['Gender'] == 'Male'][['Salary', 'Experience']])
    ```

## License
This project is open-source and available under the [MIT License](LICENSE.md).
