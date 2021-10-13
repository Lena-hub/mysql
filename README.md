# mysql

mysql>  SELECT * FROM wizard WHERE birthday BETWEEN '1975-01-01' AND '1985-12-31';
+----+-----------+----------+------------+-------------+---------------------------------------+-----------+
| id | firstname | lastname | birthday   | birth_place | biography                             | is_muggle |
+----+-----------+----------+------------+-------------+---------------------------------------+-----------+
|  1 | harry     | potter   | 1980-07-31 | london      |                                       |         0 |
|  2 | hermione  | granger  | 1979-09-19 |             | Friend of Harry Potter                |         0 |
|  4 | ron       | weasley  | 1980-03-01 |             | Best friend of Harry                  |         0 |
|  5 | ginny     | weasley  | 1981-08-11 |             | Sister of Ron and girlfriend of Harry |         0 |
|  6 | fred      | weasley  | 1978-04-01 |             |                                       |         0 |
|  7 | george    | weasley  | 1978-04-01 |             |                                       |         0 |
| 10 | drago     | malefoy  | 1980-06-05 |             |                                       |         0 |
| 14 | dudley    | dursley  | 1980-06-23 |             | Cousin d'Harry                        |         1 |
| 15 | harry     | potter   | 1980-07-31 | london      |                                       |         0 |
| 16 | hermione  | granger  | 1979-09-19 |             | Friend of Harry Potter                |         0 |
| 18 | ron       | weasley  | 1980-03-01 |             | Best friend of Harry                  |         0 |
| 19 | ginny     | weasley  | 1981-08-11 |             | Sister of Ron and girlfriend of Harry |         0 |
| 20 | fred      | weasley  | 1978-04-01 |             |                                       |         0 |
| 21 | george    | weasley  | 1978-04-01 |             |                                       |         0 |
| 24 | drago     | malefoy  | 1980-06-05 |             |                                       |         0 |
| 28 | dudley    | dursley  | 1980-06-23 |             | Cousin d'Harry                        |         1 |
| 29 | harry     | potter   | 1980-07-31 | london      |                                       |         0 |
| 30 | hermione  | granger  | 1979-09-19 |             | Friend of Harry Potter                |         0 |
| 32 | ron       | weasley  | 1980-03-01 |             | Best friend of Harry                  |         0 |
| 33 | ginny     | weasley  | 1981-08-11 |             | Sister of Ron and girlfriend of Harry |         0 |
| 34 | fred      | weasley  | 1978-04-01 |             |                                       |         0 |
| 35 | george    | weasley  | 1978-04-01 |             |                                       |         0 |
| 38 | drago     | malefoy  | 1980-06-05 |             |                                       |         0 |
| 42 | dudley    | dursley  | 1980-06-23 |             | Cousin d'Harry                        |         1 |
+----+-----------+----------+------------+-------------+---------------------------------------+-----------+
24 rows in set (0.00 sec)

mysql> SELECT firstname FROM wizard WHERE firstname LIKE 'h%';
+-----------+
| firstname |
+-----------+
| harry     |
| hermione  |
| harry     |
| hermione  |
| harry     |
| hermione  |
+-----------+
6 rows in set (0.00 sec)

mysql> SELECT * FROM wizard WHERE lastname='potter' ORDER BY firstname;
+----+-----------+----------+------------+-------------+------------------------+-----------+
| id | firstname | lastname | birthday   | birth_place | biography              | is_muggle |
+----+-----------+----------+------------+-------------+------------------------+-----------+
|  1 | harry     | potter   | 1980-07-31 | london      |                        |         0 |
| 15 | harry     | potter   | 1980-07-31 | london      |                        |         0 |
| 29 | harry     | potter   | 1980-07-31 | london      |                        |         0 |
|  3 | lily      | potter   | 1960-01-30 |             | mother of Harry Potter |         0 |
| 17 | lily      | potter   | 1960-01-30 |             | mother of Harry Potter |         0 |
| 31 | lily      | potter   | 1960-01-30 |             | mother of Harry Potter |         0 |
+----+-----------+----------+------------+-------------+------------------------+-----------+
6 rows in set (0.00 sec)

mysql> SELECT firstname, lastname, birthday FROM wizard WHERE is_muggle='0' ORDER BY birthday ASC LIMIT 1;
+-----------+------------+------------+
| firstname | lastname   | birthday   |
+-----------+------------+------------+
| albus     | dumbledore | 1881-07-01 |
+-----------+------------+------------+
1 row in set (0.01 sec)
