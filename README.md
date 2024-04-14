# Survival analysis of Veteran disease trials (in slovak)


## Introduction

In this protocol, we will attempt to analyze censored data on the treatment of veterans. Specifically, our task is to analyze patients over the age of 60 (age>60) with standard treatment (treat=1) vs with placebo treatment (treat=2). We will solve the following tasks:

- Estimation of survival time in the given two groups using parametric and non-parametric methods for censored data.
- We will compare characteristics such as MTTF, median survival times, survival function, etc. between the mentioned groups.
- We will try to apply the Cox PH model if possible.

### Highlights
![lifetime_plot](https://github.com/Many98/Survival-analysis-Veteran-disease-trial-/assets/65658910/a617f7b9-1525-43f8-9584-123f01ed7288)
![caplan_meier](https://github.com/Many98/Survival-analysis-Veteran-disease-trial-/assets/65658910/979ade9b-9728-4d44-9f9f-5f862025ab0a)

![mre](https://github.com/Many98/Survival-analysis-Veteran-disease-trial-/assets/65658910/538eda01-da72-44ef-85d0-e71bb133d46e)

![rmst](https://github.com/Many98/Survival-analysis-Veteran-disease-trial-/assets/65658910/b13bd00b-1844-4bff-8406-3529e4da58c8)


### Conclusions

In this protocol, we analyzed survival times from a clinical study of veterans (Veteran disease trial), specifically we compared patients in the age category over 60 years within the placebo and standard treatment groups. We used non-parametric as well as parametric methods to estimate the survival function. In the case of parametric models, we were forced to use a piece-wise exponential model. Characteristics such as (mean time to failure) or (median survival time) indicated a minimal improvement in average survival times in the case of treatment with the tested procedure instead of placebo. 

An interesting finding was that in the case of treatment with the standard tested procedure, there is a kind of critical area of survival times where there is a sudden change in the expected median residual life (median residual life). In the case of estimation using the Kaplan-Meier method, this critical area is roughly between the 150th and 160th day of survival. Estimates of median residual life specifically indicated for patients with standard treatment that if they survive 150 days, they have a 50% probability of surviving at least another 25 days, while if the patient survived days, there is already a 50% probability of surviving at least another 250 days, which is considerable increase. 

A similar conclusion regarding a critical area also applied to the placebo group, but it was less pronounced. What caused such a trend is not clear to us and should be investigated with the help of considering the effects of other variables in the dataset. We did not perform such an analysis, as after examining the loglog graph of the survival function, it turned out that the assumptions of the Cox PH model were not met, and therefore its use or the use of the log-rank test to compare groups may have led to misleading conclusions. As a further comparison of survival times in both groups, another integral characteristic known as restricted mean survival time RMST(t_0) was proposed. The difference in the RMST(300) characteristic for both groups again, in our opinion, indicated the minimal effectiveness of the treatment compared to placebo.
