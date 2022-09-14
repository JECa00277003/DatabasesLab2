USE lab2;

# SELECT * FROM details

#Part 1
# Question 1
# SELECT * FROM details WHERE age >= 40 && age <= 50;

# Question 2
# SELECT * FROM details WHERE hours >= 10 && hours <= 15;

# Question 3
# SELECT * FROM details WHERE firstName LIKE '%e%'
# % are wildcards of any amount

# Question 4
# SELECT * FROM details WHERE lastName LIKE '_u%';
# _ are wildcards of one unit

# Question 5
# SELECT * FROM details WHERE firstName LIKE '%n' && char_length(firstName) = 4;
# SELECT * FROM details WHERE firstName LIKE 'J%' && char_length(firstName) = 4;
# SELECT * FROM details WHERE char_length(firstName) = 3;
# SELECT * FROM details WHERE char_length(firstName) > 4;

# Question 6
# SELECT * FROM details WHERE gender = 'F' && age LIKE '%3%';
 
# Question 7
# SELECT count(gender) AS NumFemales FROM details WHERE gender LIKE 'F';
# select count(*) as NumFemales from details where gender = 'F';

# Question 8
# SELECT count(genderM) AS Males FROM details WHERE gender LIKE 'M';

# Question 9
# SELECT AVG(age) AS AverageAgeF FROM details WHERE gender LIKE 'F';
 
# Question 10
# SELECT AVG(age) AS AverageAgeM FROM details WHERE gender LIKE 'M';

# Part 2
# Question 1
# SELECT firstName, lastName, age FROM details WHERE age = (select MAX(age) FROM details);

# Question 2
# SELECT firstName, lastName, age FROM details WHERE age = (select MIN(age) FROM details);

# Question 3
# SELECT AVG(hours) AS AverageHours FROM details;

# Question 4
# SELECT SUM(rate*hours) AS SumFemaleWage FROM details WHERE gender = 'F';

# Question 5
# SELECT SUM(rate*hours) AS SumMaleWage FROM details WHERE gender = 'M';

# Question 6
# SELECT department, AVG(age) FROM details GROUP BY department;

# Question 7
# SELECT position, AVG(age) FROM details GROUP BY position;

# Question 8
# SELECT department, COUNT(*) AS NumMales FROM details WHERE gender = 'M' GROUP BY department;
# SELECT department, COUNT(*) AS NumFemales FROM details WHERE gender = 'F' GROUP BY department;
# SELECT department, gender, COUNT(*) FROM details GROUP BY department, gender;

# Question 9
# SELECT department,
# COUNT(case WHEN details.gender = 'M' THEN 1 END) AS male_count,
# COUNT(case WHEN details.gender = 'F' THEN 1 END) AS female_count
# FROM details GROUP BY department;

# Question 10
# SELECT firstName, lastName, hours*rate AS wage FROM details ORDER BY wage desc limit 3;
