# Crowdfunding ETL Project
This ETL mini project focuses on building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform data. The project involves working with a partner to divide the work, collaborate, and communicate effectively.

## Project Overview
The main objectives of this mini project are as follows:

- Build an ETL pipeline to extract and transform data.
- Create four CSV files from the transformed data.
- Use the CSV file data to create an Entity-Relationship Diagram (ERD) and a table schema.
- Upload the CSV file data into a Postgres database.
- To stay on track, ensure that at least half of the project is completed before the third day of class.

## Getting Started
- Create a new repository named "Crowdfunding_ETL" for this project. Add your partner as a collaborator. Do not add this project to an existing repository.
- Clone the new repository to your computer.
- Rename the ETL_Mini_Project_starter_code.ipynb file with the first name initial and last name of each member of the group, for example, ETL_Mini_Project_NRomanoff_JSmith.ipynb.
- Add the renamed Jupyter notebook file and the Resources folder containing the crowdfunding.xlsx and contacts.xlsx files to your repository.
- Push the changes to GitHub.
- Have your partner pull the changes, so both of you have the same notebook available on your computer.
As you work through the project deliverables, you may find it helpful to break up the work across other notebooks that you each work on individually. However, once complete, please combine all the subsections back into the final ETL_Mini_Project notebook.

## Instructions
The instructions for this mini project are divided into several subsections, as follows:

### 1. Create the Category and Subcategory DataFrames
Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame with the following columns:

- category_id (entries going sequentially from "cat1" to "catn", where n is the number of unique categories)
- category (containing only the category titles)
Export the category DataFrame as category.csv and save it to your GitHub repository.

Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame with the following columns:

- subcategory_id (entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories)
- subcategory (containing only the subcategory titles)
Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

 ![image](https://github.com/NoorBelhaj/Crowdfunding_ETL/assets/126538596/e0ab49ca-51b6-4cd3-b562-0866ee8060b5) 
 ![image](https://github.com/NoorBelhaj/Crowdfunding_ETL/assets/126538596/bac0a367-a8cf-4fb6-bddd-0675ab9e8c68)

### 2. Create the Campaign DataFrame
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame with the following columns:

- cf_id
- contact_id
- company_name
- description (renamed from blurb)
- goal (converted to the float data type)
- pledged (converted to the float data type)
- outcome
- backers_count
- country
- currency
- launch_date (renamed from launched_at, with UTC times converted to the datetime format)
- end_date (renamed from deadline, with UTC times converted to the datetime format)
- category_id (with unique identification numbers matching those in the category_id column of the category DataFrame)
- subcategory_id (with unique identification numbers matching those in the subcategory_id column of the subcategory DataFrame)
Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

![image](https://github.com/NoorBelhaj/Crowdfunding_ETL/assets/126538596/c757cb78-1404-44d0-b80a-f65bd0b672f4)


### 3. Create the Contacts DataFrame
Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:

Option 1: Use Python dictionary methods.
- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary and do the following:
  - Extract the dictionary values from the keys using a Python list comprehension.
  - Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each name column value into a first_name and last_name, placing each in a new column.
Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

Option 2: Use regular expressions.
- Import the contacts.xlsx file into a DataFrame.
- Extract the contact_id, name, and email columns using regular expressions.
- Create a new DataFrame with the extracted data.
- Convert the contact_id column to the integer type.
- Split each name column value into a first_name and last_name, placing each in a new column.
- Clean the DataFrame and export it as contacts.csv. Save it to your GitHub repository.

 ![image](https://github.com/NoorBelhaj/Crowdfunding_ETL/assets/126538596/7e5df876-5c48-429f-a6ff-859b5d63f9c9)

 
### 4. Create the Crowdfunding Database
- Inspect the four CSV files and sketch an ERD of the tables using QuickDBD.
- Use the information from the ERD to create a table schema for each CSV file. Specify the data types, primary keys, foreign keys, and other constraints.
- Save the database schema as a Postgres file named crowdfunding_db_schema.sql. Save it to your GitHub repository.
- Create a new Postgres database named crowdfunding_db.
- Use the database schema to create the tables in the correct order to handle the foreign keys.
- Verify the table creation by running a SELECT statement for each table.
- Import each CSV file into its corresponding SQL table.
- Verify that each table has the correct data by running a SELECT statement for each.
      ![image](https://github.com/NoorBelhaj/Crowdfunding_ETL/assets/126538596/ed82c200-c0aa-4a5c-a5c0-c5ef0139f441)

