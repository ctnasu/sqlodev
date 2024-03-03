# sqlodev
1. ödev
1.SELECT title,description FROM film;
2.SELECT*FROM film
WHERE length>60 AND length <75;
3.SELECT * FROM film 
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
4.SELECT last_name FROM customer 
WHERE first_name = 'Mary';
5.SELECT * FROM film 
WHERE NOT(length <= 50 AND rental_rate IN (2.99, 4.99);

2.ödev
1.SELECT * FROM film WHERE replacement_cost BETWEEN 12.99 AND 16.99;
2.SELECT first_name, last_name FROM actor 
WHERE first_name IN ('Penelope', 'Nick', 'Ed');
3.SELECT * FROM film 
WHERE rental_rate IN (0.99, 2.99, 4.99) 
AND replacement_cost IN (12.99, 15.99, 28.99);

3. ödev
1.SELECT country FROM country
WHERE country LIKE 'A%a';
2.SELECT country
FROM country
WHERE LENGTH(country) >= 6 AND country LIKE '%n';
3.SELECT title
FROM film
WHERE title ILIKE '%T%T%T%T%';
4.SELECT *
FROM film
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99;

4.ödev
1.SELECT DISTINCT replacement_cost
FROM film
2.SELECT COUNT(DISTINCT replacement_cost);
FROM film
3.SELECT COUNT(*) 
FROM film
WHERE title LIKE 'T%' AND rating = 'G';
4.SELECT COUNT(*) FROM country WHERE length = 5; 
5.SELECT COUNT(*) FROM city
WHERE name ILIKE '%r';

5.ödev
1.SELECT title
FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
2.SELECT title
FROM film
WHERE title LIKE '%n'
 ORDER BY length ASC
OFFSET 5 LIMIT 5;
3.SELECT *
FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;

6.ödev
1.SELECT AVG(rental_rate) FROM film;
2.SELECT COUNT(*)
FROM film
WHERE title LIKE 'C%';
3.SELECT MAX(length) FROM film
WHERE rental_rate = 0.99;
4.SELECT COUNT(DISTINCT replacement_cost) FROM film
WHERE length > 150;

7.ödev
1.SELECT rating, COUNT(*) FROM film
GROUP BY rating;
2.SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY film_count DESC;
3.SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;
4.SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;

8.ödev
1.CREATE TABLE employee (
    id SERIAL PRIMARY KEY,
    name VARCHAR(50),
    birthday DATE,
    email VARCHAR(100)
);
2.    insert into employee (id, name, birthday, email) values (1, 'Ravid', '1995/01/16', 'raxworthy0@npr.org');
    insert into employee (id, name, birthday, email) values (2, 'Hedi', '1999/08/14', 'hwicks1@cnet.com');
    insert into employee (id, name, birthday, email) values (3, 'Shep', '1983/06/08', 'sdodman2@discovery.com');
    insert into employee (id, name, birthday, email) values (4, 'Jud', '1978/07/12', 'jcamis3@comsenz.com');
    insert into employee (id, name, birthday, email) values (5, 'Carmella', '1994/05/21', 'cboggas4@tinypic.com');
    insert into employee (id, name, birthday, email) values (6, 'Mattheus', '1975/11/26', 'mlearmond5@cnbc.com');
    insert into employee (id, name, birthday, email) values (7, 'Papagena', '1992/05/19', 'pblowfelde6@vk.com');
    insert into employee (id, name, birthday, email) values (8, 'Alejoa', '1978/05/04', 'afillingham7@gnu.org');
    insert into employee (id, name, birthday, email) values (9, 'Marchelle', '1993/02/05', 'mcastro8@digg.com');
    insert into employee (id, name, birthday, email) values (10, 'Randi', '1986/10/15', 'rjaulmes9@woothemes.com');
    insert into employee (id, name, birthday, email) values (11, 'Tiffany', '1997/08/28', 'tsiffletta@sogou.com');
    insert into employee (id, name, birthday, email) values (12, 'Norry', '1993/04/08', 'nsabbinsb@eepurl.com');
    insert into employee (id, name, birthday, email) values (13, 'Rabi', '2002/06/14', 'rbirtonshawc@google.ca');
    insert into employee (id, name, birthday, email) values (14, 'Pablo', '1975/11/04', 'pwarringtond@ameblo.jp');
    insert into employee (id, name, birthday, email) values (15, 'Marven', '1989/08/08', 'mcutridgee@is.gd');
    insert into employee (id, name, birthday, email) values (16, 'Cosetta', '1999/10/03', 'ccrombf@google.es');
    insert into employee (id, name, birthday, email) values (17, 'Renaud', '1978/10/14', 'rhazaelg@meetup.com');
    insert into employee (id, name, birthday, email) values (18, 'Lew', '1996/10/17', 'lcarcassh@marriott.com');
    insert into employee (id, name, birthday, email) values (19, 'Gilles', '2000/09/28', 'gsandercocki@smh.com.au');
    insert into employee (id, name, birthday, email) values (20, 'Lorie', '2000/09/09', 'lpolendinej@irs.gov');
    insert into employee (id, name, birthday, email) values (21, 'Deb', '1996/06/06', 'dratchfordk@cbsnews.com');
    insert into employee (id, name, birthday, email) values (22, 'Coretta', '1983/06/23', 'chairsl@sakura.ne.jp');
    insert into employee (id, name, birthday, email) values (23, 'Henderson', '1999/08/10', 'hnisiusm@nih.gov');
    insert into employee (id, name, birthday, email) values (24, 'Rooney', '1984/06/16', 'rullyattn@reference.com');
    insert into employee (id, name, birthday, email) values (25, 'Kit', '1997/10/24', 'kewbancko@spiegel.de');
    insert into employee (id, name, birthday, email) values (26, 'Stan', '2002/12/17', 'shuxleyp@pcworld.com');
    insert into employee (id, name, birthday, email) values (27, 'Garth', '2000/06/29', 'ghaddowq@jigsy.com');
    insert into employee (id, name, birthday, email) values (28, 'Heinrick', '2003/03/29', 'haronstamr@opensource.org');
    insert into employee (id, name, birthday, email) values (29, 'Maryellen', '1985/09/19', 'mstrobands@youtube.com');
    insert into employee (id, name, birthday, email) values (30, 'Cristine', '1979/08/01', 'cdearlovet@gnu.org');
    insert into employee (id, name, birthday, email) values (31, 'Quill', '1999/09/30', 'qtheureru@de.vu');
    insert into employee (id, name, birthday, email) values (32, 'Morganne', '1997/01/19', 'mdymottv@oakley.com');
    insert into employee (id, name, birthday, email) values (33, 'Jerrie', '1974/03/11', 'jshervillew@devhub.com');
    insert into employee (id, name, birthday, email) values (34, 'Terrijo', '1996/05/13', 'tblazevicx@wikia.com');
    insert into employee (id, name, birthday, email) values (35, 'David', '1981/12/22', 'dhastwally@aol.com');
    insert into employee (id, name, birthday, email) values (36, 'Hi', '1984/07/17', 'hpanyerz@mashable.com');
    insert into employee (id, name, birthday, email) values (37, 'Rosanna', '1990/04/13', 'rdeniskevich10@epa.gov');
    insert into employee (id, name, birthday, email) values (38, 'Elise', '1974/10/04', 'esummersby11@europa.eu');
    insert into employee (id, name, birthday, email) values (39, 'Berti', '1984/02/29', 'bphuprate12@facebook.com');
    insert into employee (id, name, birthday, email) values (40, 'Terry', '1980/01/14', 'tstretton13@wix.com');
    insert into employee (id, name, birthday, email) values (41, 'Romeo', '1976/06/01', 'rbellchamber14@microsoft.com');
    insert into employee (id, name, birthday, email) values (42, 'Skipton', '1998/11/15', 'skattenhorn15@joomla.org');
    insert into employee (id, name, birthday, email) values (43, 'Jennine', '2003/04/21', 'jansley16@disqus.com');
    insert into employee (id, name, birthday, email) values (44, 'Mariel', '1983/02/24', 'mwidmore17@sitemeter.com');
    insert into employee (id, name, birthday, email) values (45, 'Arman', '1981/08/12', 'aforbear18@weather.com');
    insert into employee (id, name, birthday, email) values (46, 'Shaylynn', '1974/09/14', 'srodgman19@networksolutions.com');
    insert into employee (id, name, birthday, email) values (47, 'Chanda', '1995/06/10', 'cmarian1a@wikipedia.org');
    insert into employee (id, name, birthday, email) values (48, 'Merwyn', '1974/08/16', 'mtomas1b@harvard.edu');
    insert into employee (id, name, birthday, email) values (49, 'Saunderson', '1981/08/09', 'slipsett1c@msn.com');
    insert into employee (id, name, birthday, email) values (50, 'Liurette', '1986/09/03', 'lbraim1d@amazon.com');
    
3.UPDATE employee
SET name = 'Michael Smith'
WHERE id = 1;

UPDATE employee
SET birthday = '1987-09-25'
WHERE id = 2;

UPDATE employee
SET email = 'updated.email@example.com'
WHERE id = 3;

UPDATE employee
SET name = 'Emily Johnson'
WHERE id = 4;

UPDATE employee
SET birthday = '1995-12-10'
WHERE id = 5;

4.DELETE FROM employee
WHERE id = 1;

DELETE FROM employee
WHERE name = 'Michael Smith';

DELETE FROM employee
WHERE birthday = '1987-09-25';

DELETE FROM employee
WHERE email = 'updated.email@example.com';

DELETE FROM employee
WHERE id = 5;

9.ödev
1.SELECT city.city, country.country
FROM city
INNER JOIN country ON city.country_id = country.country_id;
2.SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN payment ON customer.customer_id = payment.customer_id;
3.SELECT rental.rental_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN rental ON customer.customer_id = rental.customer_id;




