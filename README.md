# MechaCar_Statistical_Analysis

![Screenshot 2022-11-16 at 5 33 38 PM](https://user-images.githubusercontent.com/109354592/202317762-2e726893-baa0-4c1a-96f8-99d156de737e.png)

# Overview of Project
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.   

## Deliverables
This prpject consists of three technical analysis, and a proposal to further analize company data.

1. #### _**Deliverable 1**_: Linear Regression to Predict MPG
2. #### **_Deliverable 2_**: Summary Statistics on Suspension Coils
3. #### **_Deliverable 3_**: T-Test on Suspension Coils
4. #### _**Deliverable 4**_: Design a Study Comparing the MechaCar to the Competition

## Resources
* Data Source: **`MechaCar_mpg.csv`** and **`Suspension_Coil.csv`**
* Data Tools: [`tidyverse`](https://www.tidyverse.org/), [`dplyr`](https://dplyr.tidyverse.org/), [`ggplot2`](https://ggplot2.tidyverse.org/) and [`MechaCarChallenge.RScript.R`](https://github.com/jbailey2705/MechaCar_Statistical_Analysis/blob/main/MechaCarChallenge.RScript.R).
* Software: [`RStudio`](https://posit.co/) and [`R`](https://cran.r-project.org/)

## Deliverable 1:
### Linear Regression to Predict MPG
**`MechaCar_mpg.csv`** dataset contains mpg test results for 50 prototype MechaCars, measuring the miles per gallon across multiple variables. R in RStudio was used to calculate and show the linear regression.

To deliver the findings the following steps were followed:
* **`MechaCar_mpg.csv`** was imported and read into a DataFrame
*  RScript was written to show a linear regression model, performed on six variables
*  RScript was also written to show statistical summary of the linear regression model with the intended p-values
*  Writtem summary covering the three questions

## MechaCar_DataFrame

![MechaCar_DataFrme](https://user-images.githubusercontent.com/109354592/202325917-81588d58-5a3a-47b3-8bb6-e3c1dc96c37c.png)

## Statistical Model

**mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)**

![linear_regression_model](https://user-images.githubusercontent.com/109354592/202329003-5b21c038-694b-4961-83f7-8ea8d639787e.png)

![summary_statistics](https://user-images.githubusercontent.com/109354592/202326007-504bb0db-77af-4ef1-bdb5-6fda7ebba1bb.png)


## Statistical Summary

From the data above we can see that:

- The vehicle length, and ground clearance are likely to provide non-random amounts of variance to the model. That is, the vehicle length and ground clearance have a significant impact on miles per gallon on the prototype. The _**vehicle weight**_, _**spoiler angle**_, and _**All Wheel Drive**_ (AWD) have p-Values that show to have random amounts of variance with the dataset presented
- **`P-Value: 5.35e-11`**, is much smaller than the assumed level of **0.05%**. This indicates there is enough evidence to reject our null hypothesis, which indcates that the slope on this linear model is not zero.
- The linear model has a r-squared value of **0.7149**, approximately **71%** of all mpg predictions will be determined by this model. The multiple regression model does predict mpg of MechaCar prototypes effectively.

## Deliverable 2:
### Summary Statistics on Suspension Coils

The **`Suspension_Coil.csv`** dataset shows results for multiple production lots. The wight capabilities of various suspension coils have been tested to determine if the manufacturing process is consistent across each of the production lots sampled.

* Suspension coil’s PSI continuous variable across all manufacturing lots
* PSI metrics for each lot: mean, median, variance, and standard deviation.

### Technical Analysis

The summary statistics of all of the manufacturing lots. The mean is **1498.78** for this sample and the population mean was determined to be **1500**.

![Total_Summary](https://user-images.githubusercontent.com/109354592/202792567-cf94f710-47fe-4ffe-9dbf-619f14b45a68.png)

### Summary by Manufacturing Lot Number

The means of the lot numbers are similar to the population mean as well as the sample mean.

![Lot_Summary](https://user-images.githubusercontent.com/109354592/202792730-e3faaeb5-d38f-4b7d-a2b4-73652ba0e331.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current data meet this design specification for all manufacturing lots, in total, and each lot individually?

The variance for the total manufacturing lot is **62 < 100**, which is within the expected design specifications of staying `under 100 PSI`. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of **170 > 100** and does not meet the design specifications. 
Lot 1 and Lot 2 have significantly lower variance, than 1 and 7 respectively.

## T-Tests on Suspension Coils

### T-test for all Lots

Manufacturing Lots: p-value = .6028, alpha = .05

.60 > .05, the total manufacturing lot **is not** statistically significant from the normal distribution, and normality can be assumed. While the mean falls within the 95% confidence interval.

![T-Test](https://user-images.githubusercontent.com/109354592/202795743-676e93a6-5827-469e-8b25-dcdbdc28063c.png)

### T-test for Lot 1

![t-test_Lot_1](https://user-images.githubusercontent.com/109354592/202795929-a7df2692-1b35-40a8-96e7-5888b069c491.png)

## T-test for Lot 2

Lot 2: p-value = .6072, alpha = .05

.60 > .05, Lot 2 **is not** statistically significant from the normal distribution and normality can be assumed. While the mean falls within the 95% confidence interval.

![t-test_Lot_2](https://user-images.githubusercontent.com/109354592/202796191-51e9c08b-6fe6-40ed-9fa7-a8fc0e12b3a5.png)

## T-test for Lot 3

Lot 3: p-value = .04168, alpha = .05

.04 < .05, which means **it is** statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

![t-test_Lot_3](https://user-images.githubusercontent.com/109354592/202796358-45f8e038-5416-4d85-9461-ead539b81a70.png)

Ooverall, Lots 1 & 2 show a normal distribution. There is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.

## Study Design: MechaCar vs Competition

When comparing MechaCar to its competitor’s some other metrics that may be of interest to consumer's, include cost,  color of vehicle, city/highway fuel efficiency, horsepower, average cost of repair, and safety rating.

1. What metric or metrics are being tested?
  - The metrics to test should be horsepower, safety rating, and city/highway fuel efficiency, these could address some of the safety concerns consumers may have when buying a vehicle.

2. What is the null hypothesis or alternative hypothesis?
 - The null hypothesis is that the mean of the safety rating is zero. The alternative hypothesis is that the mean of the safety rating is not zero.

3. What statistical test would you use to test the hypothesis? And why?
  - A multiple linear regression statistical summary will show the variable impact of the safety ratings for MechaCar and competitors.

4. What data is needed to run the statistical test?
   - Random sample of n > 30 for MechaCar and each competitor would need to be collected, include the safety ratings, city/highway fuel efficiency, and horsepower, also, running the data through RStudio.

