# Derbyshire-Crime-Analysis-using-R

### Introduction

The aim of this project is to analyze the crime data set from different regions in Derbyshire. The objectives of this project are to: 

 - Gain a better understanding of the data set through descriptive visualizations 
 - Evaluate the relationship between variables in the data set using linear regression.


### Dataset Description
The provided dataset includes data on the number of criminal incidents that have been reported in various Lower Layer Super Output Areas (LSOAs) of Derbyshire. The dataset contains 642 observations and 18 variables. 

### Summary Statistics - Normality Distribution

Skewness is a measure used to fact check how the data deviates from a normal distribution (Gawali, 2021). The tail of the distributions as shown in the Density plot below are longer on the positive side which is indicative that the crime variables are positively skewed.


Figure 1: Density Plot of the Crime Data
![Density Plot](https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/3973f643-a97c-4955-8f43-863622c551e9)


This phenomena of the data led to the decision of log transforming the data. Log transformation is a method used to reduce the skewness of the data. It helps to achieve a much more closer bell curve as shown below (Htoon, 2020):

Figure 2: Density Plot of the Log Transformed Crime Data
![Log Transformed Density Plot](https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/a2d31d1c-68d0-406c-8749-8a41853bb5eb)

The log transformation has reduced the skewness of the variable distribution. The means are lower than their medians, indicating negative skewness. The upper half of the data is more dispersed than the lower half.

### Simple Linear Regression
The positive slope coefficient (β1) for each crime type shows a correlation between population and crimes. The intercept for each model is negative, indicating that crime rates remain lower than the area's normal rate even with zero population. The models fit the data well with R-squared values ranging from 0.5972 to 0.8772, accounting for 59.72% to 87.72% of the variation in dependent variables.


| Crimes | β0 | β1 |Multiple R-squared | Adjusted R-squared |
| :--- |:---: |:---: |:---: |:---: |
| Anti- Social Behavior | -1.8251	 | 1.1483	 | 0.8271	 | 0.8269 |
| Burglary | -2.3017	| 1.0029	| 0.828	| 0.8278 |
| Robbery	| -3.1896	| 1.1490	| 0.8774	| 0.8772 |
| Vehicle crimes	| -2.3595	| 1.0246	| 0.8403	| 0.84 |
| Violent crimes	| -1.8708	| 1.1862	| 0.8532	| 0.853 |
| Shoplifting	| -2.9528	| 1.1448	| 0.5978	| 0.5972 |
| Criminal.Damage...Arson	| -2.3063	| 1.1246	| 0.8322	| 0.832 |
| Other theft	| -2.3096	| 1.0034	| 0.7592	| 0.7588 |
| Drugs	| -2.8459	| 1.0081	| 0.7824	| 0.782 |
| Other Crimes	| -3.159	| 1.144	| 0.8501	| 0.8499 |
| Bike theft	| -2.8323	| 1.0755	| 0.8301	| 0.8299 |
| Possession of Weapons	| -3.0845	| 1.0959	| 0.8685	| 0.8683 |
| Public order	| -2.5385	| 1.1412	| 0.7997	| 0.794 |
| Theft from the Person	| -3.1370	| 1.0746	| 0.8566	| 0.8564 |


- Linearity: Linear regression assumes a linear relationship between the dependent and independent variables. If the relationship is nonlinear, using a linear regression model may produce unreliable results. For the models, the assumption of linearity holds.


