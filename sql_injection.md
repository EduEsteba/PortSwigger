# SQL INJECTION

## LAB 1

This lab contains an SQL injection vulnerability in the product category filter. When the user selects a category, the application carries out an SQL query like the following:

SELECT * FROM products WHERE category = 'Gifts' AND released = 1
To solve the lab, perform an SQL injection attack that causes the application to display details of all products in any category, both released and unreleased.


SOLUTION
```
filter?category=%27+OR+1=1--
```


## LAB 2 

This lab contains an SQL injection vulnerability in the login function.

To solve the lab, perform an SQL injection attack that logs in to the application as the administrator user.

SOLUTION
```
' or 1=1 --
```
