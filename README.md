# Scalar-Function-sql

CREATE TABLE products(
product_id INT PRIMARY KEY,
product_name VARCHAR(100),
category VARCHAR(50),
price DECIMAL(10, 2),
stock_quantity INT,
supplier_id INT
);
INSERT INTO products (product_id, product_name, category, price,
stock_quantity, supplier_id)
VALUES
(1, 'Laptop', 'Electronics', 75000, 10, 101),
(2, 'Smartphone', 'Electronics', 40000, 20, 102),
(3, 'Tablet', 'Electronics', 30000, 15, 103),
(4, 'Headphones', 'Electronics', 2000, 50, 104),
(5, 'Smartwatch', 'Electronics', 15000, 25, 105),
(6, 'Camera', 'Electronics', 55000, 5, 106),
(7, 'TV', 'Electronics', 60000, 7, 101),
(8, 'Refrigerator', 'Appliances', 45000, 12, 107),
(9, 'Microwave', 'Appliances', 10000, 20, 108),
(10, 'Washing Machine', 'Appliances', 35000, 10, 109),
(11, 'Air Conditioner', 'Appliances', 40000, 8, 110),
(12, 'Mixer Grinder', 'Appliances', 3000, 30, 111),
(13, 'Vacuum Cleaner', 'Appliances', 12000, 15, 112),
(14, 'Sofa Set', 'Furniture', 60000, 5, 113),
(15, 'Dining Table', 'Furniture', 45000, 8, 114),
(16, 'Bed', 'Furniture', 55000, 4, 115),
(17, 'Wardrobe', 'Furniture', 35000, 10, 116),
(18, 'Bookshelf', 'Furniture', 20000, 12, 117),
(19, 'Office Chair', 'Furniture', 10000, 25, 118),
(20, 'Desk', 'Furniture', 15000, 20, 119),
(21, 'Running Shoes', 'Clothing', 5000, 50, 120),
(22, 'Jacket', 'Clothing', 8000, 30, 121),
(23, 'T-Shirt', 'Clothing', 1000, 100, 122),
(24, 'Jeans', 'Clothing', 2000, 60, 123),
(25, 'Sunglasses', 'Accessories', 3000, 40, 124),
(26, 'Belt', 'Accessories', 1000, 80, 125),
(27, 'Wallet', 'Accessories', 1500, 70, 126),
(28, 'Watch', 'Accessories', 7000, 25, 127),
(29, 'Handbag', 'Accessories', 5000, 30, 128),
(30, 'Necklace', 'Accessories', 6000, 20, 129),
(31, 'Earrings', 'Accessories', 2000, 40, 130),
(32, 'Bicycle', 'Outdoor', 15000, 10, 131),
(33, 'Tent', 'Outdoor', 10000, 15, 132),
(34, 'Backpack', 'Outdoor', 5000, 25, 133),
(35, 'Sleeping Bag', 'Outdoor', 8000, 20, 134),
(36, 'Camping Stove', 'Outdoor', 3000, 30, 135),
(37, 'Helmet', 'Outdoor', 2500, 35, 136),
(38, 'Fishing Rod', 'Outdoor', 12000, 12, 137),
(39, 'Kayak', 'Outdoor', 25000, 5, 138),
(40, 'Golf Clubs', 'Outdoor', 40000, 8, 139),
(41, 'Football', 'Sports', 1000, 50, 140),
(42, 'Basketball', 'Sports', 1500, 40, 141),
(43, 'Tennis Racket', 'Sports', 5000, 20, 142),
(44, 'Cricket Bat', 'Sports', 3000, 30, 143),
(45, 'Dumbbells', 'Sports', 2000, 25, 144),
(46, 'Treadmill', 'Sports', 35000, 5, 145),
(47, 'Yoga Mat', 'Sports', 1000, 50, 146),
(48, 'Protein Powder', 'Sports', 5000, 30, 147),
(49, 'Bicycle Helmet', 'Outdoor', 3000, 35, 148),
(50, 'Kayaking Paddle', 'Outdoor', 5000, 20, 149);
Questions and Answers Using Scalar Functions
1. Retrieve the product names in uppercase.
SELECT UPPER(product_name) AS product_name_upper FROM
products;
2. Find the length of each product name.
SELECT product_name, LENGTH(product_name) AS name_length
FROM products;
3. Concatenate the category and product name with a hyphen.
SELECT CONCAT(category,' - ', product_name) AS
category_product FROM products;
4. Round the price of each product to the nearest integer.
 SELECT product_name, ROUND(price) AS rounded_price
 FROM products;
5. Return the first 3 characters of each product name.
SELECT LEFT(product_name, 3) AS product_name_prefix
 FROM products;
