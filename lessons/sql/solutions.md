---
layout: lesson
root: ../..
title: "Solutions to SQL exercises"
---
**EXERCISE**  
Write a query that returns the year, month, day, species and weight in mg  
**SOLUTION**  

	SELECT year, month, day, species, wgt*1000 FROM surveys


**EXERCISE**  
 Write a query that returns the day, month, year, species, and weight (in kg) for individuals caught on Plot 1 that weigh more than 75 g  
**SOLUTION**  

	SELECT year, month, day, species, wgt/100 
	FROM surveys 
	WHERE (plot ="1") AND (wgt > "75")


**EXERCISE**  
 Write a query that returns The day, month, year, species ID, and weight (in kg) for individuals caught on Plot 1 that weigh more than 75 g  
**SOLUTION**
 
 	SELECT surveys.month, surveys.day, surveys.year, surveys.wgt/1000.0, species.species_id 
 	FROM surveys  
 	JOIN species ON surveys.species = species.species_id 
 	WHERE (surveys.wgt >"75") AND (surveys.plot ="1")
 
**EXERCISE**   
Write a query that returns day, month, year, species for individuals caught  in January, May and July  
 **SOLUTION**  

	SELECT year, month, day, species, wgt/100 
	FROM surveys 
	WHERE (month IN ("1", "5", "7"));
 


**EXERCISE**   
 Write a query that returns year, species, and weight in kg from the surveys table, sorted with the largest weights at the top  
**SOLUTION**  

	SELECT year, month, day, species, wgt/100 
	FROM surveys ORDER BY wgt DESC

**EXERCISE**    
 Let’s try to combine what we’ve learned so far in a single query. Using the surveys table write a query to display the three date fields, species ID, and weight in kilograms (rounded to two decimal places), for rodents captured in 1999, ordered alphabetically by the species ID.
 **SOLUTION**
 
	 SELECT year, month, day, species, ROUND(wgt/100,2) 
	 FROM surveys 
	 WHERE  (year="1999") 
	 ORDER BY species ASC
 
 

**EXERCISE**    
Write queries that return: 1. How many individuals were counted in each year 2. Average weight of each species in each year  
**SOLUTION**  

	SELECT year, species, COUNT(*)
	FROM surveys
	GROUP BY year
	ORDER BY COUNT(species)
	
	
	SELECT year, species, SUM(wgt)
	FROM surveys
	GROUP BY year, species
	ORDER BY year
	
	

**EXERCISE**  
 Write a query that returns the genus, the species, and the weight of every individual captured at the site  
**SOLUTION**  

	SELECT species.genus, species.species, surveys.wgt 
	FROM surveys 
	JOIN species 
	ON surveys.species = species.species_id 
  
