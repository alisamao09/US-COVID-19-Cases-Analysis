# US-COVID-19-Cases-Analysis

## Overview
As is a contagious disease caused by a virus, the severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2), Coronavirus disease 2019 (COVID-19) was first identified in Wuhan, China, in December 2019. The disease has since spread worldwide, leading to the ongoing COVID-19 pandemic[1]. Of those people who develop symptoms noticeable enough to be classed as patients, most (81%) develop mild to moderate symptoms (up to mild pneumonia), while 14% develop severe symptoms (dyspnea, hypoxia, or more than 50% lung involvement on imaging), and 5% suffer critical symptoms[2]. Older people are at a higher risk of developing severe symptoms.

## Problem Statement
The goal of this final project is to investigate the potential patterns of COVID-19. We want to examine the following question:
**Can COVID-19 be well modeled by SARIMA and/or SEIR models?**

## Conclusion
* After our research, we can conclude that both SARIMA and SEIR models can well model COVID-19 daily cases. In our analysis, we use AIC values to select the parameter settings of the SARIMA model and use local and global search to fit our SEIR model. Based on the analysis, the SARMA model is able to achieve a log likelihood of -3672.181 while the SEIR model results in a log likelihood of -3684.733.

* The reason that the SARIMA model has a higher log likelihood compared with the SEIR model is that we make some assumptions in the SEIR model that go against reality in order to simplify it. This affects the accuracy of the model to some extent, but the SEIR model still fits the data well. This is due to the variables beta and mu, as they reflect the influence of masks, vaccines, and mutant viruses on the infection rate. From loglik’s point of view, the SEIR model does not seem to perform as well as the SARIMA model. As project 15 in 2021 said, this may be caused by the SEIR model ignoring periodicity. Of course, there are other factors worth adding to the model, such as weather changes, since people tend to congregate indoors in winter, and/or the flow of people.

* COVID-19 is a complicated disease to analyze. Therefore, in further investigations, we plan to add more parameters as well as use different compartment models to capture the complexities of this disease.

## References
[1] Zimmer C (26 February 2021). “The Secret Life of a Coronavirus” An oily, 100-nanometer-wide bubble of genes has killed more than two million people and reshaped the world. Scientists don’t quite know what to make of it". Archived from the original on 28 December 2021. Retrieved 28 February 2021.

[2] Interim Clinical Guidance for Management of Patients with Confirmed Coronavirus Disease (COVID-19)". U.S. Centers for Disease Control and Prevention (CDC). 6 April 2020. Archived from the original on 2 March 2020. Retrieved 19 April 2020.

[3] Lecture slides - Chapter 5: Parameter estimation and model identification for ARMA models, slides 21 - 29.

[4] Lecture slides - Chapter 4: Linear time series models and the algebra of ARMA model, slides 16 - 17.

[5] Lecture slides - Chapter 6: Extending the ARMA model: Seasonality, integration and trend, slides 3 - 9, 15.

[6] Final project w21 project 15: https://ionides.github.io/531w21/final_project/project15/blinded.html

From [6] in 2021, we learn that the SEIR model has good results on the COVID-19 data. We will follow their example to build a similar model. In order to capture the emergence of Omicron, we made changes on the code of the SEIR model.

[7] United States Population https://www.worldometers.info/world-population/us-population/

[8] SEIR model for COVID-19 dynamics incorporating the environment and social distancing https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7376536/

[9] Lecture slides - Chapter 15: A case study of polio including covariates, seasonality & over-dispersion, slides 46 - 49.
