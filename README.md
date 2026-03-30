🤖 RPA DAY 7 TASKS: UiPath – Extracting Invoice Data from PDF into Excel (String Manipulation)
📌 Overview

This repository contains a UiPath automation workflow designed to extract structured invoice data from a PDF file using OCR and string manipulation techniques, and export the extracted data into Excel.

The project focuses on handling unstructured invoice text without using regex, relying instead on conditional logic and string operations.

🧠 Concepts Covered

PDF data extraction using OCR

String manipulation techniques

Conditional statements (If conditions)

Looping using For Each

Data extraction from unstructured text

Data cleaning and validation

DataTable creation and usage

Excel automation (Write Range)

⚙️ Workflow Description

🔹 Step 1: Read PDF
Use OCR to extract the entire invoice content into text format

🔹 Step 2: Convert Text to Lines
Split the extracted text into multiple lines for easier processing

🔹 Step 3: Clean Data
Remove empty or unnecessary lines
Prepare the data for accurate extraction

🔹 Step 4: Extract Header Details

Using looping and conditions, extract:

Invoice Number

Customer Name

Email

Issue Date

Due Date

Extraction is based on identifying keywords like:

“Invoice No”
“@” (for email)
“+” (for mobile)
Date patterns

🔹 Step 5: Extract Item Details
Identify invoice item rows using patterns (presence of price symbol and structure)
Extract:

Description

Quantity

Price

Total

Store all items in a DataTable

🔹 Step 6: Store Data

Store header details in one DataTable

Store item details in another DataTable

🔹 Step 7: Write to Excel
Write header data into Header sheet
Write item data into Items sheet

🛠️ Implementation Details

Activities Used:

Read PDF With OCR

Assign

If Condition

For Each

Build Data Table

Add Data Row

Write Range

Message Box / Log Message

Data Types:

String

Array (String[])

Integer

DataTable

Key Techniques:

Keyword-based extraction

Pattern recognition using string methods

Data cleaning before processing

Avoiding index-based assumptions in OCR text

▶️ Execution

Run the workflow in UiPath Studio

Provide the invoice PDF as input

Output will be generated in Excel with:

Header details

Item details

⚠️ Notes

OCR output may not be perfectly structured → always clean data before processing

Avoid relying on fixed positions (like next line or previous line)

Ensure Excel file is closed before writing data

Use debugging tools to validate extracted values

👩‍💻 Author

Sarah Carlyn Jeba.S
