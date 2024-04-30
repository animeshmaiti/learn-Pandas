# MySql
In this section, we will learn how to use MySql with Python.In my case i am using WSL2 with Ubuntu 22.04.4 LTS. And i have installed MySql ver 14.14.
## Installation
To install MySql in Ubuntu, you can use the following command:
- step 1: install MySql
```bash
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service
```
- step 2: configure MySql
```bash
sudo mysql
```
```sql
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'new_password';
```
```sql
mysql> exit;
```
- step 3: restart MySql
```bash
sudo systemctl restart mysql.service
```
- step 4: check MySql status
```bash
sudo systemctl status mysql.service
```
## Connect to MySql
To connect to MySql, you can use the following command:
```bash
mysql -u root -p
or
sudo mysql -u root -p
```
## Create a Database
To create a database, you can use the following command:
```sql
mysql> CREATE DATABASE mydatabase;
```
## Create a Table
To create a table, you can use the following command:
```sql
mysql> USE mydatabase;
mysql> CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), phone VARCHAR(20));
mysql> SHOW TABLES;
mysql> DESCRIBE customers;
mysql>INSERT INTO customers (name, phone) VALUES
    ('Donald', '12345678'),
    ('Bill', '87654321'),
    ('Elon', '12348765');
mysql> SELECT * FROM customers;
mysql> DROP TABLE customers;
```
## Using Python
To use MySql with Python, you can use the following command:
- step 1: install pymysql, sqlalchemy
```bash
conda install pymysql
conda install sqlalchemy
```
rest of the code is in the python files