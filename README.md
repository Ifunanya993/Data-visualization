# Data-visualization

Power BI offers basic visualization such as bar charts, line charts, and tables. They are effective
for comparing values, showing trends over time ,or displaying categorical data. These visaulizations 
enable users to explore hierachial data, relationships, geographical patterns and distribution of values.

## Dashboard and report design

### Creating Dashboard

Power BI allows users to create interactive multiple visualizations on a single canvas.
It also allows users to arrange and resize visualizations, add filter, and create a cohesive
story with data.

### Designing reports

Power BI enables users to design comprehensive reports with multiple pages or sections.
Users can add visuals, text boxes, images, and shapes to create engaging and informative
reports.

Reports in Power BI gives more comprehensive and detailed insights into data. It can design
reports to present a story or analysis by organizing visuals and prouding context through 
explanatory text.

### Sharing collaboration

It enables sharing and collaboration by allowing users to publish and share dashboards and reports
with others. users can collaborate, add comment, ans=d perform version control


## DATA ANALYSIS EXPRESSION (DAX)

It is a formular language used in Power BI , Excel power pivot, and Analysis service Tabular models.
It is designed to perform calculations , create custom measures, and manipulates data within these
microsoft tools.

### Calculations in DAX

Calculated columns: They are column in a table that are derived from an expression or formular
defined in DAX.

These columns can be used for data transformations, calculations, or complex calculations based
on existing columns.

Measures : They are calculations that aggregate data and provide insights into the undrlying 
data needed.

It allows users to perform calculations like sums, averages, counts, and other aggregations based 
on specified conditions.

Calculated Tables : In addition to calculate columns and measures, DAX allow the creation of calculated
tables. They are tables that are defined using DAX expressions based on existing table.

These expressions can involve filtering, joining, or performing other calculations to create new tables with 
customized data.


## COMMON DAX FUNCTIONS

### SUM

It calculates the sum of values in a column or expression.
SYNTAX : SUM( Column or expression)

### AVERAGE

It calculates the average of values in a column or expression
SYNTAX : AVERAGE( Column or expression)

### COUNT

It counts the number of roes in a column or expression .
SYNTAX : COUNT(Column or expression)

### MIN

It returns the minimum value from a column .
SYNTAX : MIN(Column or expression)

### MAX

It returns the maximum value from a column or expression.
SYNTAX : MAX(Column or expression)

### IF

It evaluates a condition and returns one value if true and another if false.
SYNTAX : IF( Condition value_if_true or value_if_false)

### RELATED

It retrieves a value from a related table based on a relationship
SYNTAX : RELATED( table[column])



## DATA MODELLING AND RELATIONSHIPS

Data modelling in Power BI is one of the features used to connect mulpitple Data sources using
a relationship. A relationship defines how data sources are connected with each other and you can 
create an interesting data visualization on multiple data sources.

Importance of Data Modelling

It helps create a unifiedview of data by defining tables, columns, and relationship.
It lmproves data organisation, accuracy, and consistency for effecive analysis and 
reporting.

_____________


## QUESTION

USING THE BANK TERM DEPOSIT SUBSCRIPTION DATASET PROVIDED

- Create a dashboard
  
- Create a measure for the Average age depositor
  
- Create a new column named 'Age-band' containing the following
  
1. 'young' for age below 30

2. 'Mid-aged' for age between 30-50

3. 'Old' for age above 50

- Create a measure calculating the total balance for

1. Job - Technician

2. Marital - single and married.

- USING 'OLIST' DATASETS

1.  Create a relationship among all the tables. 
  

## SOLUTION

### To create a dashboad

Import the CSV data.

Transform your data in Query Editor and load

Click on the Report view at the left pane of your desktop

Click on a new card for a single creation

Click on visualization to format


### Average age depositor

Click on a new measure

Average age depositor = Average(bank-full[age])
and  enter.


### To create a column name AGE-BAND and enter the conditions

Click on the new column 

Change the Data type

Use Age-band = IF(Bank-full[age]<30,"young",if(bank-full[age]<=50,"mid-aged","old")
and click ok.


### To create a measure total balance for Job-Technician

Click on new measure

Total balance for Job Technician = calculate (sum(bank-full[balance]), filter(bank-full,
bank-full[job] = "Technician")


### For marital-Married

Click on new measure

Total balance for marital-married = calculate (sum(bank-full[balance]), filter(bank-full,
bank-full[marital] = " married")



### TO create a relationship between OLIST tables

Data modelling

Power BI supports three relationship types which includes:

- One_on_one relationship : This links one record in a table to exactly one record
in another table.

- One_to_many relationship : It links one record to multiple related records in another
table.

- Many_to_many relationship : It involves intermediate tables to establish connections between multiple
records in different tables.

Primary keys uniquely identify each record in a table and ensure data intergrity.

Foreign keys establihsh relationships by linking to the primary key of another table.

Import the OLIST datasets from csv files

Click on Model at the left pane of your desktop.

By default, Power BI will create a relationship

To delete a connection, right click on the connection link and delete.

OLIST datasets and their relationships
 
Employees table and Customer table : The tables was connected by City, which is the common column.

Shippers table and Orders table: The tables was connected by ShipperID, which is the common column.

Order details  table and Products table : The tables was connected by ProductID, which is the common column.

Employees table and Orders table : The tables was connected by EmployeeID, which is the common column.

Category table and Product table : The tables was connected by CategoryID, which is the common column.

Shippers table and Order table : The tables was connected by ShippersID, which i the common column.

Order details table and Order table : The tables was connected by OrderID, which is the common column.

Shippers table and Customer table : The tables was connected by Companyname, which is the common column.

Customers table and Order table : The tables was connected by CustomerID, which is the common column.














