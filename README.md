## Dataset Used
- <a href="https://github.com/Dennisogaka/Distributor_Sales_Data_Analysis/blob/main/Excel_Assignment%20and%20Brief_Final.xlsx">Dataset<a/>
## Data Issues Found
-	There were duplicate order IDs
-	There were negative unitprices and discounts above 30%
-	There were blank city, salesperson, and channel cells.
-	Data types were incorrect (Dates, Numercs and Text)
-	Required Dates were earlier than the order Dates
## Cleaning Rules and Assumptions
-	A staging table was created by duplicating the raw data sheet to preserve data integrity. All steps were conducted on the staging table while keeping the original data unchanged.
-	Rows were considered duplicates if the Order ID was identical.
-	Negative unit prices were treated as data entry errors and corrected by finding and replacing them with positive values. 
-	Discounts above 30% were considered unusually high based on standard business practices and were capped at 30% to prevent distortion of revenue and margin calculations. These corrections ensured realistic pricing while preserving all valid transaction records.
-	The columns were formatted to the correct data type to eliminate Chart, formulas, and Pivot Tables breaking if the data types are wrong.
-	Orders with an earlier required date than the order date were corrected by resetting the RequiredDate to a reasonable lead time of seven days after the OrderDate through the use of an IF function and named the column "Correct_Required_Date". This ensured chronological consistency while maintaining realistic delivery expectations.

## Questions to Answer
-	Total Revenue
-	Gross Profit 
-	Margin % 
-	Avg Order Value
-	On-Time % (LeadTimeDays ≤ 7)
-	Revenue by Month (line chart).
-	Profit by Region and Channel (stacked column).
-	Top 10 SKUs by Revenue (bar).
-	Discount Outliers
-	Dynamic titles reflecting applied filters.
  ## Dashboard
  ![Dashboard_View](https://github.com/user-attachments/assets/25095ca4-b1db-459d-9888-53cb6140af74)

  
## Key Findings
-	Africa had the lowest delayed service delivery and on-time delivery, but also contributed the least in terms of order numbers.
-	On Average Americas has the cheapest cost of goods, therefore, a good region to consider for production. But if we were to consider the cheapest country, then Japan has the cheapest cost of goods on average.
-	Asia had the highest profit, and the direct channel contributed the highest percentage of this profit.
-	In terms of favorable sales channels, distributors are higher in Africa, direct in the Americas and Europe, and Retail in Asia.
-	Asia contributed a higher percentage of the discount totals offered across the regions.
-	2024 was the year when the cost of goods was high, but it also had higher profits.
