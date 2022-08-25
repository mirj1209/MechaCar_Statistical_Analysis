# MechaCar Statistical Analysis
Statistical analysis of automobile performance with R

## Overview
AutosRUs' new project, the MechaCar, is suffering from production troubles that are restrict the manufacturing team's progress. This analysis is meant to review the production data in hopes of providing some insight with the following goals:
- Determine which variables predict the mpg of MechaCar prototypes
- Collect summary statistics on the PSI (pounds per square inch) of the suspension coils
- Run t-tests to determine if the manufacturing lots are statistically different from the mean
- Design a study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

# Results
## Linear Regression to Predict MPG 
![image](https://user-images.githubusercontent.com/104941338/186560436-8b4d8fbc-f3b0-46a6-9725-9ef5141ceea1.png)
- The most significant values in our dataset showing a non-random effect on the MPG of the prototype are the vehichle length and the ground chance. Focus your attention to those two variables in the image above and you'll see a linear regression model run on these variables against figures for MPG. These resulted p-values of 2.6x10^-12 and 5.21x10^-8. The intercept was also statistically significant saying that there are likely other factors, not included in the dataset which have a strong impact on the MPG.
- The slope of the linear model cannot be considered zero, as the p-value is 5.35x10^-11, is lower than a huge level of significance and therefore a null hypothesis must be rejected meaning that, the relationship between our variables and the MPG is subject to more than mere random chance. 
- This model does predict the MPG of the prototype with relative effectiveness. The r-quared value of 0.7149 indicates that the model is around 71% accurate thus there's room for improvement.

## Summary Statistics on Suspension Coils
![image](https://user-images.githubusercontent.com/104941338/186561606-42ad5078-6269-40fb-bfa0-d93aa8d587e4.png)
![image](https://user-images.githubusercontent.com/104941338/186561725-385a7e45-2eaf-43a2-9c8a-d757fc0dbeea.png)
- As shown in the Total summary data above, is under 100 PSI and meets specifications. There's an issue with one of the lots as shown in the lot summary stats, the variance of lot 3 is well over the acceptable threshold, at 170.28

## T-Tests on Suspension Coils.
Suspension coils cumulative t-test:
![image](https://user-images.githubusercontent.com/104941338/186562483-4d314258-7d31-4578-92de-65232bcc8b50.png)
The image above is a small review on the results of the t-test for the suspension of coils across all manufacturing lots shows that they aren't statistically different from the population average/mean. The p-value is not low enough for us to reject the null hypothesis. 

![image](https://user-images.githubusercontent.com/104941338/186562844-353d7c73-5d76-423b-b14c-ea0a662eb8ff.png)
- A review on the results of the t-test for the suspension coils for lot 1 shows that they're not statistically different from the population mean/average and the p-value isn't low enough for us to reject the null hypothesis.

![image](https://user-images.githubusercontent.com/104941338/186563577-a4e81368-982e-48ce-9206-3499953804f8.png)
- A review on the results of the t-test for the suspension coils for lot 2 shows that they're not statistically different from the population average/mean (like in lot 1) and the p-value isn't low enough for us to reject the null hypothesis. 

![image](https://user-images.githubusercontent.com/104941338/186563761-0681ce3c-bcb9-4a97-b083-201945fcd5bb.png)
- A review on the results of the t-test for the suspension coils for lot 3 shows that they are slightly statistically different to the population mean/average and the p-value is just low enough for us to reject the null hypothesis and therefore this may need to be discarded and re-evaluated more closely. 

## Study Design: MechaCar vs Competition

### Metric to test:
To narrow down the test, we should evaluate MechaCar's carrying capacity in cubic inches in comparisson to competitor's vehicles as consumers take into consideration the capacity of the vehicle when purchasing. 

### Null and Alternate Hypothesis:
- MechaCar's prototype's mean capacity is similar to competitors and in the same vehicle class
- MechaChar prototype's mean capacity is statistically above or below competitor vehicles. 

### Statistical test used:
The  best for this would be two t-tests on average carrying capacity data in cubic inches. 
