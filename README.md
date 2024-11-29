# Crowdfunding_ETL Project
- **Group: 10**

## Requirements:

### Install dependencies:

Imported Pandas and Numpy dependencies
Run Python version 3.10.14 and 3.12.7
Extracting the Crowdfunding Data
Got a brief summary of the crowdfunding_info DataFrame using '.info'

### Category and Subcategory DataFrames:

- Create a Category DataFrame that has the following columns:
We load the crowdfunding dataset from an Excel file.
We extract the unique categories from the 'category' column.
We create a new DataFrame that includes a sequentially numbered 'category_id' and the unique 'category' names.
Finally, we export this DataFrame to a CSV file named`category.csv`.

- Create a SubCategory DataFrame that has the following columns:
Prepare the data that will be used to create the DataFrames. You should have lists of category names, subcategory names, and their corresponding IDs
A "subcategory_id" column that is numbered sequential form 1 to the length of the number of unique subcategories.
A "subcategory" column that has only the subcategories.
Export the DataFrame as a `subcategory.csv` CSV file.

_ Conclusion:
The category and subcategory Dataframes have been successfully created and exported as csv files.

### Campaign DataFrame:

This document outlines the structure and content of the Campaign DataFrame created for our project.
DataFrame Structure:

The Campaign DataFrame includes the following columns:

cf_id: Unique identifier for each crowdfunding campaign.

Contact_id: Identifier for the contact associated with the campaign.

company_name: Name of the company running the campaign.

description: A brief description of the campaign.

goal: The funding goal for the campaign, represented as a float data type.

pledged: The amount pledged by backers, represented as a float data type.

outcome: The result of the campaign (e.g., successful, failed).

backers_count: The number of backers who contributed to the campaign.

country: The country where the campaign is based.

currency: The currency used for pledges.

launch_date: The date and time when the campaign was launched, converted to the datetime format.

end_date: The date and time when the campaign ended, converted to the datetime format.

category_id: Unique identification numbers that match those in the category DataFrame.

subcategory_id: Unique identification numbers that match those in the subcategory DataFrame.



We renamed the blurb, launched_at, and deadline columns into 'description', 'launched_date' and 'end_date' respectively using the function '.rename()'.Used the astype function to convert the 'goal' and 'pledged' columns into float.To format the launched_date and end_date columns to datetime format we import the datetime dependencies.

We merged the campaign_df with the category_df and the subcategory_df using the '.merge()' function. and also dropped these unwanted columns; 'staff_pick', 'spotlight', 'category & sub-category','category' 'subcategory' using '.drop()' function.

_Conclusion:
The Campaign Dataframes have been successfully created and exported as csv files for further analysis and use.

### Contacts DataFrame:

Our team chose Option 1 Use Python dictionary method to extract and transform the data from the contacts.xlsx Excel data into a Dataframe.
Iterate through each dictionary, by extracting the dictionary values from the keys using a Python list comprehension.
Add the values for each row to a new list
Create a new DataFrame that contains the extracted data
Split "name" column value into a first and last name using the 'split()' function and place each in a new column.
And dropped the'name' column using '.drop()' function, and reorder all columns using double square brackets.

_Conclusion:
A cleaned DataFrame is exported as a `contacts.csv` CSV file and saved to GitHub repository.


### Crowdfunding_db Database: 

A database schema labeled, crowdfunding_db_schema.sql is created.

The database has the appropriate primary and foreign keys and relationships.

Each CSV file is imported into the appropriate tables.


_Conclusion:
The data from each table is displayed using a SELECT * statement: We run the select all and saved screenshots of the results on GitHub repository.






## License
This project is licensed under the MIT License.