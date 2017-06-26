1)##Retrieving Transportation Report Data
The logistics manager at AdventureWorks has asked you to generate some reports containing details of the company's customers to help reduce transportation costs. For starters, you need to produce a list of all of your customers' locations.
##Finish the Transact-SQL query that returns the Address table and retrieves all values for City and StateProvince, without duplicates.

SELECT  DISTINCT City, StateProvince
FROM SalesLT.Address;

2)##Retrieving Transportation Report Data (2)
You are being told that transportation costs are increasing and you need to identify the heaviest products.
##Finish the query to retrieve the names of the top ten percent of products by weight.

SELECT TOP 10 PERCENT Weight, ProductID, Name
FROM SalesLT.Product
ORDER BY Weight DESC;

3)##Retrieving Transportation Report Data (3)
The ten heaviest products are transported by a specialist carrier.
##Tweak the query to list the heaviest 100 products not including the ten most heavy ones.

SELECT Weight, ProductID, Name
FROM SalesLT.Product
ORDER BY Weight DESC
OFFSET 10 ROWS FETCH NEXT 100 ROWS ONLY;

4)##Retrieving Product Data
The product manager at AdventureWorks would like you to create some reports listing details of the products that you sell.
##Write a query to find the names, colors, and sizes of the products with a product model ID of 1.

SELECT Name, Color, Size
FROM SalesLT.Product
WHERE ProductModelID = 1;

5)##Retrieving Product Data (2)
The product manager would like more information on products of certain colors and sizes.
##Retrieve the product number and name of the products that have a Color of 'Black', 'Red', or 'White' and a Size of 'S' or 'M'.

SELECT ProductNumber, Name, Color, Size
FROM SalesLT.Product
WHERE Color IN ('Black', 'Red', 'White') AND Size IN ('S', 'M');

6)##Retrieving Product Data (3)
The product manager would also like information on products with a particular product number prefix.
##Retrieve the product number, name, and list price of products that have a product number beginning with 'BK-'.

SELECT ProductNumber, Name, ListPrice
FROM SalesLT.Product
WHERE ProductNumber LIKE 'BK%';

7)Retrieving Product Data (4)
Finally, the product manager is interested in a slight variation of the last request regarding product numbers with a particular prefix.
Modify your previous query to retrieve the product number, name, and list price of products with product number beginning with 'BK-' followed by any character other than 'R', and ending with a '-' followed by any two numerals.
Remember:
to match any string of zero or more characters, use %
to match characters that are not R, use [^R]
to match a numeral, use [0-9]

SELECT ProductNumber, Name, ListPrice
FROM SalesLT.Product
WHERE ProductNumber LIKE 'BK-[^R]%-[0-9][0-9]';
