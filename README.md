# Healthcare Data Analysis

## Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a healthcare dataset using Python and Pandas. The analysis focuses on understanding patient information, identifying missing values, converting date columns, generating descriptive statistics, and exploring billing and admission-related data.

The project demonstrates a basic but practical workflow for working with real-world healthcare data using Python.

## Dataset

The project uses the following dataset:

`healthcare_raw.csv`

The dataset contains **500 rows and 9 columns**.

### Columns

| Column              | Description                                              |
| ------------------- | -------------------------------------------------------- |
| `Patient_ID`        | Unique identifier for each patient                       |
| `Gender`            | Patient gender                                           |
| `Age`               | Patient age                                              |
| `Medical_Condition` | Recorded medical condition                               |
| `Admission_Date`    | Date when the patient was admitted                       |
| `Admission_Type`    | Type of admission, such as Routine, Urgent, or Emergency |
| `Medical_Code`      | Medical/ICD10 code                                       |
| `Billing_Amount`    | Patient billing amount                                   |
| `Discharge_Date`    | Date when the patient was discharged                     |

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Google Colab / Jupyter Notebook**

## Project Workflow

### 1. Import Libraries

The project uses NumPy, Pandas, Matplotlib, and Seaborn for data manipulation, statistical analysis, and visualization.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Load the Dataset

The healthcare CSV file is loaded into a Pandas DataFrame.

```python
df = pd.read_csv("/content/healthcare_raw.csv")
```

### 3. Explore the Dataset

The dataset is inspected to understand its structure and contents.

The analysis includes:

* Checking the number of rows and columns
* Viewing column names
* Inspecting the first and last records
* Checking data types
* Generating descriptive statistics
* Examining the overall dataset structure

The dataset contains **500 records and 9 attributes**.

### 4. Missing Value Handling

The `Medical_Code` column is checked for missing values.

If missing values are present, they are replaced with `"Unknown"`.

```python
df["Medical_Code"] = df["Medical_Code"].fillna("Unknown")
```

The column is then checked again to verify that the missing values have been handled.

### 5. Date Conversion

The `Admission_Date` and `Discharge_Date` columns are originally stored as text values. They are converted into Pandas datetime format to make date-based analysis easier.

```python
df["Admission_Date"] = pd.to_datetime(df["Admission_Date"])
df["Discharge_Date"] = pd.to_datetime(df["Discharge_Date"])
```

This allows the dates to be used for further analysis, such as calculating hospital stay duration or examining admission trends.

### 6. Statistical Analysis

Descriptive statistics are calculated for numerical columns such as:

* `Age`
* `Billing_Amount`

The dataset has an average patient age of approximately **50.11 years** and an average billing amount of approximately **7,249.00**.

## Key Dataset Information

| Attribute              |     Value |
| ---------------------- | --------: |
| Number of records      |       500 |
| Number of columns      |         9 |
| Average age            |     50.11 |
| Minimum age            |        22 |
| Maximum age            |        78 |
| Average billing amount |  7,249.00 |
| Minimum billing amount |  2,300.00 |
| Maximum billing amount | 14,200.00 |

## Purpose of the Project

The main purpose of this project is to practice **healthcare data analysis using Python**.

The project demonstrates how to:

* Load a CSV dataset
* Understand the structure of a dataset
* Inspect data types and records
* Identify and handle missing values
* Convert date columns
* Perform descriptive statistical analysis
* Prepare healthcare data for further analysis

## How to Run

### Using Google Colab

1. Open `Health_Care.ipynb` in Google Colab.
2. Upload `healthcare_raw.csv`.
3. Run the notebook cells from top to bottom.
4. Review the data inspection, cleaning, and analysis results.

### Using Jupyter Notebook

1. Install the required Python libraries.
2. Place `healthcare_raw.csv` in the project directory.
3. Open `Health_Care.ipynb`.
4. Run the notebook cells sequentially.

## Project Structure

```text
Healthcare-Data-Analysis/
│
├── Health_Care.ipynb
├── healthcare_raw.csv
└── README.md
```

## Conclusion

This project demonstrates a basic **Exploratory Data Analysis workflow for healthcare data using Python**.

It covers data loading, dataset exploration, missing-value handling, date conversion, and descriptive statistics. The project can be further extended with advanced visualizations, feature engineering, correlation analysis, patient admission trends, billing analysis, and other healthcare-related insights.
