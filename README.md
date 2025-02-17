# Datahut-QA-Assignment

### Overview
This repository contains the complete data cleaning project for the provided dataset, messy_Data.csv. The main objective of this assignment is to clean and standardize the dataset to ensure it is ready for analysis. The project addresses issues such as missing values, duplicates, incorrect email formats, noisy names, inconsistent date formats, department name typos, and salary anomalies.

Datahut-QA-Assignment/
├── messy_Data.csv                 # Original messy dataset
├── cleaned_dataset.csv            # Final cleaned dataset ready for analysis
├── QA_Issues.xlsx                 # Excel file documenting data quality issues, solutions, and prevention suggestions
├── Data_Cleaning_Notebook.ipynb   # Jupyter Notebook containing the data cleaning process and documentation
└── README.md                      # This README file

#### Data Cleaning Process
The data cleaning process was carried out in the following steps:

###### Loading the Data

The dataset was loaded into a Jupyter Notebook using the pandas library.
Initial data inspection was performed using .info(), .head(), and .describe() to understand the dataset's structure and data types.

###### Inspection and Quality Assessment
The dataset was analyzed for missing values, duplicate records, and inconsistencies in data formats.
Detailed observations were recorded in an Excel file (QA_Issues.xlsx).

###### Handling Missing Values
Numerical fields with missing values were imputed using mean or median values based on the data distribution.
Categorical fields with missing values were filled using the mode or labeled as "Unknown".
Rows with excessive missing data were removed to maintain data integrity.

###### Removing Duplicates
Duplicate records were identified and removed using pandas' .duplicated() function to ensure each record is unique.

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
