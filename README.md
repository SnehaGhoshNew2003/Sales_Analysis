# Sales_Analysis

This repository contains an SQL dump file (`db_dump.sql`) that defines the database schema and data structure for a business-related application.

## Database Overview
The database consists of the following tables:

1. **customers** - Stores customer details.
2. **date** - Contains date-related information for transactions.
3. **markets** - Stores market or location data.
4. **products** - Holds product details such as name, category, and price.
5. **transactions** - Records purchase or sales transactions.

## Setup Instructions
### Importing the Database
To import the SQL dump into MySQL, use the following command:
```bash
mysql -u your_username -p your_database_name < db_dump.sql
```
Replace `your_username` and `your_database_name` with your actual MySQL credentials.

### Using the Database
After importing, you can check the tables using:
```sql
SHOW TABLES;
```
To view the structure of a table:
```sql
DESCRIBE customers;
```

## Example Queries
- Fetch all customer records:
```sql
SELECT * FROM customers;
```
- Get total sales per product:
```sql
SELECT product_id, SUM(amount) AS total_sales FROM transactions GROUP BY product_id;
```
- Retrieve the top 5 markets by transactions:
```sql
SELECT market_id, COUNT(*) AS total_transactions FROM transactions GROUP BY market_id ORDER BY total_transactions DESC LIMIT 5;
```

## Contributing
Feel free to submit issues or pull requests to improve this database schema.
