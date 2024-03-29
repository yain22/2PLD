# Optimization of dose selection using multiple surrogates of toxicity as a continuous variable in Phase I cancer trial

![](Images/Patients.png)

## Contents
* [Overview](#Overview)
* [Introduction & Results](#introduction--results)
* [References](#References)

## Overview

The present work is a research that I had conducted as a Pharmacometrics Intern at Pharmacometry Team at [Merck Group](https://www.emdgroup.com/en), supervised by Kosalaram Goteti, Ph.D. I was a third year Ph.D. student at Texas A&M University. This work has been accepted to [American Conference on Pharmacometrics 2020](https://www.go-acop.org/): abstracts of accepted works at ACoP11 can be downloadable from [here](https://github.com/yain22/2PLD/blob/main/Poster/ACoP_Poster%20Abstracts_v4.pdf). Published poster article can be downloaed at [here](https://github.com/yain22/2PLD/blob/main/Poster/ACOP_Se_Yoon_Lee_PhD.pdf). Illustration video can be downloaed at [here](https://github.com/yain22/2PLD/blob/main/Video/ACOP_Video_Se_Yoon_Lee_PhD.mp4). The full reseach article has been published in a top medical journal "Contemporary Clinical Trials" [Impact factor : 2.226]": Download at [here](https://www.sciencedirect.com/science/article/pii/S1551714421003931). Full slide of the published work can be download at [here](https://github.com/yain22/2PLD/blob/main/Presentation/2PLD_Slides_SeYoon_Lee_PhD.pdf).

To cite our work, refer with the following:

**Se Yoon Lee, Alain Munafo, Pascal Girard, Kosalaram Goteti, "Optimization of dose selection using multiple surrogates of toxicity as a continuous variable in Phase I cancer trial", Contemporary Clinical Trials (2022)**

## Introduction & Results

For a phase I cancer clinical trial, the number of patients is sharply confined. For this reason, proper exploitation of toxicity information from each of the patients is crucial in designing an adaptive clinical trial. In such a phase I study we have to consider that treatment effect may not be known for months, possibly years, after enrollment: whereas, toxic reactions manifest in terms of days, weeks, or months rather than years. 

Because there is no immediate possibility of assessing the relative advantages of the treatment against its toxic disadvantages, the pharmacological underpinning of a new drug candidate mainly relies on a toxicity-dose curve which describes a relationship between toxicity and dose. The main goal of the phase I studies is to estimate the maximum tolerated dose (MTD), or the highest dose at which a pre-specified level of risk of toxicity is not exceeded.

![](Images/Dose_search_procedure.png)

In this study of simulation, we consider a fully sequential design setting where patients are introduced to the trials individually and sequentially, and each patient is assigned with an estimate of the MTD based on the accumulated patient’s information at interim. To protect patients from being overdosed, a drug is initiated at a very low dose and slowly escalated toward the targeted MTD as the trials go on. 

Two typical pioneering Bayesian adaptive designs for the phase I cancer clinical trials are (i) continual reassessment method (CRM) and (ii) escalation with overdose control (EWOC). Drawbacks of CRM and EWOC are as follows: (i) adverse event is recorded with a binary response: DLT (dose limiting toxicity) or non DLT and (ii) they cannot accommodate grade information for multiple adverse events (AE). To accommodate grade information from multiple AEs, recently, EWOC using normalized equivalent toxicity score (EWOC-NETS) was developed. Because EWOC-NETS is based on a pseudo-Bernoulli likelihood, its drawback is that the results cannot be reproduced by simulation. In this study, we propose a two- parameter linear dose-finder (2PLD) to address a continuous toxicity response in the phase I cancer clinical trials. The 2PLD assumes a linear relationship between a toxic reaction and a dosage (or possibly an exposure). 2PLD treats the toxicity response as a continuous variable, aimed at utilizing Common Toxicity Criteria for Adverse Events provided by the National Cancer Institute. The proposed search procedure suggests an optimal exposure to each patient by using accrued patient’s information while controlling the posterior probability of overdose.

![](Images/A_result.png)

The simulations show that this novel 2PLD method has good operating characteristics and improved accuracy in achieving MTD. Simulations showed that the 2PLD requires a fewer step to converge to the targeted MTD than using adaptive clinical trial design methods that are based on binary responses such as EWOC or CRM. This novel 2PLD can be an attractive tool for clinical scientists because of its parsimonious description of a toxicity-dose curve, medically interpretable hyperparameters, and an automated posterior computation.

## References

[1] Se Yoon Lee, Shankar Lanke, Alain Munafo, Pascal Girard, Kosalaram Goteti, "Optimization of dose selection using multiple surrogates of toxicity as a continuous variable in Phase I cancer trial", ACoP11, ISSN:2688-3953, Vol 2 (2020)

[2] Se Yoon Lee, Alain Munafo, Pascal Girard, Kosalaram Goteti, "Optimization of dose selection using multiple surrogates of toxicity as a continuous variable in Phase I cancer trial", Contemporary Clinical Trials (2022)

[3] Babb, James, André Rogatko, and Shelemyahu Zacks. "Cancer phase I clinical trials: efficient dose escalation with overdose control." Statistics in medicine 17.10 (1998): 1103-1120

[4] O'Quigley, John, Margaret Pepe, and Lloyd Fisher. "Continual reassessment method: a practical design for phase 1 clinical trials in cancer." Biometrics (1990): 33-48 

[5] Rosenblum, Michael, et al. "Adaptive design in surveys and clinical trials: similarities, differences and opportunities for cross‐fertilization." Journal of the Royal Statistical Society: Series A (Statistics in Society) 182.3 (2019): 963-982
