# Explore Racial Disparities at Police Stopes in th US
This is a project for my studies. The aim of the project is to find patterns of association between probability to get searched at police stops and subject's race and other explanatory variables subject's sex and age and officer's race and sex, and their interactions. The sample used for this analysis is police stops in Louisville from 2015 January to 2018 January. 

## Introduction
The aim of this project is to take a closer look into racial disparities at police stops in the US, exploring how other variables might effect the association between probability of getting searched and driver's race. Racial discrimination has always been a topic in the US. Especially after the murder of George Floyd in May 2020, Black Lives Matter movement gained much more international attention. The data set that is used for this project is from [The Stanford Open Policing Project](https://openpolicing.stanford.edu/data/). There are already some findings about the racial disparities regarding stop rates, search decisions, etc. In this project I am specifically interested in the disparities between black and white drivers, and I will particularly focus on how other variables such as driver's gender and age, officer's race and gender would effect the association between the probability of getting searched and driver's race at police stops, with the hope that I might be able to find something new than what has already been done.

## Data
To achieve the aim of this project, I specifically picked the data set for Louisville, where data for all the other control variables that I am interested in are also available. The data set includes data of all the traffic stops from 2015-01-01 to 2018-01-28 in Louisville, KY. I did some data cleaning and munging to filter out all the NA values, focus only on sample with drivers either black or white, categorize officers as white and non-white and consider both *frisk performed* and *search conducted* as *get searched*.

## Models and Interpretation
The pattern of association between y and the only one continuous variable subject_age (see graph in Appendix) seems close to be linear, so there is no need to use splines or polynomials. Therefore, I start building regression models.

## External Validity (Robustness Check)
The second data set I used includes data of all the traffic stops with drivers being either black or white from 2009-01-01 to 2015-12-31 in Washington Statewide. The slope coefficient for driver's race is similar to our model for Louisville previously. This suggests that for other time intervals and other regions in the US, the external validity of the model is quite high, we might expect similar slope coefficient for driver's race.

## Conclusion
In general, unsurprisingly when controlling on driver's gender, officer's gender and race, black drivers are expected to be around 3% more likely to get searched than white drivers on average. What's new for me is, we expect the disadvantage for black drivers regarding probability of getting searched to be lower when the driver is female instead of male and when officer is non-white instead of white, whereas driver's age and officer's gender have no statistically significant effect on the matter. Last but not least, within the US, it is assumed that the external validity of the preferred regression model to be quite high, we might expect similar slope coefficient for driver's race for other regions in the US.

