# SQL-funny-base-life
My way to remember queries

# 1. arise and disappear database/table/column
#arise database
CREATE DATABASE library;
--disappear 
DROP DATABASE library;
#arise table
CREATE TABLE book;
--disappear 
DROP TABLE book;
#arise column
ALTER TABLE users ADD email varchar(30);
 --disappear
ALTER TABLE users DROP COLUMN email;
 # 2. modification
#change datatype 
ALTER TABLE users MODIFY COLUMN user_name new_datatype;
--modify column 
ALTER TABLE users MODIFY COLUMN user_name varchar(30);
# 3. update data
--update single 
UPDATE users SET user_name="Krzysztof" WHERE user_id=234;
--update more
UPDATE users SET
shipping = "free",
happy_code = "cheer"
WHERE total_order > 200;

# 4. delete data
--delate row
DELETE FROM users WHERE email = NULL;
--delete all data 
DELETE FROM users;
