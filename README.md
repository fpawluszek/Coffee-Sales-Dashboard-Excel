# Coffee Orders Data Project

In this project I used Excel to clean and organize data in order to create an interactive Dashboard that shows the coffee sales data from a fictitious company to enable data driven decision-making.

# Sheets
- The first sheet includes the finalized **Dashboard**.
- The last three sheets show the raw data I started the project with. This includes:
  1) **orders_raw_data**, where the primary key is the "Order ID" column.
  2) **customers_raw_data**, related to the **orders** sheet through the "Customer ID" column.
  3) **products_raw_data**, which relates to the **orders** sheet through the "Product ID" column.
- The **orders**, **customers** and **products** sheets are where you will find the tables with the data after it was cleaned and organized through the steps explained below.
- **TotalSales**, **CountryChart** and **Top5Customers** include pivot tables intended to facilitate the creation of visualizations and filters that will become part of the final dashboard.

# Steps taken
- Populating the orders table
  1) Used XLOOKUP to reference each customer's information (name and email) and add it to the **orders** table. Some customers didn't have email data, so they are shown as "N/A".
  2) Used INDEX and MATCH to dynamically populate each cell with the product information taken from the **products** table.
  3) Calculate **Sales**.
  4) Create a **Coffee Type Full Name** column that shows the full name of each coffee type (this will be needed later to make the Dashboard easier to read). Use a nested IF formula to populate the column.
  5) Create a **Roast Type Name** column to show the name of the different kinds of roasts, and populate it using a similar nested IF function.
  6) Create a **Loyalty Card** column showing whether each customer has a card or not. Once again use XLOOKUP to populate this column with data from the **customers** table.
 
- Formatting and cleaning the orders table
  1) Format the **Date** column.
  2) Add the proper metric to the values in the **Size** column, making it clear we are talking about Kg.
  3) Show **Unit Price** and **Sales** as currency values.
  4) Select our table and check for duplicate values using the "Remove Duplicates" tool.
  5) Convert the entire table into an Excel formatted table.
 
- Pivot Tables, Visualizations and Dashboard Creation
  1) Create a Pivot Table to analyze total sales over time in a new sheet named **TotalSales**.
  2) Insert a timeline to allow for closer analysis of specific time periods.
  3) Create slicers for **Roast Type**, **Size** and **Loyalty Card** to allow filtering through these parameters in our final dashboard.
  4) Duplicate the pivot table sheet to create a new pivot table showing **Sales** by **Country**. This will allow us to add another visualization to our dashboard.
  5) Duplicate the pivot table sheet once again. This time we use it to show **Customer Name** and **Sales** so we can add another visualization showing our **Top5Customers**.
  6) After editing the desing and properly sorting each visualization we now create a new sheet to put everything together in a **Dashboard**.
  7) Make sure that every Slicer and Timeline in the dashboard is linked to every visualization using the Report Connections tool.
  8) We finally have a fully interactive **Dashboard** where we can use different filters to get visual representations of the data to draw conclusions and inform decision-making.
