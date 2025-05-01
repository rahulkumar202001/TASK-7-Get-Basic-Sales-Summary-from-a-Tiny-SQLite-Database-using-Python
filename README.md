Task 7: Basic Sales Summary with SQLite & Python

Objective
To extract and visualize basic sales information using SQL inside Python by:
- Connecting to a SQLite database
- Running SQL queries to summarize sales
- Visualizing key metrics using bar and line charts

Tools Used
- SQLite3 (Python built-in)
- Pandas (for data manipulation)
- Matplotlib (for data visualization)
- Jupyter Notebook / Python Script

Dataset
A small in-memory dataset was used to simulate real-world sales transactions. The dataset contains:
- `id`: Transaction ID
- `date`: Sale date
- `product`: Product name
- `quantity`: Units sold
- `price`: Price per unit

SQL Queries Used

Sales Summary by Product
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
