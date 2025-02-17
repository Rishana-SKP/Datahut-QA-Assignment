# Datahut-QA-Assignment

### Overview
This repository contains the complete data cleaning project for the provided dataset, messy_Data.csv. The main objective of this assignment is to clean and standardize the dataset to ensure it is ready for analysis. The project addresses issues such as missing values, duplicates, incorrect email formats, noisy names, inconsistent date formats, department name typos, and salary anomalies.

#### Key issues addressed include:
* Missing values and inconsistent data types.
* Incorrect email formats and non-professional email domains.
* Noisy and inconsistent name fields.
* Inconsistent date formats.
* Department name errors (typos, missing values, and non-standard entries).
* Salary anomalies and outlier detection.
* Duplicate record removal.

Every step has been documented in a Jupyter Notebook, and all quality issues are logged in an Excel file (QA_Issues.xlsx).

#### Data Cleaning Process
The data cleaning process was carried out in the following steps:

###### Loading the Data

The dataset was loaded into a Jupyter Notebook using the pandas library.
Initial data inspection was performed using .info(), .head(), and .describe() to understand the dataset's structure and data types.

###### Inspection and Quality Assessment
The dataset was analyzed for missing values, duplicate records, and inconsistencies in data formats.
Use .isnull().sum() to identify missing values.
Use .duplicated() to check for duplicate rows.
Review summary statistics to identify outliers and inconsistent formats.
Detailed observations were recorded in an Excel file (QA_Issues.xlsx).

###### Handling Missing Values
Numerical fields with missing values were imputed using mean or median values based on the data distribution.
Categorical fields with missing values were filled using the mode or labeled as "Unknown".
Rows with excessive missing data were removed to maintain data integrity.

###### Removing Duplicates
Duplicate records were identified and removed using pandas' .duplicated() function to ensure each record is unique.
Remove duplicates while keeping the first occurrence.

###### Correcting Email Formats
Email addresses were validated against a regex pattern.
Invalid or non-professional email addresses were corrected or removed.
Only professional emails were retained for the final dataset.

###### Cleaning Name Fields
Extraneous characters, numbers, and special characters were removed from the name fields.
Names were standardized to proper title case to ensure consistency.

###### Standardizing Date Formats
The Join Date column was standardized to the YYYY-MM-DD format.
Dates with inconsistent or erroneous values were corrected.

###### Correcting Department Names
Department names were validated against a predefined list (HR, Engineering, Marketing, Sales, Support).
Typographical errors and inconsistent capitalization were corrected.

###### Handling Salary Noise
Salary values were examined for outliers (e.g., salaries below 20,000 or above 300,000).
Identified anomalies were flagged for review and corrected accordingly.

###### Documentation
Every step of the cleaning process was documented in the Jupyter Notebook.
A detailed QA report was created in the Excel file (QA_Issues.xlsx) that lists the issues, affected row numbers, solutions, and suggestions to avoid future issues.

#### Tools and Technologies
Python 3.x
pandas
Jupyter Notebook
Excel (for QA documentation)
Regex (for pattern matching)


#### Deliverables
cleaned_dataset.csv: The final cleaned and standardized dataset.
QA_Issues.xlsx: Excel file detailing all identified data quality issues, proposed solutions, and prevention measures.
Data_Cleaning_Notebook.ipynb: Jupyter Notebook documenting the entire data cleaning process.
README.md: This file, providing an overview and instructions for the project.


#### Assumptions and Considerations
Missing Values: Imputed using mean/median (numerical) or mode/“Unknown” (categorical).
Email Validation: Only professional email addresses are retained.
Salary Thresholds: Salaries outside the range of 20,000 to 300,000 are considered unrealistic.
Department Names: Standardized based on a predefined list.
Duplicates: Only exact duplicates are removed, ensuring data integrity.
Data Line Numbers: The row indices where issues are found are documented for easy tracking and reference.

#### Future Recommendations
Data Entry Validation: Implement front-end validations to reduce errors during data entry.
Automated Cleaning: Integrate automated data quality checks to flag issues in real time.
Regular Audits: Schedule periodic audits of the dataset to maintain high data quality.
Enhanced Logging: Improve error logging and tracking mechanisms to capture more detailed information on data issues.

#### Contact
For any queries, feel free to reach out via GitHub
