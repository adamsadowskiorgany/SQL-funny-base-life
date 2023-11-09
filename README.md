# SQL-funny-base-life
My way to remember queries

# 1. arise and disappear database/table/column
#arise database
CREATE DATABASE bookstore;
--disappear 
DROP DATABASE bookstore;

#arise table
CREATE TABLE books;
--disappear 
DROP TABLE books;

#arise column
ALTER TABLE users ADD email varchar(30);
 --disappear
ALTER TABLE users DROP COLUMN email;

# 2. useful first setup 
--AUTO_INCREMENT - increase automatically by 1 
--UNIQUE - forbide to repeat the same data, for example: email
--PRIMARY KEY - 

CREATE TABLE users
( 
  user_id int AUTO_INCREMENT,
  user_name varchar(20),
  user_surname varchar(30),
  user_email varchar(30) UNIQUE,
  PRIMARY KEY(user_id)
);

 # 3. modification
#change datatype 
ALTER TABLE users MODIFY COLUMN user_name new_datatype;
---m
ALTER TABLE users MODIFY COLUMN user_name varchar(30);

# 4. add data 
INSERT INTO users(user_name, user_surname, user_email, user_id)
      VALUES ('Alex', 'Sold', 'Alex.Sold@yahoo.com',2);

# 5. update data
--update single 
UPDATE users SET user_name="Krzysztof" WHERE user_id=3;

--update more
UPDATE shipping SET
shipping_cost = "free",
shipping_happy_code = "cheer"
WHERE total_order > 200;

# 6. dupplicat elimination

SELECT DISTINCT genere_book FROM books ORDER BY genre_book ASC;

# 7. delete data
--delete row
DELETE FROM users WHERE email = NULL;

--delete all data 
DELETE FROM users;

# 8. count

SELECT COUNT(book_quantity) AS number_of_sold_books FROM books;

# 9. time for JOIN - INNER/LEFT/RIGHT
