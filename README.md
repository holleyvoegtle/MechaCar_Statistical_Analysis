# MechaCar_Statistical_Analysis

## Purpose/Background
AutosRUs’ newest project, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutoRUs’ upper management has called on an the data analytics team to review the production data for insights that may help the manufacturing team. 

The team will do the following:
	•	Perform multiple linear regression analysis to identify which variable in the dataset predict the mpg of MechaCar prototypes.
	•	Collect summary statistics on the PSI of the suspension coils from 3 different manufacturing lots.
	•	Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
	•	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 

## Linear Regression to Predict MPG
A dataset is obtained that contains that results for 50 prototype MechaCars. The prototypes were produced using multiple design specifications to identify ideal vehicle performance. Metrics such as vehicle length, vehicle weight,  spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. With the use of R, a linear model was designed that could predict the mpg of MechaCar prototypes. 

![](https://github.com/holleyvoegtle/MechaCar_Statistical_Analysis/blob/main/images:graphs/output%20from%20linear%20regression%20DEL1.png)

### Questions 
The variables/coefficients that provided a non-random amount of variance to the mpg would be vehicle length and ground clearance due to the Pr(>ltl) value as seen in the output. This represents the probability that each coefficient contributes a random amount of variance to the linear model. According to the results, vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the linear model. Meaning, they have an impact on mpg. 

Since out p-values for vehicle length and ground clearance in less than 0.05%, this means the the slope of our linear model is not zero and is significant. 

Does this linear model predict mpg of MechaCar prototypes effectively? I would say that the model could predict the mpg due to our r-square value of 0.7149. combined with p-value, means the relationship is significantly significant. 



## Summary Statistics on Suspension Coils
The MechaCar Suspension coil csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. The following tables are seen below from the results of using R. The first table is the total summary table and the second is the individual lots. 

![](https://github.com/holleyvoegtle/MechaCar_Statistical_Analysis/blob/main/images:graphs/lot%20summary.png)
![](https://github.com/holleyvoegtle/MechaCar_Statistical_Analysis/blob/main/images:graphs/lot%20summary.png)

### Questions
Does the current manufacturing data meet the design specifications? The design specifications for the coils dictate that the variance of the suspension coils must not exceed 100 pound per square inch. Based on the results from this test, it would illustrate that the design specifications are met. But there are definitely anomalies in the results. For example, in the total summary, the mean and the median are very close in values but the variance is 62.29 which means the data is more dispersed from the mean with the standard deviation of 7.9. When we look at the individual lots we see that lot 1 and 2 have a small variance and standard deviation but lot 3 has a lot larger variance and standard deviation which could be there are some data points that are outliers. But overall I would say that the design speciations are correct but more information is needed. 

## T-Tests on Suspension Coils

### 
This section looked at running t-test on the 3 different lots of suspension coils and to test if each lot is significantly different from the population mean of 1,500 pounds per square inch. After performing 3 t-tests, the concluding result is that there is no significant difference between the first two lots (p-value is 1 and .6072) but there is a significant difference with lot 3 with a p-value = -.04168.  A value less than 0.05 means there is a significant difference from the other 2 lots. This can be seen below:

![](https://github.com/holleyvoegtle/MechaCar_Statistical_Analysis/blob/main/images:graphs/t-tests.png)

## Study Design: MechaCar vs Competition 

### 
The data for this particular study is very limited. So in order to get a more comprehensive assessment of the MechaCar prototypes, we could compare them to the competition. The metrics that could be used to expand our data would be to look at city vs highway fuel efficiency. How does MechaCar stack up with other car manufacturers? What about safety ratings? Mecha cars can be compared to how the competition performs in accidents or recalls or just overall safety. Another parameter of data that could be compared could be maintenance cost. How often are certain cars, make, model and class, in the repair shop? 

One of of null hypothesis to accept or reject would be through the use of the t-test. For example, one null hypothesis could be that there is no difference between fuel efficiency in the MechaCar with its main competitor when it comes to city vs highway. Through the use of a t-test we could statistically reject or accept our null hypothesis. To further build, our alternative hypothesis could be that there is a difference in fuel efficiency with MechaCar and its competitor. 

Another analysis we could perform if there was more data available would be through the use of linear regression and look at fuel efficiency over time as the car ages. If there are a multiple variables, then we would test to see it the significance level if appropriate which could lead to further collect of data and studies. 

