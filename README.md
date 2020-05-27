## Measuring Algorithmic Fairness: challenges and solutions for the industry

How can we quantitatively measure and mitigate algorithmic bias? 

The tutorial will focus on communicating real-world experience on assessing fairness throughout the machine learning model development life-cycle (all elements also relevant to non-machine learning analytical models). It will cover innovative solutions for measuring and correcting algorithmic bias through hands-on exercises in a range of use-case scenarios from banking to policing.

### Tutorial Description

As machine learning models are employed to inform decisions in an increasingly wide range of human scenarios (e.g. banking, criminal justice, medicine and employment), it is very important to ensure that these decisions are equitable. This tutorial aims at providing the audience with an understanding of the nascent field of algorithmic fairness, by analysing the existing approaches in the literature, and complementing and critiquing them with lessons learned from our experience applying them in real-life situations, both in financial services and government agencies.

Exercises will focus on key lessons learned and will cover how to deal with scenarios such as where highly unbalanced datasets mean the state-of-the-art metrics are not sensitive enough and where the defined state of the art metrics fall short in specific modelling contexts, as well as essentials such as how to choose the best fairness metric to use for a given scenario,  how to understand the effect of the repair algorithms and when it makes business sense to use them and the need to understand the source of bias prior any other steps and focus on alternative solutions to the repair algorithms.

### What makes algorithmic fairness worth the attention?

Algorithmic Fairness is an emerging area that is attracting a lot of attention, with academic publications in the topic increasing exponentially in the last 5 years, but we have very few examples of actually applying these approaches to industry, which is where the real value lies. Bias has become one of technology industries most notorious ethical issue and is receiving substantial coverage in the media, with some famous cases concerning some of the technology giants.

Even though unintended, algorithmic bias is most dangerous when it rules over critical systems such as predictive policing, hiring processes or medical applications. Extensive efforts are being directed towards understanding its sources and impact across these applications.

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

The community of fairness-aware machine learning professionals aim to develop automated-decision based systems that, once introduced into a social context, lead to fair and just outcomes. We outline the importance of a joint effort of multidisciplinary communities that will bring together ideas and insights from law, social and behavioural sciences combined with methodologies from the computer science field.

With this in mind, we kick off the session with a general overview of algorithmic fairness (individual vs group fairness, protected features, types of metrics, bias mitigation options, safe bands and guidelines). The tutorial will only go deep into metrics and algorithms for classification models. In this section of the tutorial we summarize the prerequisites and provide attendees with the datasets and models to be used throughout the tutorial.

### Fairness Metrics Selection

There are many different definitions of fairness and satisfying two or more definitions at the same time may not always be feasible. In this section we explain the rationale for selecting the most adequate fairness metric for a use-case using examples such as policing and credit risk.

### Bias Propagation and Evaluation Workflow

In this section we focus on a basic classification workflow (data preparation,model build, model evaluation) and we carry out fairness analyses at two different stages: (i) pre- model build and (ii) post-model build through hands-on exercises.

### Challenges from Real-World Implementations

#### Protected features and proxies

Discrimination is often prohibited by law on grounds of gender, race, religion, genetic information etc. and this means that algorithms are allowed to take certain protected categories into account when making predictions. For instance, algorithms which are used to predict loan eligibility or risk of recidivism should not be allowed to base predictions off of gender or race. However, even if such categories are eliminated from training dataset used by the algorithm, information contained into these protected categories can leak into other available variables. For instance, while race might be excluded from reoffending profiling data, birthplace could still be used as a proxy to diferentiate among racial group.  Often, even when it isn’t a legal requirement, it is still the case that we do not want protected categories to impact predictions.

#### Metrics definition for unbalanced datasets

This section is focused on use cases where the target is a rare event such as fraud prediction. We show how in these cases, the standard definitions of fairness may not be sensitive enough. We propose variations of the existing definitions of fairness metrics and we compare them to the conventional ones. These new variation are also assessed with respect to current guidelines.

#### Data transformation for bias mitigation

The mitigation algorithm creates a modified version of the initial dataset, such that information with respect to the protected feature is removed to different degrees, as selected by the user. The resulting dataset changes only the non-protected attributes while the protected feature and class remain the same as in the original data. In this exercise, using a toy dataset we look at the algorithm in a step-by-step fashion. We focus on understanding when it makes business sense to use this algorithm in a real use-case setting and exactly for what purpose.

#### False Positive Rate

The core of this section is the analysis of False Positive Rate (FPR) as a fairness metric. In this section we evaluate the potential causes of a disparity in FPR. We show solutions to FPR disparity that include bias-mitigation algorithms and other approaches such as segmentation. The advantages and disadvantages of the different solutions are discussed and evaluated.

#### Importance of defined standards and thresholds when implementing

