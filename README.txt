# USE lab2;

# SELECT * from details

# Question 1
# SELECT * from details WHERE age >= 40 && age <= 50;

# Question 2
# SELECT * from details WHERE hours >= 10 && hours <= 15;

# Question 3
# SELECT * from details WHERE firstName LIKE '%e%'
# % are wildcards of any amount

# Question 4
# SELECT * from details WHERE lastName LIKE '_u%';
# _ are wildcards of one unit

# Question 5
# SELECT * from details WHERE firstName LIKE '%n' && char_length(firstName) = 4;
# SELECT * from details WHERE firstName LIKE 'J%' && char_length(firstName) = 4;
# SELECT * from details WHERE char_length(firstName) = 3;
# SELECT * from details WHERE char_length(firstName) > 4;

# Question 6
# SELECT * from details WHERE gender = 'F' && age LIKE '%3%';
 
# Question 7
# SELECT count(gender) FROM details WHERE gender LIKE 'F';

# Question 8
# SELECT count(gender) FROM details WHERE gender LIKE 'M';

# Question 9
# SELECT AVG(age) AS AverageAge FROM details WHERE gender LIKE 'F';
 
# Question 10
# SELECT AVG(age) AS AverageAge FROM details WHERE gender LIKE 'M';
