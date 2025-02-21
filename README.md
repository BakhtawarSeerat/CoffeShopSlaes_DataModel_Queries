# CoffeShopSlaes_DataModel_Queries
You are provided with a dataset containing Coffee Sales data. Your goal is to transform, clean the data and create a data model.

Import Data
_____________________________________________________________________________________________________________________________________________________________________________________________________________________

● Load the provided Coffee Shop Sales into Power BI.

Data Transformation:
_____________________________________________________________________________________________________________________________________________________________________________________________________________________

● Check Column names, data types, missing, and error values. (If any)

● Split the dataset into smaller tables to normalize the data:

○ Transactions:

transaction_id, transaction_date, transaction_time,
transaction_qty, store_id, product_id.

○ Stores:

store_id, store_location.

○ Products:
product_id, unit_price, product_category, product_type,
product_detail.

● Make sure to remove duplicates from each table.

Data Modeling
_____________________________________________________________________________________________________________________________________________________________________________________________________________________

● Identify Fact and Dimension Tables.

● Create Relationships between tables.

● Identify the schema.

Power Query Analysis
_____________________________________________________________________________________________________________________________________________________________________________________________________________________

Perform the following tasks:

1. Create a column for Sales
   
○ Merge column ”Unit price” from “products” to the “Transaction” table.

○ Create a custom column: Sales = unit price x transaction_qty.

2. Conditional column:
   
○ Create a conditional column Is High Quantity:

If transaction_qty > 4, return "Yes", otherwise "No".

3. Parameters:
   
○ Calculate the given and store them as parameters:

i. Calculate Total Sales: Sum of Total Sales.

ii. Calculate Average Transaction Quantity: Average of transaction_qty.

4. Filter based on parameters:
   
○ Create a duplicate of the Transactions Table.

○ Filter the transactions with a quantity greater than the parameter “ Average transaction quantity”.

5. Sales Based on Location:
   
○ Merge Sales from “Transaction Table” to “Store” and show the aggregated value “Sum of Sales”.

7. Count of Products in each product Category:

○ Create a duplicate of “Products”. Apply GroupBY to count products in each category. Rename this table as “Product summary”
