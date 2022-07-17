![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/AutoLot.png)
# MechaCar_Statistical_Analysis
Module 15

## Overview

This project is a statistical analysis for AutosRUS using R and RStudio with two provided csv data files (located in the 'Resources' folder here. Linear Regression is used to predict MPG on prototype vehiles and determine what factors are most inportant in predicting the MPG. Summary descriptive statistics and T-tests are used to assess the manufacturing consistency of suspension coils. The final deliverable of this project is a suggested study to compare MechaCar with competitors.

## Linear Regression to Predict MPG

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/Image1.png)

Using the 'dplyer' and 'tidyverse' python libraries and importing the MechaCar_mpg.csv file into a DataFrame in RStudio, a linear fitting model is created using the lm() function for all independent variables. As seen in the image above, the 'vehicle_length' and 'ground_clearance' varibales were found to have a non-random impact on MPG while vehicle_weight, spoiler_angle, and AWD have p-Values showing random variance.

The p-Value for this model is 0.0000000000535 (or 5.35e-11) which is clearly smaller than the significance level of 0.05% and is sufficient to reject the null hypothesis. This indicates that the slope of the linear model is not zero.

The R-squared values (Multiple R-squared: 0.7149, Adjusted R-squared: 0.6825) indicate that ~70% of MPG predictions can be determined by this model, making it effectinve in predicting MPG for MechaCar prototypes. 


![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/SportSprings.png)
## Summary Statistics on Suspension Coils

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/TotalSummary.png)

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/LotSummary.png)

After imprting the data from Suspension_Coil.csv into a table, the total variance for all lots is under the threshold of 100 PSI. The variance for each lot indicates that there is an issue with Lot 3 (Var_PSI = 170.2861224), as it is the only lot with a variance greater than 100 PSI. Looking further, Lots 1 (Var_PSI = 0.979) and 2 (Var_PSI = 7.469) have very little variance and are well within tolerance limits while Lot 3 has almost enough variance to siggest a problem for total production.



## T-Tests on Suspension Coils

![image](https://github.com/Bryan-Corn/MechaCar_Statistical_Analysis/blob/main/Images/T-Tests.png)

The T-test for all suspension coil lots shows that there is no statistically significant difference from the population mean and the p-Value is not low enough to reject the the null hypothesis. 

As shown above, Lot 1 (t = 0) has very little-to-no variance with a p-Value of 1 and a 95% confidence of 1499.719 - 1500.281. Lot 2  has more variance than Lot 1 one but falls well within tolerance limits (t = 0.51745, p-Value = 0.6072). Lot 3 (t = -2.0916, p-Value = 0.04168) does not meet the variance standards and the manufacturing process needs review. Both lots 2 and 3 should more closely emulate the manufacturing process of Lot 1.



## Study Design: MechaCar vs Competition

Because we already have a good start with our statistical analysis of suspension coils PSI, a future study could examine the variance of MechaCar's suspension coil PSI variance versus sample lots of various competitors' coils. T-tests for each sample lot could be used to asses each competitor and an ANOVA test could be conducted to describe the significance of the variance between each sample and MechaCar's manufacturing. The data needed would be the same suspension coil data that was used in this project but collected from more samaples from other manufacturers. The null hypothesis would be that there is no significant statistical difference in PSI variance.
