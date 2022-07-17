# MechaCar_Statistical_Analysis
Module 15

## Overview

This project is a statistical analysis for AutosRUS using R and RStudio with two provided csv data files (located in the 'Resources' folder here. Linear Regression is used to predict MPG on prototype vehiles and determine what factors are most inportant in predicting the MPG. Summary descriptive statistics and T-tests are used to assess the manufacturing consistency of suspension coils. The final deliverable of this project is a suggested study to compare MechaCar with competitors.

## Linear Regression to Predict MPG

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/Image1.png)

Using the 'dplyer' and 'tidyverse' python libraries and importing the MechaCar_mpg.csv file into a DataFrame in RStudio, a linear fitting model is created using the lm() function for all independent variables. As seen in the image above, the 'vehicle_length' and 'ground_clearance' varibales were found to have a non-random impact on MPG while vehicle_weight, spoiler_angle, and AWD have p-Values showing random variance.

The p-Value for this model is 0.0000000000535 (or 5.35e-11) which is clearly smaller than the significance level of 0.05% and is sufficient to reject the null hypothesis. This indicates that the slope of the linear model is not zero.

The R-squared values (Multiple R-squared: 0.7149, Adjusted R-squared: 0.6825) indicate that ~70% of MPG predictions can be determined by this model, making it effectinve in predicting MPG for MechaCar prototypes. 


## Summary Statistics on Suspension Coils

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/TotalSummary.png)

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/LotSummary.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?



## T-Tests on Suspension Coils

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/T-Tests.png)

briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.



## Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating


In your description, address the following questions:
• What metric or metrics are you going to test?
• What is the null hypothesis or alternative hypothesis?
• What statistical test would you use to test the hypothesis? And why?
• What data is needed to run the statistical test?
