# Crowdfunding_ETL

## Introduction

  The purpose of this project is to extract, transform, and load (hence, ETL) data related to crowdfunding using both Python and SQL. Pandas and Python are used to extract and transform raw data, and PostgreSQL and pgAdmin were used to load clean data that is ready for analysis.

## Sources of data

Within Resources Folder:
*  contacts.xlsx
*  crowdfunding.xlsx

## Database & Tools Used

* Database : postgreSQL
* Data Cleaning and Processing: Jupyter Notebook
* Packages Used: pandas, numpy, datetime, plotly
* Data Loading: pgAdmin

## Steps

### Extraction and Transformation

#### Category and Subcategory DataFrames
- We extracted data from the "crowdfunding.xlsx" Excel file to create a category DataFrame.
- We performed similar extraction and transformation to create a subcategory DataFrame.
- Both DataFrames were exported to "category.csv" and "subcategory.csv" respectively.

#### Campaign DataFrame
- We extracted campaign data from the "crowdfunding.xlsx" Excel file.
- The campaign DataFrame underwent various transformations, including data type conversions and renaming of columns.
- UTC times were converted to datetime format for "launch_at" and "deadline".
- Category and subcategory IDs were added to link with the respective DataFrames.
- The transformed campaign DataFrame was exported to "campaign.csv".

#### Contacts DataFrame
- We used two methods to extract and transform data from the "contacts.xlsx" Excel file using Python dictionary methods
- For both methods, we extracted contact IDs, names, and email addresses.
- In the dictionary method, we iterated through the DataFrame and created dictionaries for each row.
- The transformed contacts DataFrame was exported to "contacts.csv".

### Loading data to the Database
- We sketched an Entity-Relationship Diagram (ERD) using the QuickDBD tool.
- Using the ERD, we designed a table schema for each CSV file, specifying data types, primary keys, and foreign keys.
- The table schema was saved in "crowdfunding_db_schema.sql".
- Tables were created in the correct order to handle the foreign keys.
- CSV files were imported into corresponding SQL tables.
- The loaded data was verified using SELECT statements.



## Authors

* Deelan Patel
* Yashesh Darji
