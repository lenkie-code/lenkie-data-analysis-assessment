# Lenkie SQL Assessment

Lenkie allows customers to make payments to their suppliers through our dashboard. Customers have multiple payment options, for this assessment, analyse the dataset provided to you that contains payments processed using our Credit Facility product. 


### Credit Facility

A Credit Facility is a line of credit that is made available to customers. Customers draw funds from the Credit Facility and pay their suppliers. Once payment is made, a loan is created by Lenkie with agreed upon payment dates.

### Dataset

The dataset is an SQL view that has the following columns:

#### Customer Columns
- Customer Id: A unique identifier of the customer which made a payment

#### Bill Columns

- Bill Id: A unique identifier of the bill which the customer made payment on
- Bill Amount: The bill amount paid by the customer to the supplier
- Bill Currency: The currency of the bill (One of GBP, USD, EUR)

#### Loan Columns
- Loan Origination Date: The [ISO8601](https://en.wikipedia.org/wiki/ISO_8601) date on which the loan was issued to the customer
- Fee: The loan fee

#### Repayment Columns
- Repayment Id: A unique identifier of a repayment that is either paid | pending | overdue
- Repayment Amount: The repayment amount, includes the loan fee
- Principal Repaid: The repayment amount, exclusive of the fee
- Due Date: The date the repayment was / is due
- Payment Date: the date the repayment was made
- Repayment Status: The status of the repayment, one of:
  - Not Paid: Repayment is not yet due 
  - Scheduled: Repayment is due and has been scheduled for collection
  - Paid: Repayment has been collected
  - Failed: Repayment was not collected successfully
 

# Questions

Given this data set, write SQL queries that answer the following questions:
--

1. List all unique customer names from the dataset
2. What is the total number of loans originated
3. Find the total loan amount (`Bill Amount`) for each customer
4. What is the average `Repayment Amount (GBP) (Principal)` per loan
5. Which loans were originated in the year 2023
6. Find the number of repayments due each month
7. Which customer has the highest total repayment amount
8. Generate a monthly report that shows the total number of loans, total loan amount and average loan amount per month

Bonus
--

- Write a SQL query to create a pivot table showing the total repayment amount per customer per month
- Write a SQL query to categorise loans into `Small`, `Medium` and `Large` based on the `Bill Amount`. You can define the thresholds


