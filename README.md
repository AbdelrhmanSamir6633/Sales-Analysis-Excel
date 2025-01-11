# Sales-Analysis-Excel-PowerQuery-PivotTables
In this project, I utilized Excel and Power Query to perform an in-depth sales analysis. The goal was to analyze raw sales data, identify key performance metrics, and deliver actionable insights through a dynamic and interactive dashboard.

After downloading AdventureWorks dataset  " .bak file "  from Microsoft Learn (The Link is provided Finally in the last section "Data Sources") 
1-) I imported the " .bak file " in SQL Server using SSMS.
2-) From Data view in Microsoft Excel, I imported the dataset from SQL Server to Microsoft Excel PowerQuery to apply some data transformation and cleaning to make dataset ready for analysis and visualization like:
  - Clear unnecessary columns.
  - Handling NULL values.
  - Merging some columns together.
  - Joining Tables together using "Merge Queries" command.
  - Handling PK and FK between tables.
  - ... and so on.

  Final Result after data transformation:
  ![Power_Query](https://github.com/user-attachments/assets/558fa916-89a1-4372-856d-a0aea6ae1ce6)


  - Finally, I had 3 Tables ( 1 FACT Table and 2 DIMENSION Tables ):
     - FACT Table:
        - Sales table: contains FKs of DIMENSION Tables + the full details about all sales transactions including:
           - [SalesOrderID]: The ID of each SalesOrder.
           - [OrderDate], [DueDate], and [ShipDate]: which express detailed dates of SalesOrder process.
           - [CustomerID]: which expresses to which customer was this order sold?
           - [SalesPersonID]: which expresses who the salesman sold the order?
           - [TerritoryID] (FK): which expresses in which territory/region this order was sold?
           - [ProductID] (FK): which expresses the product that the order contains.
           - [OrderQty]: which expresses the quantity of each product in each order.
           - [UnitPrice]: which expresses the unit price of each product in each order.
           - [TotalDue]: which expresses Total Sales of each order. 

     - DIMENSION Tables:
       - SalesTerritory table: contains Name and ID of each Territory with columns [TerritoryID] and [Name].
       - Products table: contains details about each product with columns [ProductID], [SubcategoryID], [CategoryID], [Product Name], [Subcategory Name], and [Category Name] that describe full characteristics of each product.

  The Dimensional Data Model is STAR SCHEMA, as shown below:

  Data Model:
![Data_Model](https://github.com/user-attachments/assets/65386f8f-abf3-4e51-b7e4-616978679806)
   
3-) After data preparation in PowerQuery, I loaded data (ONLY the 3 tables mentioned above) into Excel worksheet to start the analysis and visualization processes using Pivot Tables, as shown below:

Pivot Tables:
![Pivot_Tables_page-0001](https://github.com/user-attachments/assets/5b1453cc-fbc2-46d3-8a09-02fbe64bc612)

4-) I leverege the different types of charts and visuals to create an informative, user-friendly and visually appealing interactive dashboard tailored to manager specific needs, as shown below:

FINAL Dashboard:
![FINAL Dashboard_page-0001](https://github.com/user-attachments/assets/9cf0054e-82a8-4f41-af30-c6622824c7aa)


Dataset Source:
- <a href="https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms">AdventureWorks2012 from Microsoft Learn </a>
 
