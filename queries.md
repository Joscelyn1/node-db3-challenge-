# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT Categories.CategoryName, Products.ProductName FROM [Products]
inner join [Categories] on Products.CategoryID = Categories.CategoryID

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

SELECT Orders.OrderID, Shippers.ShipperName FROM [Orders]
inner join [Shippers] on Shippers.ShipperID = Orders.ShipperID
where Orders.OrderDate < '1997-01-09'

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

SELECT Products.ProductName, OrderDetails.Quantity FROM [Products]
inner join [OrderDetails] on Products.ProductID = OrderDetails.ProductID
where OrderDetails.OrderID = 10251
order by Products.ProductName

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

SELECT Orders.OrderID, Customers.CustomerName, Employees.LastName FROM [Orders]
inner join [Customers], [Employees] on Orders.CustomerId = Customers.CustomerId AND Orders.EmployeeID = Employees.EmployeeId

### (Stretch) Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a column called ItemCount that shows the total number of products placed on the order. Shows 196 records.
