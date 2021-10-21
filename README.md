# u-develop-it

Coding bootcamp week 12/24. Voting app

Continue reading 12.
Working on 12.1.

mysql --version
mysql -u root -p

SQL Commands

- Initiates sql and asks for passcode
  mysql -u root -p

- Crerates "election" database
  mysql> CREATE DATABASE election;

- Selects "election" to be used
  USE election;

  - Execute script
    SOURCE folder name/file name with extension

- Creates "candidates" table
  CREATE TABLE candidates (
  id INTEGER AUTO_INCREMENT PRIMARY KEY,
  first_name VARCHAR(30) NOT NULL,
  last_name VARCHAR(30) NOT NULL,
  industry_connected BOOLEAN NOT NULL
  );

- Displays "candidates" table without actual values
  DESCRIBE candidates;

- Adds values to the candidates table
  INSERT INTO candidates (first_name, last_name, industry_connected)
  VALUES ('Ronald', 'Firbank', 1);

- displays _(all) from candidates.
  SELECT _ FROM candidates;

- Displays data from candidates with the first name and last name values
  SELECT first_name, last_name FROM candidates;

- queries to display candidates that are industry connected where industry connected is a filter. 1 is the bolean for true.
  SELECT first_name, industry_connected
  FROM candidates
  WHERE industry_connected = 1;

- Queries to display with id
  SELECT first_name, last_name, industry_connected
  FROM candidates
  WHERE id = 5;

- within a database SHOW provides a list of tables.
  SHOW tables;

* Update a row, where selects the row to update and SET updates the info
  UPDATE candidates
  SET industry_connected = 1
  WHERE id = 3;

* Delete - self explanatory
  DELETE FROM candidates
  WHERE first_name = "Montague";
