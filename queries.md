# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT p.productName,c.categoryName  FROM products as p
join categories as c on p.categoryID = c.categoryID

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

SELECT o.orderId,s.shippername  
FROM orders as o
join shippers as s on o.shipperId = s.shipperId
where orderDate < '1997-01-09'

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

SELECT p.productName, o.quantity
FROM products as p
join orderdetails as o on p.productId = o.productId
where orderId = 10251
order by p.productName

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

SELECT o.OrderId, c.customerName as 'Customer Name', e.lastName as 'Employee Last Name'
FROM orders as o
join customers as c on o.customerId = c.customerId
join employees as e on o.employeeId = e.employeeId

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 