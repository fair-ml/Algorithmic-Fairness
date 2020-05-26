## Measuring Algorithmic Fairness: challenges and solutions for the industry

How can we quantitatively measure and mitigate algorithmic bias? 

The tutorial will focus on communicating real-world experience on assessing fairness throughout the machine learning model development life-cycle. It will cover innovative solutions for measuring and correcting algorithmic bias through hands-on exercises in a range of use-case scenarios from banking to policing.

### Tutorial Description

As machine learning models are employed to inform decisions in an increasingly wide range of human scenarios (e.g. banking, criminal justice, medicine and employment), it is very important to ensure that these decisions are equitable. This tutorial aims at providing the audience with an understanding of the nascent field of algorithmic fairness, by analysing the existing approaches in the literature, and complementing and critiquing them with lessons learned from our experience applying them in real-life situations, both in financial services and government agencies.

Exercises will focus on interesting lessons learned and will cover scenarios such as highly unbalanced datasets where the state-of-the-art metrics are not sensitive enough, how to understand the effect of the repair algorithms and when it makes business sense to use them and exactly for what purpose. We address the need to understand the source of bias prior any other steps and focus on alternative solutions to the repair algorithms.

### What makes algorithmic fairness worth the attention?

Algorithmic Fairness is an emerging area that is attracting a lot of attention, with academic publications in the topic increasing exponentially in the last 5 years, but we have very few examples of actually applying these approaches to industry, which is where the real value lies. Bias has become one of technology industries most notorious ethical issue and is receiving substantial coverage in the media, with some famous cases concerning some of the technology giants.

Even though unintended, algorithmic bias is most dangerous when it rules over critical systems such as predictive policing, hiring processes or medical applications. High efforts are directed towards understanding its sources and impact across these applications.

### Table of contents