6. Display the price with two decimal places using FORMAT.
SELECT product_name, FORMAT(price, 2) AS formatted_price
 FROM products;
7. Find products with 'Bike' in their name using LOCATE.
SELECT product_name FROM products WHERE LOCATE('Bike',
product_name) > 0;
8. Replace 'Bike' with 'Cycle' in product names.
SELECT REPLACE(product_name, 'Bike', 'Cycle') AS
updated_name FROM products;
9. Find the ASCII value of the first character of each product name.
SELECT product_name, ASCII(LEFT(product_name, 1)) AS
ascii_value FROM products;
10.Trim spaces from the beginning and end of the product names.
SELECT TRIM(product_name) AS trimmed_name FROM products;
11. Convert the product names to lowercase.
SELECT LOWER(product_name) AS product_name_lower FROM
products;
12.Find the position of the first occurrence of 'a' in product names.
SELECT product_name, LOCATE('a', product_name) AS
position_of_a FROM products;
13.Find the product with the highest price using MAX.
SELECT MAX(price) AS highest_price FROM products;
14.Find the product with the lowest stock quantity using MIN.
SELECT MIN(stock_quantity) AS lowest_stock FROM products;
15.Calculate the total stock quantity across all products using SUM.
SELECT SUM(stock_quantity) AS total_stock FROM products;
16.Get the average price of products using AVG.
SELECT AVG(price) AS average_price FROM products;
17.Find the number of products in the table using COUNT.
SELECT COUNT(product_id) AS total_products FROM products;
18.Display the price of each product rounded down to the nearest integer
using FLOOR.
SELECT product_name, FLOOR(price) AS price_floor FROM
products;
19.Display the price of each product rounded up to the nearest integer
using CEIL.
SELECT product_name, CEIL(price) AS price_ceil FROM
products;
20.Generate a random number for each product using RAND.
SELECT product_name, RAND() AS random_number FROM
products;
21.Find the length of the category name for each product.
SELECT category, LENGTH(category) AS category_length FROM
products;
22.Find products whose category names start with the letter 'C'.
SELECT product_name FROM products WHERE LEFT(category, 1)
= 'C';
23.Extract the numeric part from the price by removing the decimal point
using CAST.
SELECT product_name, CAST(price AS UNSIGNED) AS
price_integer FROM products;
24.Return the day part of the current date using DAY.
SELECT DAY(CURDATE()) AS current_day;
25.Return the current date and time using NOW.
SELECT NOW() AS current_date_time;
26.Find the week number of the current date using WEEK.
SELECT WEEK(CURDATE()) AS current_week_number;
27.Convert the price to a string using CAST.
SELECT product_name, CAST(price AS CHAR) AS price_string
FROM products;
28.Check if the product name is NULL using IFNULL.
SELECT IFNULL(product_name, 'Unknown') AS product_name
FROM products;
29.Find the square root of the price for each product using SQRT.
SELECT product_name, SQRT(price) AS price_sqrt FROM
products;
30.Display the product names reversed using REVERSE.
SELECT REVERSE(product_name) AS reversed_name FROM
products;
31.Get the month part of the current date using MONTH.
SELECT MONTH(CURDATE()) AS current_month;
32.Display the sine of the price for each product using SIN.
SELECT product_name, SIN(price) AS price_sine FROM
products;
33.Show only 5 characters from the right side of the product names using
RIGHT.
SELECT RIGHT(product_name, 5) AS last_five_characters
FROM products;
34.Round the price of each product to the nearest multiple of 100 using
ROUND.
SELECT product_name, ROUND(price, -2) AS
price_rounded_to_hundred FROM products;
35.Display the natural logarithm of the product prices using LN.
SELECT product_name, LN(price) AS price_ln FROM products;
36.Return the absolute value of the stock quantity using ABS.
SELECT product_name, ABS(stock_quantity) AS
absolute_stock FROM products;
37.Generate a unique identifier for each product using UUID.
SELECT product_name, UUID() AS unique_identifier FROM
products;
38.Display the prices of products multiplied by 1.1 (assuming a 10% price
increase).
SELECT product_name, price * 1.1 AS new_price FROM
products;
39.Return the name of the weekday for the current date using DAYNAME.
SELECT DAYNAME(CURDATE()) AS day_name;
40.Get the hour part of the current time using HOUR.
SELECT HOUR(NOW()) AS current_hour;
These questions focus on scalar functions like UPPER(), LOWER(), CONCAT(),
LENGTH(), ROUND(), FORMAT(), mathematical functions like FLOOR(), CEIL(),
ABS(), LN(), and date/time functions like NOW(), DAY(), WEEK(), etc.
