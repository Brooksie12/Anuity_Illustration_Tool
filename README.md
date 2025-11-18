# Annuity Illustration Tool

## Description
An introductory project in financial modelling, data automation, and VBA macro development.

This tool converts verbally described annuity products into an interactive calculator and visualization tool. Users can adjust plan details and age ranges to see annual payments, total payout amounts, and summary statistics. VBA macros then automate the process of applying these calculations to an entire block of business, eliminating hours of manual calculations and allowing batch processing of customer records. Finally, graphs are generated for high-level business insights and reporting.

## Features
- Interactive user-driven annuity calculator based on plan parameters and age ranges
- VBA macros for automated batch processing of customer records
- Automated output of total and annual plan values
- Summary metrics and grouped results by plan type
- Basic graphs for business visualization and reporting

## Installation / Setup
1. Download the Excel workbook
2. Open in:
   - **Microsoft Excel** (required for full VBA functionality)
   - Google Sheets / Excel Online *(view only – VBA functionality will not work)*

## Structure
**File:** `Annuity_Illustration_Tool.xlsx`  
Contains **5 sheets:**

### 1. Calculator
- Implements core annuity calculations based on:
  - Plan type (`B7`)
  - Start age (`B9`)
  - End age (`B11`)
- Outputs:
  - Annual payment schedules
  - Total and average payments
  - Tabular illustration for stakeholders

### 2. Block of Business
- Contains raw plan and customer data for batch processing
- Represents plans already sold or proposed

### 3. Data
- VBA macros pull data from *Block of Business* through the calculator and output results here
- Includes **3 macros:**
  - `CalculateData` — runs all customers through the calculator and fills columns A:D
  - `SumByPlan` — groups amounts by plan (row G)
  - `PlanYearDataPayment` — computes annual expense to company (table beginning at column J)

### 4. Graphs
- Visual summaries of company-level metrics based on the output in *Data*

### 5. Plan Descriptions
- Original text definitions of annuity plans used as the basis for calculator logic

## References
Dataset provided by the Actuarial Accelerator community for educational purposes only.
