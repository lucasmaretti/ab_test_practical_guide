This notebook was designed with the intention of providing a clear framework for those learning about experimentation and A/B testing. After taking several courses on the subject and then reading the most cited references in the area, I realized that most courses teach A/B testing in a confusing matter, often falling prey to some of the "intuition busters" mentioned by Kohavi et al. on the paer "A/B testing intuition busters - Common misunderstanding in Online Controlled Experiments". The idea is to provide a clear step-by-step of the correct order in which to proceed with the analysis as well as providing clear and correct definitions of the most common concepts used in A/B testing such as p-values, statistical power and others.

## Table of contents

1. [Introduction](#introduction)
2. [Data description](#data)
3. [Scenario description and goals](#statement)
4. [Hypothesis testing](#wrangling)
5. [Conclusions](#conclusions)
6. [References](#licensing)

## Introduction <a name="introduction"></a>

A/B testing, also known as split testing, is a method used to compare two versions of a webpage, app feature, or any other product aspect, to determine which one performs better. In its simplest form, A/B testing involves showing version A (the control) to one group and version B (the variant) to another group. By comparing how the two groups respond, we can infer which version is more effective given a pre-defined metric that we use as evaluation.

This approach can help to answer critical questions and hypotheses and reduce guesswork in decision-making. By testing the impact of changes on real users, organizations can optimize their products and services based on actual user responses rather than assumptions, or as mentioned by Kohavi et al on the paper *Controlled experiments on the web: survey and practical guide*: "Our experience indicates that significant learning and return-on-investment are seen when development teams listen to their customers, not to the Highest Paid Person's Opinion (HiPPO)".

## Data description <a name="data"></a>

Data provided by Udacity in their Data Scientist Nanodegree course under creative commons license.

## Scenario description and goals <a name="statement"></a>

*Scenario description*

We work for a software company that is looking for ways to increase the number of people who pay for their software. The way that the product is currently offered, users can download and use the software free of charge, for a 7-day trial. After the end of the trial, users are required to pay for a license to continue using it.

An idea that the company wants to evaluate is to change the layout of the homepage to emphasize more prominently that there is a 7-day trial available for the software. The current fear is that some potential users are missing out on using the software because of a lack of awareness of the trial period. If more people download the software and use it in the trial period, the hope is that this will encourage more people to make a purchase after seeing what the software can do.

*Goal of the study*

The first thing we should do is specify the objective or goal of our study:

 - Revising the structure of the homepage will increase the number of people that download the software and, ultimately, the number of people that purchase a license.
   
### Hypothesis testing <a name="modelling"></a>
Null hypothesis (H0): The average download and license purchase rates between the old design and the new design that emphasizes the 7-day trial are the same.

Alternative hypothesis (HA): The average download and license purchase rates between the old design and the new design that emphasizes the 7-day trial are different.

## Conclusions <a name="conclusions"></a>
We found that there was a statistically significant difference in download rates, but not in license purchasing. We can hypothesize that the change we made in our website increases awareness on our product for the 7-day trial but did not contribute to people buying it more. In order to confirm this we would need more data and checking, for example the demographics of people who try out and buy the product to try to understand preferences. Also, when concluding about the results of the experiment it is important to analyze the tradeoff between statistical and practical significance. While statistical significance tells us whether the observed effect in an A/B test is likely not due to random chance, practical significance delves into whether the effect is large enough to be meaningful in a real-world context. For example, if we decide to change the homepage, we have to think about questions like how much will it cost to develop and rollout the changes and if we have the budget for it; what type of resources will it demand; does it align with long-term strategy of the business? And so on.

In summary, while statistical significance is essential for validating the results of an A/B test, practical significance is key to determining the real-world impact of those results. Balancing these two aspects ensures that the insights gained from A/B testing are both scientifically valid and strategically valuable, leading to more informed and effective decision-making.


## References <a name="licensing"></a>

[1] Kohavi, Ron, et al. "Controlled experiments on the web: survey and practical guide." Data mining and knowledge discovery 18 (2009): 140-181.
[2] Kohavi, Ron, Alex Deng, and Lukas Vermeer. "A/b testing intuition busters: Common misunderstandings in online controlled experiments." Proceedings of the 28th ACM SIGKDD Conference on Knowledge Discovery and Data Mining. 2022.