Equal Employment Opportunity Commission’s 80 per cent rule (or 4/5th rule) – US Based – has been formalised by the fair-ML community into a formal measure of bias called Disparate Impact. As no similar guidelines exist for the other metrics, in this exercise, we look at potential ways that might be used to apply the  guideline to other fairness metrics such as FPR. In addition, we will be assessing not only relative thresholds (4/5th rule) but also absolute thresholds (i.e. absolute number of False Positives)

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
   
   **Role in tutorial:**  Overview, business context for fairness and SME on real world implementation challenges in banking
   <details><summary>Bio Details</summary>
   <p>
   Medb is Managing Director of Accenture Labs in Dublin, one of Accenture’s seven key research hubs around the world –            where she leads a team of research scientists that apply emerging technology in the area of AI to help solve problems and create value for clients and society. One of the main focus areas of her team is Explainable AI – which is a key element of being able to ascertain if an AI system is fair.
   
   Medb is Accenture-Turing Research Director with The Alan Turing Institute in the UK – where she sets agenda and oversees the Accenture portfolio of joint research focusing on ‘Innovating for the Responsible use of AI’. As part of this role, she participated in an Accenture Turing Hackathon in 2018 and brought one of the outcomes, a POC on quantifying Algorithmic Fairness, to Accenture the Dock and sponsored a project to develop this into an Algorithmic Fairness Tool that year. She then oversaw the application of the tool with a European Financial Services Client. She oversees the annual joint innovation symposium – a video of the 2019 symposium, which featured the Algorithmic fairness tool can be found here: https://www.turing.ac.uk/collaborateturing/current-partnerships-and-collaborations/accenture
   
   She presents regularly both internally and externally on Responsible AI, including algorithmic fairness. 
   
   </p>
   </details>

* Steven Tiell - Sr. Principal, Responsible Innovation, Accenture Labs

  **Role in tutorial:** Ethical AI Overview, business context for fairness and SME on Ethical AI Governance
   <details><summary>Bio Details</summary>
   <p>
   Steven started Accenture’s journey in data ethics in 2013 while leading foresight research for the firm’s annual
   Technology Vision. Since that time, his pace of discovery in the field has only accelerated. You can read the first set    of papers he published in collaboration with over a dozen others in 2016 at Accenture.com/dataethics. In 2018, he started the Data Ethics Salon Series for practitioners to convene and help each other establish best practices – he has spun the Salon Series out to the Atlantic Council’s GeoTech Center to accelerate the global discovery and publication of best practices. He speaks frequently on topics of data ethics, governance, and related issues, often to large, global audiences and he has published extensively in this field.
    Steven is the author of many publications including: <em>Universal Principles of Data Ethics: 12 Guidelines for Developing Ethics Codes</em>, <em>Facilitating ethical decisions throughout the data supply chain</em>, <em>Ethical algorithms for “sense and respond” systems</em>, <em>Building Data and AI Ethics Committees</em>.
      </p>
   </details>
  
* Laura Alvarez Jubete - Analytics Innovation Assoc. Manager at The Dock, Accenture’s Global Innovation Center
  
  **Role in tutorial:** Data Scientist to teach technical aspects of the tutorial
   <details><summary>Bio Details</summary>
   <p>
   Laura is an Analytics Lead at The Dock, Accenture’s Global Innovation Center in Dublin, Ireland. Her main research   interest is in the area of ethical AI and algorithmic fairness. Laura has led for the last 1.5 years the design and build of Accenture’s Algorithmic Fairness Tool. She has recently completed a 5-month project with a European Financial Services Client where herself and her team conducted the fairness assessment and bias mitigation of two of their classification models, gaining valuable insights as to the challenges and solutions related to the application of state-of-the-art methods coming from academia in a real-life setting.
      
    [linkedin](linkedin.com/in/laura-alvarez-jubete-b7501257)
   </p>
   </details>

* Andreea Roxana Miu - Analytics Innovation Analyst at The Dock, Accenture’s Global Innovation Center

  **Role in Tutorial:** Data Scientist to teach technical aspects of the tutorial
   <details><summary>Bio Details</summary>
   <p>
   Andreea has been working closely with a European Financial Institution in the area of Algorithmic Fairness for the last 5 months. The collaboration consisted in implementing algorithmic fairness approaches researched in academia and testing their suitability and applicability in industry settings.
   
   Andreea recently graduated a MSc in Data and Computational Science from University College Dublin, where she focused her research thesis on explainability in machine learning. In 2017 she received a BSc in statistics and economics from the Faculty of Cybernetics, Statistics and Economic Informatics in Bucharest, Romania.
   
   <a href="www.linkedin.com/in/andreeamiu">linkedin</a>
   </p>
   </details>  