* [Introduction to algorithmic fairness](#introduction-to-algorithmic-fairness)
* [Fairness Metrics Selection](#fairness-metrics-selection)
* [Bias Propagation and Evaluation Workflow](#bias-propagation-and-evaluation-workflow)
* [Challenges from Real-World Implementations](#challenges-from-real-world-implementations)
    * [Protected features and proxies](#protected-features-and-proxies)
    * [Metrics definition for unbalanced datasets](#metrics-definition-for-unbalanced-datasets)
    * [Data tranformation for bias mitigation](#data-transformation-for-bias-mitigation)
    * [False Positive Rate](#false-positive-rate)
    * [Importance of defined standards and thresholds when implementing](#importance-of-defined-standards-and-thresholds-when-implementing)
* [Other Fairness Relevant Resources and suggestions for further reading](#other-fairness-relevant-resources-and-suggestions-for-further-reading)

### Introduction to algorithmic fairness

Community of fairness-aware machine learning aims at developing automated-decision based systems that, once introduced into a social context, lead to fair and just outcomes. We outline the importance of a joint effort of multidisciplinary communities that will bring together ideas and insights from law, social and behavioural sciences combined with methodologies from the computer science field.

With this in mind, we kick off the session with a general overview of algorithmic fairness (individual vs group fairness, protected features, types of metrics, bias mitigation options, safe bands and guidelines). The tutorial will only go deep into metrics and algorithms for classification models. In this section of the tutorial we summarize the prerequisites and provide attendees with the datasets and models to be used throughout the tutorial.

### Fairness Metrics Selection

There are many different definitions of fairness and satisfying two or more definitions at the same time may not always be feasible. In this section we explain the rationale for selecting the most adequate fairness metric for a use-case using examples such as policing and credit risk.

### Bias Propagation and Evaluation Workflow

In this section we focus on a basic classification workflow (data preparation,model build, model evaluation) and we carry out fairness analyses at two different stages: (i) pre- model build and (ii) post-model build through hands-on exercises.

### Challenges from Real-World Implementations

#### Protected features and proxies

Discrimination is prohibited on grounds of gender, race, religion, genetic information etc. This encourage the idea that algorithms should not be allowed to take certain protected categories into account when making predictions. For instance, algorithms which are used to predict loan eligibility or risk of recidivism should not be allowed to base predictions off of gender or race.
However, even if such categories are eliminated from training dataset used by the algorithm, information contained into these protected categories can leak into other available variables. For instance, while race might be excluded from reoffending profiling data, birthplace could still be used as a proxy to diferentiate among racial groups. In this section, we tackle Mutual Information, correlation (for numerical only) and information value, focusing on what they convey about the relationships between the predictors and protected factors.

#### Metrics definition for unbalanced datasets

This section is focused on use cases where the target is a rare event such as fraud prediction. We show how in these cases, the standard definitions of fairness may not be sensitive enough. We propose variations of the existing definitions of fairness metrics and we compare them to the conventional ones. These new variation are also assessed with respect to current guidelines.

#### Data transformation for bias mitigation

The mitigation algorithm creates a modified version of the initial dataset, such that information with respect to the protected feature is removed to different degrees, as selected by the user. The resulting dataset changes only the non-protected attributes while the protected feature and class remain the same as in the original data. In this exercise, using a toy dataset we look at the algorithm in a step-by-step fashion. We focus on understanding when it makes business sense to use this algorithm in a real use-case setting and exactly for what purpose.

#### False Positive Rate

The core of this section is the analysis of False Positive Rate (FPR) as a fairness metric. In this section we evaluate the potential causes of a disparity in FPR. We show solutions to FPR disparity that include bias-mitigation algorithms and other approaches such as segmentation. The advantages and disadvantages of the different solutions are discussed and evaluated.

#### Importance of defined standards and thresholds when implementing

Equal Employment Opportunity Commission’s 80 per cent rule (or 4/5th rule) – US Based – has been formalised by the fair-ML community into a formal measure of bias called Disparate Impact. As no similar guidelines exist for the other metrics, in this exercise, we look at ways of transferring this guideline to other fairness metrics such as FPR. In addition, we will be assessing not only relative thresholds (4/5th rule) but also absolute thresholds (i.e. absolute number of False Positives)

### Prerequisites

To complete the workshop, attendees will need:

- a gmail account
- Google Colaboratory installed on their accounts (user-manual)

As part of the tutorial, attendees will be asked to:

- run jupyter notebooks

### Slides

The slides for the tutorial will be available on this page.

### Tutorial duration

Half-Day Tutorial (3 hours)

### Other Fairness Relevant Resources and suggestions for further reading

* [Certifying and removing disparate impact](https://arxiv.org/abs/1412.3756)
* [A Framework for Understanding Unintended Consequences of Machine Learning](https://arxiv.org/pdf/1901.10002.pdf)
* [Auditing Black-box Models for Indirect Influence](https://arxiv.org/pdf/1602.07043.pdf)
* [A Survey on Bias and Fairness in Machine Learning](https://arxiv.org/pdf/1908.09635.pdf)
* [The Measure and Mismeasure of Fairness: A Critical Review of Fair Machine Learning](https://arxiv.org/pdf/1808.00023.pdf)

### Brief biographies of the presenters

* Medb Corcoran - Managing Director, Lead of Accenture Labs, Dublin
  - Role in tutorial:  Overview, business context for fairness and SME on real world implementation challenges in banking
  - website:

* Steven Tiell - Sr. Principal, Responsible Innovation, Accenture Labs
  - Role in tutorial: Ethical AI Overview, business context for fairness and SME on Ethical AI Governance
  - website: Accenture.com/dataethics
  
* Laura Alvarez Jubete - Analytics Innovation Assoc. Manager at The Dock, Accenture’s Global Innovation Center
  - Role in tutorial: Data Scientist to teach technical aspects of the tutorial
  - linkedin:

* Andreea Roxana Miu - Analytics Innovation Analyst at The Dock, Accenture’s Global Innovation Center
  - Role in Tutorial: Data Scientist to teach technical aspects of the tutorial
  - linkedin:
