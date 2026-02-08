🛒 RETAIL SALES ANALYTICS USING SQL JOINS AND WINDOW FUNCTIONS

📋 PROJECT OVERVIEW

For this project, I analyzed retail sales data using SQL JOINs and window functions. The main goal was to turn raw transactional data into meaningful business insights to support decision-making in marketing, inventory management, and customer relationship management.

Implementation was done in PostgreSQL. I applied relational database design concepts and ran analytical queries to simulate a real business scenario.

🏢 BUSINESS CONTEXT

Retail companies collect large amounts of data from customers buying products in different regions. Having raw data alone doesn’t automatically help decision-making. Proper analysis is needed to:

Identify top customers

Track product performance

Understand sales trends over time

This project focused on providing insights that help with marketing strategies, inventory planning, and customer retention.

⚠️ DATA CHALLENGE

The company’s transactional data is stored across multiple tables (customers, products, orders, order_items).

Challenges include:

Combining multiple tables for analysis

Identifying top-selling products

Tracking customer purchase behavior

Monitoring month-to-month sales trends

🎯 EXPECTED OUTCOME

The project aims to:

Identify high-performing products

Analyze customer purchasing behavior

Track sales trends over time

Provide insights for marketing campaigns and inventory planning

✅ SUCCESS CRITERIA

I measured success using five analytical goals:

🥇 Identify top customers by total spending (Ranking Functions)

📈 Calculate running monthly sales totals (Aggregate Functions)

🔄 Measure month-to-month sales growth (Navigation Functions)

📊 Segment customers into spending groups (Distribution Functions)

📅 Calculate three-month moving average sales trends

🗄 DATABASE SCHEMA DESIGN

The database uses four related tables to simulate a realistic retail sales system, with normalized structure and proper primary/foreign key relationships.

🖼 ER Diagram – Shows relationships between Customers, Orders, Order_Items, Products

<img width="671" height="571" alt="Retail sales database ER diagram drawio" src="https://github.com/user-attachments/assets/e708be1e-3307-4832-8440-1ed49789973b" />

















🔗 PART A — SQL JOIN IMPLEMENTATION

Purpose: Combine multiple tables to generate meaningful business insights.

INNER JOIN – Retrieves completed transactions involving valid customers and products.

<img width="1361" height="762" alt="Screenshot 2026-02-08 121327" src="https://github.com/user-attachments/assets/53b5c552-dec9-484f-b53b-f66d95c41ce0" />


LEFT JOIN – Identifies customers who have never placed an order.

<img width="1365" height="767" alt="Screenshot 2026-02-08 141054" src="https://github.com/user-attachments/assets/d056fc82-af5d-4d0f-9868-693fa3f92c6e" />


RIGHT JOIN / FULL OUTER JOIN – Detects products with no sales activity.

<img width="1365" height="767" alt="Screenshot 2026-02-08 141213" src="https://github.com/user-attachments/assets/77675e7d-4688-4e5e-af98-b8a040248941" />



SELF JOIN – Compares customers within the same region.

<img width="1365" height="767" alt="Screenshot 2026-02-08 141331" src="https://github.com/user-attachments/assets/78150547-866b-4739-9fa7-15defb60b537" />
















📊 PART B — WINDOW FUNCTIONS IMPLEMENTATION

Purpose: Perform advanced analytical calculations that regular aggregation cannot easily achieve.

Ranking Functions (ROW_NUMBER, RANK, DENSE_RANK, PERCENT_RANK) – Identify top customers by total spending.

<img width="1365" height="767" alt="Screenshot 2026-02-08 141703" src="https://github.com/user-attachments/assets/4d2a5024-72fd-4877-b704-d2cfd2f65eb7" />


Aggregate Functions (SUM, AVG with ROWS/RANGE) – Calculate running monthly totals and moving averages.

<img width="1365" height="767" alt="Screenshot 2026-02-08 141741" src="https://github.com/user-attachments/assets/5d18f60e-b177-444e-a7a4-44f4ede09677" />


Navigation Functions (LAG, LEAD) – Compare sales month-to-month to detect growth or decline.

<img width="1355" height="754" alt="Screenshot 2026-02-08 141813" src="https://github.com/user-attachments/assets/f737431d-7a7c-4442-bc99-b97c7768d5c3" />


Distribution Functions (NTILE, CUME_DIST) – Segment customers into spending groups for targeted marketing.

 <img width="1365" height="767" alt="Screenshot 2026-02-08 141838" src="https://github.com/user-attachments/assets/075a284e-02ec-4b9f-a647-488182a719e3" />


📈 RESULTS ANALYSIS

Descriptive Analysis — WHAT HAPPENED?
Small number of customers contributed most revenue; sales varied across months; clear differences between high and low spenders.


Diagnostic Analysis — WHY DID IT HAPPENED?
Differences caused by loyalty, buying habits, promotions, low sales products, and inactive customers.



Prescriptive Analysis — WHAT SHOULD BE DONE?
Focus on loyalty programs, personalized promotions, target inactive customers, review low-selling products, and improve inventory planning.






💻 TECHNOLOGIES USED

PostgreSQL
SQL
pgAdmin
Draw.io (ER Diagram Design)
GitHub (Version Control and Documentation)



📚 REFERENCES

PostgreSQL Global Development Group. PostgreSQL Documentation. https://www.postgresql.org/docs/

Oracle Corporation. SQL Window Functions Documentation. https://docs.oracle.com/en/database/

Silberschatz, A., Korth, H., & Sudarshan, S. Database System Concepts, 7th ed., McGraw-Hill

W3Schools. SQL JOIN Tutorial. https://www.w3schools.com/sql/




🛡 ACADEMIC INTEGRITY STATEMENT

All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.
