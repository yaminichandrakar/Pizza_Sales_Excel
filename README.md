# Pizza_Sales_Excel
I recently created an Excel report using a dataset from Kaggle — completely built on my own understanding of Excel so far. This project represents the starting point of my data journey, where I practiced skills like PivotTables, Power Query, Power Pivot, formulas, and basic charts to turn raw data into insights.

What excites me most is how much more there is to explore! 
📊 This is just the beginning — looking forward to leveling up further in Excel and beyond!

**Highlights of Important KPI's:-**
. Average order value
. Total revenue
. Avg pizza per order
. Total order 
. Total pizza sold
			
📈 Sales & Revenue Insights
What days and time do we tend to be busiest?			
Which pizza generates the highest total revenue?
What is the average order value (AOV)?
Which day of the week has the highest number of orders or revenue?
Are there seasonal or monthly trends in pizza sales?

🍕 Product Performance
How many pizzas are we making during peak periods?			
What are our best and worst-selling pizzas?	
Which pizza size (S, M, L, XL, XXL) is the most popular by quantity sold?
Which pizza category (Classic, Veggie, Supreme, Chicken) contributes the most to sales revenue?
What are the top 5 best-selling pizzas by quantity?
Which pizzas are rarely ordered and might be considered for removal or promotion?
What is the average selling price per pizza size or category? 

📊 Customer & Order Behavior
How many pizzas are typically ordered per transaction?
What is the distribution of order quantities (e.g., single pizza orders vs bulk)?
How often do large-size pizzas appear in large orders?
Are there specific categories more popular at certain times of the day?

		
I've created 5 Measures which is essential for report creation:-

1. average order value :-   **=SUM([total_price])/COUNT([order_details_id])**

2. AvgPizzasPerOrder :- **=AVERAGEX(
                                VALUES(Table1[order_id]),
                                    CALCULATE([sum_of_quantity])
                                                                 )**

3. OrderCount :- **=COUNTROWS(VALUES(Table1[order_id]))**

4. sum_of_quantity :- **=SUM([quantity])**

5. TotalOrderQuantity :- **=CALCULATE(SUM([quantity]), ALLEXCEPT(Table1, Table1[order_id]))**
