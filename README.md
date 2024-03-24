# Crowdfunding ETL

This project is a mini project focused on building an ETL (Extract, Transform, Load) pipeline using Python, Pandas, and either Python dictionary methods or regular expressions. The goal is to extract data from an Excel file, transform it, and load it into CSV files and eventually into a PostgreSQL database. 

## Instructions

The instructions for this mini project are divided into the following subsections:

### Create the Category and Subcategory DataFrames

1. **Create a category DataFrame:** 
   - Include a "category_id" column with entries going sequentially from "cat1" to "catn", where n is the number of unique categories.
   - Include a "category" column containing only the category titles.
2. **Export the category DataFrame:** 
   - Save it as `category.csv` in your GitHub repository.

3. **Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame:** 
   - Include a "subcategory_id" column with entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories.
   - Include a "subcategory" column containing only the subcategory titles.
4. **Export the subcategory DataFrame:** 
   - Save it as `subcategory.csv` in your GitHub repository.

### Create the Campaign DataFrame

1. **Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame:** 
   - Include the following columns:
     - "cf_id"
     - "contact_id"
     - "company_name"
     - "description" (renamed from "blurb")
     - "goal" (converted to float)
     - "pledged" (converted to float)
     - "outcome"
     - "backers_count"
     - "country"
     - "currency"
     - "launch_date" (renamed from "launched_at" and converted to datetime)
     - "end_date" (renamed from "deadline" and converted to datetime)
     - "category_id" (matching the unique identification numbers in the "category_id" column of the category DataFrame)
     - "subcategory_id" (matching the unique identification numbers in the "subcategory_id" column of the subcategory DataFrame)
2. **Export the campaign DataFrame:** 
   - Save it as `campaign.csv` in your GitHub repository.

### Create the Contacts DataFrame

1. **Choose one of the following options for extracting and transforming the data from the contacts.xlsx Excel data:**
   - Option 1: Use Python dictionary methods.
   - Option 2: Use regular expressions.

### Create the Crowdfunding Database

1. **Inspect the four CSV files:** 
   - Sketch an ERD of the tables using a tool like QuickDBD.
   
2. **Create a table schema for each CSV file:** 
   - Specify data types, primary keys, foreign keys, and other constraints.
   - Save the database schema as a Postgres file named `crowdfunding_db_schema.sql`, and store it in your GitHub repository.

3. **Create a new Postgres database:** 
   - Name it `crowdfunding_db`.

4. **Create tables in the correct order to handle foreign keys:** 
   - Use the information from the ERD.

5. **Verify table creation:** 
   - Run a SELECT statement for each table.

6. **Import each CSV file into its corresponding SQL table.**

7. **Verify data:** 
   - Run a SELECT statement for each table to ensure that each table has the correct data.

[Include any acknowledgments, links to documentation, or additional information that you think would be helpful to users and contributors.]
