# Demonstrating Proficiency in SQL Database Management System
## Creating-and-Managing-a-Database-for-Manchester-United-Legends
## 1. Create the `Customers` Table

This SQL code defines the structure of a `Customers` table in a database. It will store information about customers, including their names, positions, contact details, and creation time.
```
CREATE TABLE Customers (
    customer_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    position VARCHAR(50) NOT NULL,
    date_of_birth DATE,
    email VARCHAR(100),
    phone_number VARCHAR(15),
    address VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
## 2. Create the `BankAccounts` table for customer bank accounts
```
CREATE TABLE BankAccounts (
    account_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    account_type ENUM('Checking', 'Savings', 'Business') NOT NULL,
    balance DECIMAL(15, 2) DEFAULT 0.00,
    account_status ENUM('Active', 'Inactive', 'Closed') DEFAULT 'Active',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```
## 3. Insert Manchester United Legends into the `Customers` table
```
INSERT INTO Customers (first_name, last_name, position, date_of_birth, email, phone_number, address)
VALUES
('Peter', 'Schmeichel', 'Goalkeeper', '1963-11-18', 'peter.schmeichel@manutd.com', '555-0001', '1 Old Trafford, Manchester'),
('Gary', 'Neville', 'Right Back', '1975-02-18', 'gary.neville@manutd.com', '555-0002', '2 Old Trafford, Manchester'),
('Denis', 'Irwin', 'Left Back', '1965-10-31', 'denis.irwin@manutd.com', '555-0003', '3 Old Trafford, Manchester'),
('Nemanja', 'Vidic', 'Center Back', '1981-09-21', 'nemanja.vidic@manutd.com', '555-0004', '4 Old Trafford, Manchester'),
('Rio', 'Ferdinand', 'Center Back', '1978-11-07', 'rio.ferdinand@manutd.com', '555-0005', '5 Old Trafford, Manchester'),
('David', 'Beckham', 'Right Midfielder', '1975-05-02', 'david.beckham@manutd.com', '555-0006', '6 Old Trafford, Manchester'),
('Ryan', 'Giggs', 'Left Midfielder', '1973-11-29', 'ryan.giggs@manutd.com', '555-0007', '7 Old Trafford, Manchester'),
('Roy', 'Keane', 'Central Midfielder', '1971-08-10', 'roy.keane@manutd.com', '555-0008', '8 Old Trafford, Manchester'),
('Paul', 'Scholes', 'Attacking Midfielder', '1974-11-16', 'paul.scholes@manutd.com', '555-0009', '9 Old Trafford, Manchester'),
('Eric', 'Cantona', 'Forward', '1966-05-24', 'eric.cantona@manutd.com', '555-0010', '10 Old Trafford, Manchester'),
('Wayne', 'Rooney', 'Striker', '1985-09-24', 'wayne.rooney@manutd.com', '555-0011', '11 Old Trafford, Manchester')
('Jaap', 'Stam', 'Center Back', '1972-07-17', 'jaap.stam@manutd.com', '555-0004', '4 Old Trafford, Manchester');
```
## 4. Insert corresponding bank account data into the `BankAccount` table
```
INSERT INTO BankAccount (customer_id, account_type, balance)
VALUES
(1, 'Checking', 20000.00),
(2, 'Savings', 15000.00),
(3, 'Checking', 18000.00),
(4, 'Business', 25000.00),
(5, 'Savings', 30000.00),
(6, 'Checking', 12000.00),
(7, 'Savings', 22000.00),
(8, 'Checking', 27000.00),
(9, 'Savings', 24000.00),
(10, 'Business', 32000.00),
(11, 'Checking', 19000.00)
(11, 'Checking', 15000.00);
```
## `Customers` Table - Manchester United Legends

| customer_id | first_name | last_name | position | date_of_birth | email | phone_number | address | created_at |
|---|---|---|---|---|---|---|---|---|
| 1 | Peter | Schmeichel | Goalkeeper | 1963-11-18 | peter.schmeichel@manutd.com | 555-0001 | 1 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 2 | Gary | Neville | Right Back | 1975-02-18 | gary.neville@manutd.com | 555-0002 | 2 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 3 | Denis | Irwin | Left Back | 1965-10-31 | denis.irwin@manutd.com | 555-0003 | 3 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 4 | Nemanja | Vidic | Center Back | 1981-09-21 | nemanja.vidic@manutd.com | 555-0004 | 4 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 5 | Rio | Ferdinand | Center Back | 1978-11-07 | rio.ferdinand@manutd.com | 555-0005 | 5 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 6 | David | Beckham | Right Midfielder | 1975-05-02 | david.beckham@manutd.com | 555-0006 | 6 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 7 | Ryan | Giggs | Left Midfielder | 1973-11-29 | ryan.giggs@manutd.com | 555-0007 | 7 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 8 | Roy | Keane | Central Midfielder | 1971-08-10 | roy.keane@manutd.com | 555-0008 | 8 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 9 | Paul | Scholes | Attacking Midfielder | 1974-11-16 | paul.scholes@manutd.com | 555-0009 | 9 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 10 | Eric | Cantona | Forward | 1966-05-24 | eric.cantona@manutd.com | 555-0010 | 10 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 11 | Wayne | Rooney | Striker | 1985-09-24 | wayne.rooney@manutd.com | 555-0011 | 11 Old Trafford, Manchester | 2024-09-07 20:25:51 |
| 12 | Jaap | Stam | Center Back | 1972-07-17 | jaap.stam@manutd.com | 555-0004 | 4 Old Trafford, Manchester | 2024-09-07 20:32:38 |

## `BankAccounts` Table - Manchester United Legends

| account_id | customer_id | account_type | balance   | created_at           |
|------------|-------------|--------------|-----------|----------------------|
| 1          | 1           | Checking     | 20000.00  | 2024-09-07 20:25:51  |
| 2          | 2           | Savings      | 15000.00  | 2024-09-07 20:25:51  |
| 3          | 3           | Checking     | 18000.00  | 2024-09-07 20:25:51  |
| 4          | 4           | Business     | 25000.00  | 2024-09-07 20:25:51  |
| 5          | 5           | Savings      | 30000.00  | 2024-09-07 20:25:51  |
| 6          | 6           | Checking     | 12000.00  | 2024-09-07 20:25:51  |
| 7          | 7           | Savings      | 22000.00  | 2024-09-07 20:25:51  |
| 8          | 8           | Checking     | 27000.00  | 2024-09-07 20:25:51  |
| 9          | 9           | Savings      | 24000.00  | 2024-09-07 20:25:51  |
| 10         | 10          | Business     | 32000.00  | 2024-09-07 20:25:51  |
| 11         | 11          | Checking     | 19000.00  | 2024-09-07 20:25:51  |
| 12         | 12          | Checking     | 20000.00  | 2024-09-07 20:34:28  |


## 5. Rename the tables for consistency (if needed)
```
RENAME TABLE Customers TO customers;
RENAME TABLE BankAccounts TO bank_accounts;
```
## 6. Update David Beckham's email and increase his account balance by 5000.00
```
UPDATE customers
SET email = 'beckham.legend@manutd.com'
WHERE first_name = 'David' AND last_name = 'Beckham';
```
| customer_id | first_name | last_name | position | date_of_birth | email | phone_number | address | created_at |
|---|---|---|---|---|---|---|---|---|
| 6 | David | Beckham | Right Midfielder | 1975-05-02 | beckham.legend@manutd.com | 555-0006 | 6 Old Trafford, Manchester | 2024-09-07 20:25:51 |
```
UPDATE bank_accounts
SET balance = balance + 5000.00
WHERE customer_id = 
    (SELECT customer_id FROM customers WHERE first_name = 'David' AND last_name = 'Beckham');
```
| account_id | customer_id | account_type | balance | created_at |
|---|---|---|---|---|
| 6 | 6 | Checking | 17000 | 2024-09-07 20:25:51 |

## 7. Add a new column `account_status` to the `bank_accounts` table
```
ALTER TABLE bank_accounts
ADD COLUMN account_status ENUM('Active', 'Inactive', 'Closed') DEFAULT 'Active';
```
## 8. Delete Jaap Stam's customer and bank account records (assuming he exists)
```
DELETE FROM bank_accounts
WHERE customer_id = 
    (SELECT customer_id FROM customers WHERE first_name = 'Jaap' AND last_name = 'Stam');

DELETE FROM customers
WHERE first_name = 'Jaap' AND last_name = 'Stam';
```
## 9. Drop the `bank_accounts` table if no longer needed
```
DROP TABLE IF EXISTS bank_accounts;
```
## 10. Truncate the `bank_accounts` table (removes all data but keeps the table structure)
```
TRUNCATE TABLE bank_accounts;
```


























