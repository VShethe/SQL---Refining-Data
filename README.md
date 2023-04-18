
# SQL: Refining Data





## Table of Content


**1. SQL: Refinig Data**
 - Adding_Books.sql
 - Distinct.sql
 - Order_by.sql
 - Limit.sql
 - Like.sql
 - Exercise.sql
## Project Description

**Refining Data:**

**1. Adding Books**

    SELECT * FROM books;

    INSERT INTO books
        (title, author_fname, author_lname, released_year, stock_quantity, pages)
    VALUES 
        ('10% Happier', 'Dan', 'Harris', 2014, 29, 256), 
           ('fake_book', 'Freida', 'Harris', 2001, 287, 428),
           ('Lincoln In The Bardo', 'George', 'Saunders', 2017, 1000, 367);
![3](https://user-images.githubusercontent.com/128286364/232774179-3b441609-6958-4309-a805-a64b2c27d139.png)

**2. DISTINCT**

    SELECT 
        DISTINCT author_lname 
    FROM books;
![2](https://user-images.githubusercontent.com/128286364/232774398-85d0d149-b68b-4b72-85f7-cd52bbe64193.png)

    SELECT 
        DISTINCT CONCAT(author_fname,' ', author_lname) As Author 
    FROM books;
![3](https://user-images.githubusercontent.com/128286364/232774458-a9c57905-abcc-4270-9de5-518294f0f0fd.png)


**3. ORDER BY:**

    SELECT 
        title, released_year, pages 
    FROM books 
    ORDER BY released_year;
![4](https://user-images.githubusercontent.com/128286364/232774492-5063796e-510f-4ab0-9304-1cecca4fc15c.png)

    SELECT 
        title, author_fname, author_lname
    FROM books 
    ORDER BY 1 DESC;
![5](https://user-images.githubusercontent.com/128286364/232774532-ce783761-9046-41a9-ace1-e0bb5e972a50.png)


**4. LIMIT:**

    SELECT 
        title 
    FROM books 
    LIMIT 3;
![6](https://user-images.githubusercontent.com/128286364/232774580-00103417-975f-443a-9339-b655dfac3c11.png)

    SELECT 
        title, released_year 
    FROM books
    ORDER BY released_year DESC 
    LIMIT 0,5;
![7](https://user-images.githubusercontent.com/128286364/232774629-967d717c-85e7-44d9-a712-a0f4d534af02.png)

**5. LIKE:**
 
    SELECT 
        title,author_fname 
    FROM books
    WHERE author_fname LIKE '%da%';
![8](https://user-images.githubusercontent.com/128286364/232774672-897fee99-49ac-44c4-8b78-07e62430cf75.png)


    SELECT 
        title, stock_quantity 
    FROM books 
    WHERE stock_quantity LIKE '____';
![9](https://user-images.githubusercontent.com/128286364/232774721-197935d1-1487-4b08-9c38-a91e5807941b.png)

    SELECT 
        title 
    FROM books 
    WHERE title LIKE '%\%%'
 ![10](https://user-images.githubusercontent.com/128286364/232774751-d93d1937-9425-4837-a0ab-cad436d1be18.png)
 

## Installation

To run the program

mysq-ctl cli;
