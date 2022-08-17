# Reference Standards for Rating of Perceived Exertion During Exercise Testing: Data from the Fitness Registry and the Importance of Exercise International Database (FRIEND)

## Summary:
Rating of perceived exertion (RPE) is collected during exercise testing to monitor a subject's status. Peak RPE can also be used to indicate whether a subject performed a maximal effort during a cardiopulmonary exercise test (VO<sub>2max</sub> test). However, no study to date had reported the distribution of peak RPE values across a diverse cohort of individuals. **This study provides the first normative reference standards for peak RPE in healthy individuals performing a maximal exercise test on a treadmill or cycle ergometer.**

## The Rationale:
Monitoring rating of perceived exertion (RPE) during an exercise test is valuable as it is related to objective measures of exercise intensity independent of sex, age, exercise mode, and physical activity status. Furthermore, for maximal exercise tests, peak RPE is commonly used as a subjective indicator of whether a participant performed a maximal effort.

RPE is a measure that is commonly collected and reported by researchers and clinicians. Traditionally, a scale of 0–10 or 6–20 (the Borg scale) is used to assess RPE. When using the Borg scale, a peak RPE of ≥18 is traditionally used to define sufficient effort during a maximal exercise test. However, no study to date has reported reference standards or the distribution of peak RPE values from the Borg scale across a diverse cohort of individuals. **Thus, the purpose of this study was to provide peak RPE reference standards for the Borg scale for males and females performing an exercise test on either a treadmill or cycle ergometer.**

## The Process:
### Dataset creation.
The data for this study comes from [FRIEND (an international database of fitness tests)](https://jimpeterman-friend-app-app-m9w2iq.streamlitapp.com/). 

The dataset creation relied heavily on the Python packages pandas and numpy. Data were filtered to tests that involved the Borg scale and to meet the other inclusion criteria of the study (e.g., exercise test performed on a treadmill or cycle ergometer, aged 20-90 years old, etc.).

### Analysis
Reference standards were created along with summaries of other related variables. Python's statsmodels package was used to compare peak RPE across age groups, sexes, and exercise modes. Figures were created using matplotlib and seaborn.

I also explored potential trends in those who reported low peak RPE values (<17) and explored longitudinal trends in RPE for those who performed two exercise tests using the same mode. Nothing particularly noteworthy was observed and the results were not included in the subsequent publication.

## The Final Product/Results:
The mean and median peak RPE for each sex, age group, and test mode was between 18 and 19, consistent with traditional definitions of sufficient maximal effort. The figure below illustrates the distribution of peak RPE values across combined treadmill and cycle ergometer CPX:

![figure_1](images/fig_1.tiff)

Some statistically significant differences were observed in peak RPE between age groups and between sexes. However, these small, statistically significant differences in peak RPE are presumably due to the substantially large sample size (9,551 tests) and it is unlikely that these differences are clinically relevant. 

Lastly, statistically significant correlations were found between peak RPE and other exercise test variables, including VO<sub>2max</sub> and peak heart rate as a percentage of age-predicted max (highlighted below). Again, despite the statistical significance, the correlations were weak and overall suggest peak RPE is largely independant of these variables.

![figure_2](images/fig_2.tiff)

Overall, this study produced reference standards for peak RPE when using the 6 – 20 Borg scale and found consistency in peak RPE responses during maximal exercise testing. I summarized these findings and submitted the manuscript to Medicine & Science in Sports & Exercise where it was accepted for publication following peer review by experts in the field [the publication can be found here](https://journals.lww.com/acsm-msse/Abstract/9900/Reference_Standards_for_Peak_Rating_of_Perceived.105.aspx). Following publication, these reference standards may improve exercise test interpretations, especially in settings that rely on subjective indicators like RPE to determine if a participant/patient achieved maximal effort.


