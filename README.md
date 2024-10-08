# Crowdfunding_ETL
NW Bootcamp Project 2

# As stated by my partner Adam in his repo https://github.com/AdamKarner/Crowdfunding_ETL, this ETL (Extract, Transform, Load) script is designed to process and transform data from a crowdfunding dataset (crowdfunding.xlsx) and a contacts dataset (contacts.xlsx) using Python and Pandas. The script performs data extraction, transformation, and exports the final transformed data into CSV files that can be further used to create an ERD (Entity-Relationship Diagram) and a PostgreSQL database. In order to complete this project I used a couple of repos for reference to review my code and check my work. https://github.com/Asalvs/Crowdfunding_ETL
https://github.com/micah-trp/Crowdfunding_ETL


# Create Category and Subcategory DataFrames : I extracted and transformed the crowdfunding.xlsx excel data to create a dataframe, which included a "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories. A "category" column that contains only the category titles. Next, i exported the category DF as a csv. I extracted and transformed the excel dara once again to create a subcategory DF with the following columns: A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories. As well as a  "subcategory" column that contains only the subcategory titles. I then exported the subcategory DF as a csv.

# Create the Campaign DataFrame : I extracted and transformed the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

The "cf_id" column

The "contact_id" column

The "company_name" column

The "blurb" column, renamed to "description"

The "goal" column, converted to the float data type

The "pledged" column, converted to the float data type

The "outcome" column

The "backers_count" column

The "country" column

The "currency" column

The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format

The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format

The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame

The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame. 
Finally, exporting the campaign dataframe as a csv. 

# My partner was then in charge of creating the Contacts DataFrame using the first option, which consisted of using python dictionary methods. Import the contacts.xlsx file into a DataFrame. Iterate through the DataFrame, converting each row to a dictionary. Iterate through each dictionary, doing the following: Extract the dictionary values from the keys by using a Python list comprehension. Add the values for each row to a new list. Create a new DataFrame that contains the extracted data. Split each "name" column value into a first and last name, and place each in a new column. Clean and export the DataFrame as contacts.csv.

# After it was brought to our attention that some of the project work was missing, I went ahead and used the csv file information to sketch an ERD. With that information, I made a table schema for each CSV file into the "crwodfunding_db" that I created in Postgres. 
