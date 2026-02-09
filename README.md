# Project: SQL Server Sales Reporting

## Problem
The business needed monthly sales and customer performance reports to track revenue and identify top-performing products and customers. Manual tracking was time-consuming and prone to errors.

## Solution
I designed a SQL Server database with the following tables:
- **Customers**: Customer details
- **Products**: Product details
- **Orders**: Order information
- **OrderDetails**: Product quantities per order

Using SQL queries, I:
- Joined multiple tables to fetch combined data
- Used `GROUP BY` and aggregation functions for monthly sales and total spending
- Implemented reporting queries to identify top customers and product performance

## Sample Output

**Monthly Sales Report**
| Month    | TotalSales |
|----------|------------|
| 2024-01  | 56000      |
| 2024-02  | 1500       |

**Top Customers by Sales**
| Customer Name | TotalSpent |
|---------------|------------|
| Ravi Kumar    | 56500      |
| Anita Sharma  | 1500       |
| John Paul     | 0          |

**Product Performance**
| Product Name | TotalQuantitySold |
|--------------|-----------------|
| Laptop       | 1               |
| Mouse        | 5               |
| Keyboard     | 1               |

## Skills Used
- SQL Server
- Joins (INNER, LEFT)
- Aggregations (SUM, COUNT)
- Group By & Subqueries
- Reporting & Data Analysis

## Optional Notes
- Queries are included in the `queries.sql` file.
- Tables creation and sample data are included in `tables.sql` and `insert-data.sql`.
- Designed for clarity, maintainability, and easy extension for additional reporting needs.

