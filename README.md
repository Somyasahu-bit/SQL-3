# SQL-3
DROP TABLE IF EXISTS users;

CREATE TABLE IF NOT EXISTS users (       
  user_id SERIAL PRIMARY KEY,
  username VARCHAR(50) NOT NULL,
  email VARCHAR(100) UNIQUE,
  age INT,
  City VARCHAR(50)
);

SELECT * FROM users;

INSERT INTO users (username, email, age, city)
VALUES ('Somya','somya@gmail.com', 20, 'Seoni'),
('Raju','rajugmail.com', 21, 'Sehore'),
('Shiv','shiv@gmail.com', 24, 'indore'),
('Kajal', 'kajal@gmail.com', 25, 'Seoni');



SELECT user_id FROM users;

UPDATE users
SET age=22
WHERE username='Somya';

SELECT * FROM users ORDER BY username ASC;
SELECT * FROM users ORDER BY user_id ASC

UPDATE users
SET City='jabalpur'
WHERE age>=20;

UPDATE users
SET age=24,city='china'
WHERE username='Raju';
