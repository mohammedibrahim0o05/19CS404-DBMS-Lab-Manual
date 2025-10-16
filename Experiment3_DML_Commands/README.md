# Experiment 3: DML Commands

## Name: MOHAMMED IBRAHIM MN 
## Reg.no:212223100034

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**

Write a SQL statement to update the product_name as 'Grapefruit' whose product_id is 4 in the products table.
```
update products
set product_name='Grapefruit'
where product_id=4;
```
**Output:**

![image](https://github.com/user-attachments/assets/f7cb35b7-e15c-4d6d-be26-695316a2752f)

**Question 2**

Write a SQL query to reduce the reorder level by 30% where cost price is more than 50 and quantity in stock is less than 100 in the products table.
```
update Products
set reorder_lvl=reorder_lvl*0.7
where cost_price>50 and quantity<100;
```
**Output:**

![image](https://github.com/user-attachments/assets/be6557eb-cca2-408a-ba08-390d6e796285)

**Question 3**

Write a SQL query to Delete a Specific Surgery which was made on 28th Feb 2024.
```
delete from Surgeries 
where surgery_date='2024-02-28';
```
**Output:**

![image](https://github.com/user-attachments/assets/10904988-223a-42e7-94ca-3b48b01b9c31)

**Question 4**

Write a SQL query to Delete customers from 'customer' table where 'GRADE' is not equal to 3.
```
delete from customer
where GRADE!=3;
```
**Output:**

![image](https://github.com/user-attachments/assets/79285c8a-2978-407d-82ba-b3c2cdb69272)

**Question 5**

Write a query to fetch details of employees whose EmpLname ends with an alphabet ‘A’ and contains five alphabets.
```
select * from EmployeeInfo 
where EmpLname like '%A' and length(EmpLname)=5;
```
**Output:**

![image](https://github.com/user-attachments/assets/821d1823-0fea-438e-9709-d82220eea49a)

**Question 6**

Write a SQL query to classify base in the Calculations table as 'Provided' if it is not NULL, otherwise 'Not Provided'.
```
select id,base,
case when base is not NULL then 'Provided'
else 'Not Provided'
end as base_status
from Calculations;
```
Thus, the SQL queries to implement DML commands have been executed successfully.
