# Cinema-Ticket-Sales-Data-Cleaning-Analysis
## Project Overview
* This project focuses on cleaning, validating, and analyzing a real-world cinema ticket sales dataset containing 10,000+ records.
* The dataset contained multiple data quality issues such as missing values, duplicate records, invalid entries, inconsistent formats, and incorrect calculations.
* The objective of this project was to transform raw, unstructured data into a clean, reliable, and analysis-ready dataset using Python and Pandas
## Raw Uncleaned Dataset
<a href="https://github.com/SUNIL-RAJ-07/Cinema-Ticket-Sales-Data-Cleaning-Analysis/blob/main/cinema_ticket_sales_uncleaned.csv">Dataset</a>
## Data Cleaning Process
The project was completed in structured stages:
## Data Exploration
* Used df.info(), df.head(), and df.describe() to understand structure and data types.
* Identified missing values and inconsistent formats.
## Handling Missing & Duplicate Values
* Removed duplicate records using:
  * Order_ID
  * Booking_ID
  * Customer_ID
  * Filled missing values using business logic:
  * Customer_Name → "Unknown"
  * Email → default placeholder
  * Feedback_Score → median per movie
  * Seat_Type → "Regular"
## Fixing Invalid & Outlier Values
* Removed rows with:
 * Negative or zero Price
 * Invalid Quantity
 * Incorrect Discount values
 * Corrected inconsistent text formatting (e.g., payment modes, seat types).
 * Standardized casing and removed whitespace.
 * Converted and validated date columns.
 * Ensured Booking_Date was not after Show_Date.
## Feature Engineering
* Created new analytical columns:
 * Net_Amount → Adjusted revenue after discount
 * Booking_Lag → Days between booking and show
 * Revenue_Category → Low / Medium / High revenue
 * Customer_Type → New vs Returning
 * Is_Weekend_Show → Weekend indicator
 * Encoded categorical variables numerically
## Data Validation
* Validated revenue calculations:
 * Checked if Total_Amount matched Price × Quantity × Discount
 * Detected outliers using IQR method.
 * Replaced blank/whitespace cells with NaN.
 * Verified missing values using df.isna().sum().
## Aggregation & Analysis
* Performed group-based analysis to extract insights:
 * Top 5 movies by total revenue
 * Top performing theatres
 * Highest revenue cities
 * Most used payment methods
 * Customers with highest spending
 * Average feedback score per movie
# Cleaned Dataset
<a href="https://github.com/SUNIL-RAJ-07/Cinema-Ticket-Sales-Data-Cleaning-Analysis/blob/main/cleaned_file.xlsx">Dataset</a>
## Project Insights
* Identified high-revenue movies and top-performing theatres.
* Observed customer behavior patterns including repeat bookings.
* Weekend shows contributed significantly to revenue.
* Data cleaning significantly improved reporting accuracy.
* Validation checks revealed inconsistencies in calculated totals before cleaning.
## Final Conclusion
* This project demonstrates the importance of data cleaning before performing analysis.
* By systematically handling missing values, removing duplicates, validating calculations, and engineering new features, the dataset was transformed into a reliable, analysis-ready format.
* The cleaned dataset can now be confidently used for reporting, visualization, and business decision-making.
