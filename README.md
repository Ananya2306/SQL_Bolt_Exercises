# SQL_Bolt_Exercises

### Exercise-1

Find the title of each film? SELECT Title FROM Movies; Find the director of each film? SELECT Director FROM Moives; Find the title and director of each film? SELECT Title,Director FROM Movies; Find the title and year of each film? SELECT Title, Year FROM Movies; Find all information about each film? SELECT * FROM Movies;

---
### Exercise-2 

Find the movie with a row id of 6? SELECT * FROM Movies WHERE id = 6; Find the movies released in the years between 2000 and 2010? SELECT * FROM movies where Year BETWEEN 2000 AND 2010; Find the movies not released in the years between 2000 and 2010? SELECT * FROM movies where Year NOT BETWEEN 2000 AND 2010; Find the first 5 Pixar movies and their release year? SELECT Title, Year FROM movies limit 5;

---
### Exercise-3 

Find all the Toy Story movies? SELECT * FROM movies WHERE Title LIKE "Toy Story%"; Find all the movies directed by John Lasseter? SELECT * FROM movies WHERE Director = 'John Lasseter'; Find all the movies (and director) not directed by John Lasseter? SELECT Title,Director FROM movies WHERE Director != 'John Lasseter'; Find all the WALL-* movies? SELECT * FROM movies WHERE Title LIKE 'WALL-%';

---

### Exercise-4 

List all directors of Pixar movies (alphabetically), without duplicates? SELECT DISTINCT Director FROM movies ORDER BY Director ASC; List the last four Pixar movies released (ordered from most recent to least)? SELECT Title FROM movies ORDER BY Year DESC LIMIT 4 ; List the first five Pixar movies sorted alphabetically? SELECT Title FROM movies ORDER BY Title ASC LIMIT 5 ; List the next five Pixar movies sorted alphabetically ? SELECT Title FROM movies ORDER BY Title ASC LIMIT 5 OFFSET 5;

---
### Exercise-5 

List all the Canadian cities and their populations? SELECT City,Population FROM north_american_cities Where Country ='Canada'; Order all the cities in the United States by their latitude from north to south? SELECT City FROM north_american_cities WHERE Country = 'United States' Order by Latitude DESC; List all the cities west of Chicago, ordered from west to east ? SELECT City FROM north_american_cities WHERE longitude < ( SELECT longitude FROM north_american_cities WHERE city = 'Chicago' ) Order by Longitude ASC; List the two largest cities in Mexico (by population)? SELECT City FROM north_american_cities WHERE country = 'Mexico' ORDER BY population DESC LIMIT 2; List the third and fourth largest cities (by population) in the United States and their population ? SELECT City,Population FROM north_american_cities WHERE country = 'United States' ORDER BY population DESC LIMIT 2 OFFSET 2;
