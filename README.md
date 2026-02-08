  🛒 RETAIL SALES ANALYTICS USING SQL JOINS AND WINDOW FUNCTIONS

📋 PROJECT OVERVIWE

For this project, I worked on analyzing retail sales data using SQL JOINs and window functions. The main goal was to understand the raw data and turn it into useful insights for the company. This includes seeing which customers are buying the most, tracking product performance, and noticing sales trends over time.
I implemented everything using PostgreSQL. During the project, I applied database design ideas and ran SQL queries to simulate a real business scenario.

🏢 BUSINESS CONTEXT

Retail companies collect lots of information from customers buying products in different regions. Just having raw data doesn’t automatically help them make decisions. Proper analysis is needed to see which customers are valuable, which products sell well, and how sales trends change over time.
In this project, I focused on helping the company identify top customers, track product performance, and understand sales patterns. The analysis is meant to help with marketing campaigns, inventory planning, and keeping customers engaged.

⚠️ DATA CHALLENGE

The company stores transactions involving customers, products, and orders. One challenge is that this data is split across multiple tables, which makes it hard to analyze without joining them properly.
Another challenge is finding patterns like top-selling products, customer purchase habits, and month-to-month sales changes. Without the right queries, it’s difficult to make decisions based on this data.

🎯 EXPECTED OUTCOME

The goal of the project was to identify the best-performing products, analyze how customers make purchases, and track sales trends. The results should help the business plan marketing campaigns, improve product strategies, and increase overall performance.

✅ SUCCESS CRITERIA

I measured the success of this project using five main goals:

🥇 Identify top customers based on total spending using ranking window functions.

📈 Calculate running monthly sales totals using aggregate window functions.

🔄 Measure month-to-month sales growth using navigation window functions.

📊 Segment customers into four groups based on spending using distribution window functions.

📅 Calculate three-month moving average sales to see long-term trends.

🗄 DATABASE SCHEMA DESIGN

The database has four related tables to simulate a realistic retail sales system. I focused on keeping the structure normalized and linking the tables properly.

👥 CUSTOMERS TABLE

Stores customer info like customer ID, name, email, region, and registration date. Each customer has a unique ID.

🛍 PRODUCTS TABLE

Stores product details like product name, category, and price. Each product has a unique ID.

🧾 ORDERS TABLE

Keeps track of purchase transactions. Each order links to a customer, and one customer can place many orders.

📦 ORDER_ITEMS TABLE

Records the products included in each order. It links to both orders and products and includes quantity and total cost.

🔗 SQL JOIN IMPLEMENTATIONS

I used JOIN operations to combine data from multiple tables and get useful insights.

🔹 INNER JOIN 🟢

Used to get valid transaction records including customers, products, and orders. Shows which sales actually happened.

🔹 LEFT JOIN 🟡

Used to find customers who haven’t placed any orders. Helps plan marketing campaigns for inactive customers.

🔹 RIGHT JOIN / FULL OUTER JOIN 🔵

Used to detect products with no sales. Also helps compare matched and unmatched records across tables.

🔹 SELF JOIN 🟣

Used to compare customers in the same region. Helps spot patterns and distribution in specific areas.

📊 WINDOW FUNCTIONS IMPLEMENTATIONS

Window functions allowed me to do calculations that regular queries can’t easily do.

🥇 RRANKING FUNCTIONS

ROW_NUMBER(), RANK(), DENSE_RANK(), PERCENT_RANK()
Used to find the top customers based on total spending. Helps identify loyal, high-value customers.

📈 AGGREGATE WINDOW FUNCTIONS

SUM(), AVG()
Used to calculate running monthly totals and moving averages. Helps track sales trends over time.

🔄 NAVIGATION FUNCTIONS

LAG(), LEAD()
Used to compare sales from one month to the next. Shows whether sales are increasing or decreasing.

📊 DISTRIBUTION FUNCTIONS

NTILE(), CUME_DIST()
Used to split customers into spending groups. Helps plan targeted marketing strategies.

📈 RESULTS ANALYTICS

🔹 Descriptive Analysis — What Happened?

I found that a small number of customers make up most of the total revenue. Sales also changed across months, probably due to promotions or seasonal effects. Dividing customers into spending groups showed clear differences between high and low spenders.

🔹 Diagnostic Analysis — Why Did It Happen?

The differences might be caused by loyalty, buying habits, or promotions. Some products had low or no sales, which could be a pricing or visibility issue. I also noticed some registered customers never made a purchase, showing low engagement.

🔹 Prescriptive Analysis — What Should Be Done?

The company should focus on keeping high-value customers with loyalty programs or personalized offers. Marketing should target inactive customers. Low-selling products should be reviewed for pricing or promotion adjustments. Tracking sales trends can also help with inventory planning.

🖼 ER DIAGRAM

The ER diagram shows how Customers, Orders, Order_Items, and Products are linked. It illustrates how customers place orders, how orders contain multiple products, and how products connect to transactions.

<img width="671" height="571" alt="Retail sales database ER diagram drawio" src="https://github.com/user-attachments/assets/4ca2c882-2f70-48b3-8623-4f5e56f2cfbe" />

💻 TECHNOLOGIES USED 

PostgreSQL

SQL

pgAdmin

Draw.io (ER Diagram Design)

GitHub (Version Control and Documentation)

📚 REFERENCES 

PostgreSQL Global Development Group. (2024). PostgreSQL Documentation. Retrieved from https://www.postgresql.org/docs/

Oracle Corporation. (2024). SQL Window Functions Documentation. Retrieved from https://docs.oracle.com/en/database/

Silberschatz, A., Korth, H., & Sudarshan, S. (2019). Database System Concepts (7th ed.). McGraw-Hill Education.

W3Schools. (2024). SQL JOIN Tutorial. Retrieved from https://www.w3schools.com/sql/

🛡 ACADEMIC INTEGRITY STATEMENT

All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.
