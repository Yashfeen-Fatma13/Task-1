# Task-1
Cleaned Data set
This repository contains a cleaned Excel dataset originally created for data cleaning practice.

## Dataset Overview

- *File Name*: cleaned_customer_data.xlsx
- *Total Rows*: 12 (excluding header)
- *Total Columns*: 7

## Columns Description

| Column Name   | Description                                      | Data Type |
|---------------|--------------------------------------------------|-----------|
| customer_id   | Unique ID for each customer                      | Integer   |
| name          | Customer's full name (title-cased)               | Text      |
| email         | Cleaned, standardized email addresses            | Text      |
| phone_number  | Digits only, no formatting symbols               | Text      |
| join_date     | Formatted as dd-mm-yyyy, blank if missing      | Date/Text |
| country       | Standardized (e.g., “USA”, “United States”)      | Text      |
| gender        | Standardized text ("Male", "Female")             | Text      |

## Cleaning Steps Performed

- Handled missing values (left blank where appropriate).
- Removed duplicate records.
- Standardized column headers (lowercase, no spaces).
- Reformatted dates to dd-mm-yyyy.
- Here's a step-by-step summary of data cleaning tasks in Excel:


---

1. Identify and Handle Missing Values

How to Check:

Apply filters to columns: Go to Data > Filter, then look for blanks.

Or use Conditional Formatting > Highlight Cells > Blanks.


How to Fix:

Fill manually or with a formula (e.g., =IF(A2="", "Unknown", A2)).

Or delete rows with missing values if needed.




---

2. Remove Duplicate Rows

Steps:

1. Select your data range.


2. Go to Data > Remove Duplicates.


3. Choose the columns to check for duplicates and click OK.





---

3. Standardize Text Values (e.g., Gender, Country Names)

Steps:

Use LOWER(A2) to make text lowercase.

Use SUBSTITUTE(A2, " ", "_") to replace spaces with underscores.

Use TRIM(A2) to remove extra spaces.

For mapping (e.g., "M" to "Male"), use VLOOKUP() with a reference table.




---

4. Convert Date Formats to Consistent Format (e.g., dd-mm-yyyy)

Steps:

1. Select the date column.


2. Right-click > Format Cells > Custom.


3. Enter dd-mm-yyyy as the format.



If dates are stored as text, use:


=TEXT(DATEVALUE(A2), "dd-mm-yyyy")


---

5. Rename Column Headers to Be Clean and Uniform

Steps:

Use this formula to create clean headers:



=LOWER(SUBSTITUTE(A1, " ", "_"))

Copy and paste the cleaned row over the original headers (use Paste Values).



---

6. Check and Fix Data Types

Age as Integer:

Use =INT(A2) to get only the integer part.

Format cells: Home > Number Format > Number, set decimals to 0.


Date as Date:

Format cells: Home > Number Format > Short Date or Custom > dd-mm-yyyy.

If stored as text, convert using:



=DATEVALUE(A2)

- Cleaned phone numbers to contain only digits.
- Standardized text values for gender and country fields.
