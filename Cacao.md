# Flavours of Cacao


https://www.kaggle.com/rtatman/chocolate-bar-ratings?select=flavors_of_cacao.csv


Purpose of the analysis is to find out what makes the best chocolate bar. 
*do not judge, dataset was chosen while being sick and on PMS*


Data set includes manufacturers, the country of manufacturing. bean type and it's origin, as well as the cacao percentage and date and outcome of the review.

What could be analised is:
 - What types of beans get the highest / lowest ratings?
 - What is the origin of beans with the highest / lowest ratings?
 - Does any manufacturer stand out?
 - Does any country stand out?
 - Does the cacao & influence the rating?
 - How has the rating for particular factors change throught the years?
 
 
## CLEANING
 
 1. Column names changed for better usability.
 2. Duplicates checked.
 3. Missing values checked.
     3a. Columns with missing values identified.
     3b. Replacement assigned.
     3c. 'fillna' not working - content of the "empty" cell identified and replaced
 4. Identifying blends 
to limit the amount of bean origins - multiple options have failed, turned out some values were identified as "floats", changing the type has enabled me to create a list of blends, as well as replace all of them with a generic "blend" value.
 5. Finding misspelled origins
 6. Simplifying bean types
 7. Identifying misspelled duplicates in bean types and correcting them.
 *  Quick assessment of data for highest and lowest rated bars 
 8. Further cleanup = changing a column name and getting rid of the percentage sign
 9. Saving the ready dataset to a file.
 
 
 ## ANALYSIS
 
 1. First, I wanted to see what the general tendency in rating was. Have the bars mainly been rated as bad, mediocre or outstanding?
 
![rating_counts](rating_counts.png)
     
 And the result is, as we can see - bars are mainly rated as avarage and slightly above avarage. Generally a positive outcome then, as expected when it comes to chocolate.
 
 
 2. Secondly, has any bean type stood out?
 
![bean_type_rating](Bean_type_rating.png)
 
 From the scatterpplot it could be clearly seen that for some types ratings vary more than for others, could this be caused by the difference in number of records for each type?
 
 
 3. Is the number of records for different bean types comparable?
 
![Bean_type_records](Bean_type_records.png)
     
  This clearly shows only a few bean types are represented by enough records to be useful for analysis. I have also checked and confirmed that the same types are the main representations in the "best" and "worst" subsets, to confirm that the same types should be of our main interest.
  
  
 4. Have the avarage Cacao percentages or ratings changed?
  
![Average_perc_and_rates](Average_perc_and_rates.png)

 The average rating, after a big drop in 2008 have been been going up with some drops to then experience a bigger spike in 2017. Hopefully this means the quality of chocolate has been improving in that period and will always continue the trend so we can expeirence even better chocoalate each year!
 
 Cacao percantage has been fluctuation with a significant spike in 2013 only to drop back down after. Seems that the trend for a much higher percentages has only been short lived.
 
 
 5. What do the ratings look like depending on the Bean Origin?
    
![origin_rate](origin_rate.png)

For most origins ratings are quite spread out. The three countries that stand out among the lowest ratings are Hawaii, Mexico and West Africa, especially the latter. Some that have values above average would be South America, Guatemala, Cuba. Phillipines, Honduras, Tanzania and blends. (Here I can notice that South America could potentially be considered a blend or! blends should be split out into subcategories, where south america could be one of them).
     
     
 6. Are the numbers of records for different bean origins comparable?
 
![origin_records](origin_records.png)

Considering how different amounts of records are for specific origins, it would be difficult to reasonably compare them without further data. (are these the only chocolate bars produced in the country? how have they been chosen? should we group the data by more specific features - i.e. specifi percentages of cacao or bean type - room for a more in depth analysis.)

Analyisng the 5 most common origins, Venezuela stands out as the highest rated origin along with Belize (although the latter had a much smaller sample size available).

![comm_origin_rate](comm_origin_rate.png)
    
    
    
   + How does the cacao percentage change through the years look like for the most common origins comparing to all?
Seems that for the most common origins the trend to go for higher percentages has grown a bit faster towards the previously mentioned 2013 spike, whereas for all origins we can notice a higher spike in 2008, which could suggest other origins where previously used for the higher percentages and then few years later, our popular origins got their turn.

![percentage_comparison](./Interactive/percentage_comparison.png)
    
    
7. What about country of production?

![comm_madein_rate](comm_madein_rate.png)

Similar analysis has been done for the Countries of production and the conclusions are similar. It's difficult to compare among much different sample sizes, although we could assume some countries manufacture more than others - again, more information about how the data has been gathered and chosen to be included in the dataset would be required. From the analysis of the most common producers, Canada seems to be the one with higest ratings, while UK is the least favorited one of the lot.


8. Does the percentage of cacao has impact on the rating?

![ratings_and_percentage](./Interactive/ratings_and_percentage.png)

Seems that no matter the percantage the rating could vary in a similar way. Having said that, if you do not want the rating to go below 3, aim for 69%, but if you're ambitious and aiming for a 5 - up that one percent into 70% :)


9. Lastly, in our data set, what do the occurances of different cacao percentages look like through the years?

![percentage_in_time](./Interactive/percentage_in_time.png)

As we have previously noticed, the avarage percentage has been growing between 2009 and 2013, however - for the first 4 years of that growth it seems that manufacturers were sticking more to the safer, lower percentages anyway, not reaching the 90% mark.


## CONCLUSION
Analysing chocolate in any way is always fun, however for this data set I found it quite difficult to easily come to any conclusions and particular factors were not readily comparable. It definitely asks for more in depth analysis, dividing data into more specific subsets or ideally, gathering a bigger sample size or altrnatively.. diving into some data gathering on my own - hands (and tummy) on.
