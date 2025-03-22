# week4-DML-ASSIGNMENT
QUESTION 1
Retrieve the total payment amount for each payment date, sorted in descending order, and limited to the five most recent payment dates.
SELECT paymentDate, SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;

QUESTION 2
Find the average credit limit for each customer, grouped by customer name and country.
SELECT customerName, country, AVG(creditLimit) AS avg_credit_limit
FROM customers
GROUP BY customerName, country;

QUESTION 3
Compute the total price of products ordered, grouped by product code and quantity ordered.
SELECT productCode, quantityOrdered, SUM(quantityOrdered * priceEach) AS total_price
FROM orderdetails
GROUP BY productCode, quantityOrdered;

QUESTION 4
Find the highest payment amount for each check number.
SELECT checkNumber, MAX(amount) AS highest_payment
FROM payments
GROUP BY checkNumber;


