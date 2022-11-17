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









