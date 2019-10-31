# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT productname,categoryname FROM Products p join categories c on p.categoryid=c.categoryid

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

select o.orderid, s.shippername,o.orderdate from orders o join shippers s on o.shipperid=s.shipperid where o.orderdate<'1997-01-09'

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

select o.orderid, p.productname, o.quantity from orderdetails o, products p where o.productid=p.productid and o.orderid=10251

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

SELECT o.OrderID,
c.CustomerName Customer,
e.LastName Employee_Last_Name
FROM Orders o
JOIN Employees e ON o.EmployeeID = e.EmployeeID
JOIN Customers c ON o.CustomerID = c.CustomerID

### (Stretch) Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a column called ItemCount that shows the total number of products placed on the order. Shows 196 records.
