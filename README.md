# Does sleep quality and number of drinks affect the depression score?
Exploratory and statistical analysis on the effects of sleep quality and number of alcoholic drinks on the depression score of a college student

Tecchniques used:
- Data Wrangling and Transformation
- Data Visualization
- Data Modeling
- Bootstrapping

## Abstract

I investigated whether poor quality sleep and alcohol use have an effect on depression, using the dataset “SleepStudy” from the RStudio package dataset library “Lock5Data”. The data is from a study of sleep patterns for 253 college students. In this investigation, I have found that quality of sleep has a significant effect on the depression score of students. I have also found a weak relationship between the alcohol use and depression score. These findings might be considered valuable for general public and add to a larger health and medicine knowledge

## Data 

I considered the quantitative variable Poor Sleep Quality score, which is a measure of sleep quality (higher values represent poorer sleep quality). I also considered the quantitative variable “Drinks”, which represents the number of alcohol drinks per week. There are two responses variables of interest: “Depression Status” and “Depression Score”. Both of these variables represent the same thing, and the only difference is in the type of variable.“Depression Status” is a categorical variable, while “Depression Score” is quantitative. This data set contains 253 observations and 27 variables. I have filtered out the original data and selected only four variables of interest. The table below displays the mean and standard deviation in Poor Quality Sleep scores and drinks per week for each Depression Status.

![table](https://user-images.githubusercontent.com/94130159/152214079-dc91809b-1dda-473b-9974-4ef9ae8a042f.jpg)

![denstiy plot](https://user-images.githubusercontent.com/94130159/152214314-8dda0f90-1aef-4c48-aed1-3102190471b3.jpg)

![sleep-depr](https://user-images.githubusercontent.com/94130159/152214472-f15fa6f8-6854-4b6e-804a-e086b4bd7fed.jpg)

![drink_depr](https://user-images.githubusercontent.com/94130159/152214489-17c175e6-ed42-48e5-a50e-1a50d1a9a8d7.jpg)


## Model fitting

I fit two models. One without an interaction term between PSQ (Poor Sleep Quality) score and number of drinks per week, and one with the interaction term. 

Model 1 includes PSQ and number of alcoholic drinks as fixed effects. No interaction term. Here's the table of coeffiecients:
![table111](https://user-images.githubusercontent.com/94130159/152215877-77287f77-6b3a-42c7-84e2-895746dddb90.jpg)


Model 2 includes an interaction term and the same fixed effects. Here's the table of model coefficients:
![table1](https://user-images.githubusercontent.com/94130159/152215096-22aab908-431d-4da2-a240-071b52de7c4f.jpg)

From the tables, I concluded that interaction term doesn’t really help explaining the model any better. That's why I'll use model 1.

## Bootstrapping

First, I need to calculate a confidence interval for the expected value of Depression score for a score of 15 in PSQ, considering student doesn’t drink. Then, I need to calculate a confidence interval for the the expected value of Depression score if a student drinks 20 alcoholic drinks per week, but has a PSQ score of zero.


![boot1](https://user-images.githubusercontent.com/94130159/152216504-b113d6d5-c539-49bc-8fe0-47985522f1e3.jpg)


![boot2](https://user-images.githubusercontent.com/94130159/152216511-fb8aef5e-b657-41fe-996a-adc73da99c3f.jpg)


## Conclusion

This investigation was trying to find if there are any effects of Poor Quality Sleep and number of drinks er week on the Depression score and status. I have to note that most of the college students in this data set have low depression score and have indicated a normal depression status, which impacted my conclusions.

My study supports a largely known relationship between the quality of sleep and depression, however my results for the relationship between alcohol and depression are not significant enough. There is a potential for further studies especially for alcohol use and depression, and looking at how alcohol use could potentially lead to later development of depression.

