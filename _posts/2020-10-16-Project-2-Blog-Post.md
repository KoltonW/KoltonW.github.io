---
layout: post
title: Project 2 Blog Post
---
 
[Here is a link to my Project 2 Github page repo](https://koltonw.github.io/ST558Project2/)

For this project, the task was to take a bike sharing data set, filter by weekday, split the data up into training and test sets, create summaries and plots for the training data, create predictive models for the cnt response variable, and test these model fits on the test sets for each weekday automatically. 

Initially, I read in the data set, then fit a linear model to see what predictor variables had the most importance with the response variable, cnt, which is the count of rental bikes for each day between 2011 and 2012. I was able to narrow the predictor variables down to 8 important ones: season, weekday, working day, holiday, weather situation, temperature, humidity, and wind speed. From here, I restructured the data a bit before setting it to filter for each day of the week. I then set the training data to be 70% of this new filtered data, with the test set being the other 30%. 

I next performed a little bit of exploratory data analysis by looking at some summaries and plots for this training data. I looked at just an overview of summary statistics for the cnt response variable itself. Then, I checked how the mean and standard deviation of this response variable changed with different values of season and weather situation. From here, I created scatterplots of cnt vs wind speed, temperature, and humidity to see if there were any correlations between these variables. A main finding from these plots was that for each weekday, cnt had a moderately high correlation with temperature; meaning that as the temperature increased, the number of bikes rented increased as well. 

Next, two models were fit on the training data: a regression tree model and a boosted tree model. Both models had a variety of tuning parameters to select from, and the final model reflected the tuning parameters that created a model with the lowest RMSE and MAE and highest R-squared value. The final models from each of these types were then fit onto the test set. The models were compared on how well they fit the test set by details such as RMSE, MAE, and R-squared values. 

After finalizing all this for one day and testing it on weekday = Monday, I created a render function to automate reproduction of this report for each day of the week. All resulting analyses are shown in my Project 2 Github page repo in separate links. Another link to my [Project 2 Github page can be found here.](https://koltonw.github.io/ST558Project2/)

This whole process was not too entirely difficult once I was able to plan out each of my steps and go from there. If I was to do this project again, I might try with different predictor variables for the response of cnt and see if there was any improvement in model accuracy. The most difficult part was getting the automation to run for all days of the week while filtering the data out. However, my big take-away from this project was how much easier it is to automate multiple reports with one render function than trying to change the code and knit over and over. Also, I made sure to take note of how different tuning parameters affects the model based on the data given. 
