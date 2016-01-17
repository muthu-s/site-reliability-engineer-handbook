# SQL Views

A view is a virtual table.

This chapter shows how to create, update, and delete a view.

###SQL CREATE VIEW Statement

In SQL, a view is a virtual table based on the result-set of an SQL statement.

A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database.

You can add SQL functions, WHERE, and JOIN statements to a view and present the data as if the data were coming from one single table.

###SQL CREATE VIEW Syntax
```
CREATE VIEW view_name AS
SELECT column_name(s)
FROM table_name
WHERE condition
```

**Note**: A view always shows up-to-date data! The database engine recreates the data, using the view's SQL statement, every time a user queries a view.

###SQL CREATE VIEW Examples
If you have the Northwind database you can see that it has several views installed by default.

The view "Current Product List" lists all active products (products that are not discontinued) from the "Products" table. The view is created with the following SQL:
```
CREATE VIEW [Current Product List] AS
SELECT ProductID,ProductName
FROM Products
WHERE Discontinued=No
```

We can query the view above as follows:
```
SELECT * FROM [Current Product List]
```