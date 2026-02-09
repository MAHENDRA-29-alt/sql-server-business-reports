-- Queries for Sales Reporting Project

-- 1. Monthly Sales Report
SELECT 
    FORMAT(O.OrderDate, 'yyyy-MM') AS Month,
    SUM(P.Price * OD.Quantity) AS TotalSales
FROM Orders O
JOIN OrderDetails OD ON O.OrderID = OD.OrderID
JOIN Products P ON OD.ProductID = P.ProductID
GROUP BY FORMAT(O.OrderDate, 'yyyy-MM');

-- 2. Top Customers by Sales
SELECT 
    C.CustomerName,
    SUM(P.Price * OD.Quantity) AS TotalSpent
FROM Customers C
JOIN Orders O ON C.CustomerID = O.CustomerID
JOIN OrderDetails OD ON O.OrderID = OD.OrderID
JOIN Products P ON OD.ProductID = P.ProductID
GROUP BY C.CustomerName
ORDER BY TotalSpent DESC;

-- 3. Product Performance
SELECT 
    P.ProductName,
    SUM(OD.Quantity) AS TotalQuantitySold
FROM Products P
JOIN OrderDetails OD ON P.ProductID = OD.ProductID
GROUP BY P.ProductName;
