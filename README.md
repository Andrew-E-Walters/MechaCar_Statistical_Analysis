# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
Using the MechCar_mpg.csv we were able to look a number of factors that could have an impact on the overall MPG of cars. By setting the MPG as the dependent variable and the others as the independed variables we can then see what impact if any they have. 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Import and read in the MechaCar_mpg.csv file as a dataframe. Perform linear regression using the lm() function. In the lm() function, pass in all six variables. Using the summary() function, determine the p-value and the r-squared value for the linear regression mode
![Code for Deliverable 1](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/Deliverable%201.png)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
Reffering to the above summary we can see that Vehicle Length, Spoiler Angle, and AWD had more than a non random ammount of variance to the MPG values. The P Values for each of those independent variables was of an ammount that is deemed statistically signifigant. They are all above the 0.05 P value. So from that we can say that Vehicle Length, Spoiler Angle, and AWD have a statistically signifigant impact on a vehichles MPG. 

### Is the slope of the linear model considered to be zero? Why or why not?
The Slope of the linear model is not 0. This is because the when we are accounting for all of the variables it gives us a level of predicabilty on the MPG. However some of the independent variables are a greater predictor than others. We can see that some of the variables have a positive vs negative corelation, while some of the varibles have no corelation. 

![Linear Regression Graphs](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/Deliverable%201%20Graphs.png)

### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
Looking back to the summary we can see the the R Squared Values. THe Multiple R Squared is 0.7149 and the Adjusted R Squared is 0.6825. So we can say that roughly 70% of the variablilty of our dependent variables is explained using this linear model. So our multiple linear regression is better at predicting our current dataset than possibly one of the independent variables on its own. However the lack f significant variables is evidence of overfitting. It fails to generalize and predict future data correctly. Also depending on the standards that the MechaCar company is looking for, having 70% of the variability could be too low of a standard for them. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Summary Statistics on Suspension Coils
![Code of Deliverable 2](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/Deliverable%202%20Code%20for%20both%20steps.png)
![total summary](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/Deliverable%202%20Total%20table.png)
![lot summary](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/Deliverable%202%20Table.png)

### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
When we look at the total summary of the data related to PSI we see that the variance of the suspension coils does not exceed 100 pounds per square inch. It complies with this standard and we can see that the variance is 62.29. However when we look at the Variance of each individual lot we then see that this is not the case for all lots. Lot 1 and Lot 2 both still hold themselves to this standard, but Lot 3 has a Variance of 170.28 with the PSI. So as a total, the manufacturing lots meet the design specifications, but looking deeper, all but Lot 3 are meeting the design specifications. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## T-Tests on Suspension Coils

### An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population
![Lot T tests](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/t%20test%20all%20lots.png)
### An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population
![Lot T tests](https://github.com/Andrew-E-Walters/MechaCar_Statistical_Analysis/blob/main/FOR%20RESUBMIT%20%20UPDATED%20T%20TEST.png)

### Summary of the t-test results across all manufacturing lots and for each lot
We have run a T-Test on not only all of the lots against the mean PSI of the population but each lot itself against the population. The one-sample t-test is used to determine whether there is a statistical difference between the means of a sample dataset and a hypothesized, potential population dataset. The Null Hypothesis is that there is no statistical difference between the observed sample mean and its presumed population mean. The Alternative Hypothesis is there is a statistical difference between the observed sample mean and its presumed population mean.

We can use the one sample t-test to assert our data as long as most of these assumtions are met. 
1. The input data is numerical and continuous. This is because we are testing the distribution of two datasets.
2. The sample data was selected randomly from its population data.
3. The input data is considered to be normally distributed.
4. The sample size is reasonably large. Generally speaking, this means that the sample data distribution should be similar to its population data distribution.
5. The variance of the input data should be very similar.

With the assumtion that our significane level was 0.05 percent we can use or p-value to determine the signifigance level. 

When it comes to the total for that compares all manufacturing lots against the mean PSI we can see it is a signifigant p-value and accept the Null Hypothesis. 
We can also accept the null Hyopthesis for Lot 3 as it p-value was signifigant. Where we would have to reject the null, and accept the alternative is with Lot 1 and Lot 2. In this case the Null was that the the mean is equal to the mean of the total population mean PSI of 1500. The Alternative Hypothesis is that the true mean is not equal to 1500. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Study Design: MechaCar vs Competition
We are going to see how MechaCar vehicles perform compared to other vehicles when it comes to their highway miles per gallon efficiency.
### What metric or metrics are you going to test?
To test how MechaCar compares to the competition we are going to be looking at the MPG values of the vehicles that MechaCar produces as well as MPG data fromn the auto industry and their competition. 
### What is the null hypothesis or alternative hypothesis?
In order to find out if there is a diffrence we would need to gather the data and test it against a Null hypothesis as well as provide an alternative hypothesis. 
The Null Hypothesis would be: MechaCars have a satistically signifigant diffrence in the fuel efficiency then the mean of other manufacurers fuel efficiency.
The Alternative Hypothesis would be: MechaCars do not have any more fuel efficiency than the mean of other manufacturers fuel efficiency.
### What statistical test would you use to test the hypothesis? And why?
In order to test this, I would gather MPG data on MechaCars and all other manufacturers. Once we have a large enough data set, we will test the mean MPG of each class of Mecha Cars to the Mean of the total MPG of all cars. This would be a one sample T-test that would tell us if there is a statistical diffrence between the mean of the sample distribution and the mean of the populatiuon distribution. We could also test using a 2 sample T-test and compare MechaCars to one other manufacturer to see how they do against the competition. Depending on the results we would then either reject or accept the null hypothesis that MechaCars have a better MPG fuel efficiecny compared to the rest of the auto idustry/competition.
### What data is needed to run the statistical test?
We would need MPG data from the auto industry so we can gather a Mean MPG of the population of vehicles. We would also need which manufactuer it came from so we would have sample Means to test against our MechaCar MPG. 
