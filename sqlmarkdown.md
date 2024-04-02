Weather Observation Station 
![sql-Station.jpg](attachment:sql-Station.jpg)

1 /*Query a list of CITY and STATE from the STATION table.The STATION table is described as follows:
 */
 
SELECT CITY, STATE FROM STATION;
2/* Query all columns for all American cities in CITY with populations larger than 100,000. The CountryCode for America is USA. */
SELECT * FROM CITY WHERE COUNTRYCODE = "USA" AND POPULATION > 100000;
3 /* Query all columns for a city in CITY with the ID 1661. */
SELECT * FROM CITY WHERE ID = 1661; 
4 /*Query a list of CITY names from STATION with even ID numbers only. You may print the results in any order, but must exclude duplicates from your answer. */
SELECT DISTINCT CITY FROM STATION WHERE MOD(ID,2)=0 ORDER BY CITY ASC; 
5 /* query the number of non-unique CITY names in STATION by subtracting the number of unique CITY entries in the table from the total number of CITY entries in the table. */
SELECT COUNT(CITY) - COUNT(DISTINCT CITY) FROM STATION; 
6 /* Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically. */
SELECT CITY, LENGTH(CITY) FROM STATION ORDER BY LENGTH(CITY) DESC, CITY ASC FETCH FIRST ROW ONLY;
SELECT CITY, LENGTH(CITY) FROM STATION ORDER BY LENGTH(CITY) ASC, CITY ASC FETCH FIRST ROW ONLY;
7 /*Query the list of CITY names starting with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates. */
SELECT DISTINCT(CITY) FROM STATION WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' 
OR CITY LIKE 'U%' ORDER BY CITY ASC;   
8 /* Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates. */
SELECT DISTINCT(CITY) FROM STATION WHERE CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' 
OR CITY LIKE '%U' ORDER BY CITY ASC;
9 /* Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates. */

SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1)) NOT IN ("A","E","I","O","U") OR UPPER(SUBSTR(CITY,Length(City),1)) NOT IN ("A","E","I","O","U");

10 /*Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates. */
SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1)) NOT IN ("A","E","I","O","U")

```python

```


```python

```
