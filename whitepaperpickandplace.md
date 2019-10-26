
# An Intelligent, AI Process Control Solution for Automated Pick and Place Equipment in Electronic Assembly Manufacturing

### Embracing Industry 4.0 Digital Transformation  
### Published January 2019 

## Authors:
Greg Vance (Rockwell Automation)
Mikica Cvijetinovic (Rockwell Automation)
Francisco P Maturana (Rockwell Automation)
Balamurugan Balakreshnan (Microsoft)
Michael Walton (Microsoft)
Stephen Philip (Microsoft)


## An Intelligent, AI Process Control Solution for Automated Pick and Place Equipment in Electronic Assembly

- Introduction Table of Contents
- Pick and Place Nozzle Failure
- Process Overview
- Solution Overview
- Remarks
- References
- Disclaimer:


## Introduction

In our vision of smart manufacturing, we leverage the best technology blends to achieve
Digital Transformation on the plant-floor processes to facilitate operational data
integration with the rest of the enterprise. We envision this transformation as a leap
step into an ecosystem of tools and information that will make data acquisition and
integration more accessible for analysis.

## Pick and Place Nozzle Failure

Smart manufacturing requires quick decision making in which product and process
performance needs to be monitored proactively to prevent excessive downtimes and
failures. To proactively monitor such systems, there is a need to generate contextualized
data out of the physical environment in various volumes and frequencies so enough data
can be collected for trending and root cause analysis. Typically, data resides in disparate
locations ( e.g. databases, machines, gateways, etc.) and behind proprietary interfaces
and firewalls, making data integration a daunting task.

State-of-the-art systems require users to go to individual machines to pull data to
establish a meaningful data integration and actionable information from it. Moreover, if
the intended analysis requires data assimilation with other production data or even
transactional or supply chain data, engineers often must run queries that need to be
associated and merged before it can be analyzed in an offline manner. This is a task that
makes data analysis costly and slow, while making effective real-time data analysis
difficult, too late, and expensive.

In our vision of smart manufacturing, we leverage the best technology blends to achieve
Digital Transformation on the plant-floor processes to facilitate operational data
integration with the rest of the enterprise. We envision this transformation as a leap
step into an ecosystem of tools and information that will make data acquisition and
integration more accessible for analysis.

We observed the component placement operation (aka pick and place operation) of an
electronic assembly manufacturing plant. The pick and place operation is a critical step in
the manufacturing of printed circuit boards (PCBs). It is a data rich operation in the
overall process with multiple vacuum-based nozzles picking and placing the components
onto PCBs. Pick and place data is collected directly from the machine’s database. Our
intention is to leverage this data-rich environment to create knowledge and capture
insights that can be converted into valuable information for the operators and plant
support to help them apply corrective actions for maximizing throughput and
minimizing potential defects in the product. The challenge is the know-how to


implement an information backbone that will permit observing the process in
application real time and to generate insights on-the-fly, so operators can be notified in
a timely manner about potential perturbations in the process. Furthermore, the interest
is in keeping the attention of the operators on the process itself rather than having them
paying attention to monitors waiting for deviations to occur.

The ability to leverage AI based machine learning allows for advanced notification of a
nozzle/spindle/head failure, giving the plant the chance to modify their maintenance
team prior to failure. As all this monitoring, troubleshooting, and restart actions translate
into downtime and therefore affecting the overall process OEE, the objective of this new
way to analyze data is to minimize such a downtime by controlling the variables based
on the new information. Our belief is that data analysis can help to accelerate the time-
to-realization of this endeavor.

In this work, we present initial steps in the direction of automated data acquisition, data
harmonization, storage and processing capacity that will use the best of the cloud
computing environments to achieve the smart manufacturing vision on a legacy
electronic assembly manufacturing system. We propose using this high-performance
computing setting to create actionable analytics and visualization around the electronic
assembly processes by measuring machine performance at scale and in application real
time. This solution will allow the machine operators and production engineers to
identify potential outliers in the production processes as they emerge and to unveil
product quality tendencies that can be resolved faster and with anticipation.

## Process Overview

Pick and place is a machine process within an automated assembly line that produces
circuit boards in an electronic assembly manufacturing plant, as shown in Figure 1.
These are very sophisticated machines that can be programmed to populate various
sizes of circuit boards based on product requirements.

The pick and place operation consist of picking electronic components/parts from a tape
or tray, taking an image of them to identify the placement centroid and then placing
them in the appropriate location on the PCBs as directed by a placement program. The
nozzles mount to various spindles contained within a head that moves at a high speed.
Nozzle vacuum degradation (clogging or mechanical defect) increases the likelihood to
miss-pick/scrap components and increases the potential of a defect in the electronic
assembly. This equipment is robotically controlled and can be programed to optimally
meet the board-layout requirements. The real challenge is to be able to leverage the
knowledge conveyed in the generated information that is extracted during this
operation to learn potential defects and other tendencies of interest, yet to be
discovered.

![alt text](https://github.com/balakreshnan/PickAndPlace/blob/master/images/pic1.png "SMT process")
```
Figure 1 – Electronic assembly line
```
An area where improvements can be made is minimizing the rate of the failure to pick
and place components. If a nozzle starts to fail, it tends to miss-pick components. As this
error rate increases it can cause downtime and reduces the operation efficiencies as well.
By detecting and/or predicting the failure/degradation of the nozzles, it will facilitate
alerting support personal to proactively troubleshoot the nozzle(s) before they become a
significant problem. Early detection also minimizes the opportunity to introduce defects
into the product.

This pick and place equipment handles about 1 - 30 nozzles per head and there are one
to four heads with nozzle changers with some number of nozzles. When a nozzle fails, it
can take a significant amount of time in troubleshooting to determine the specific
nozzles that need replacement. One goal is to be able to control downtime by
anticipating the nozzle failure. Knowing when it can fail will transform the maintenance
process into a proactive activity based on factual calculations and higher certainty.

One of the main concerns here is also to avoid false positives or false alarming to avoid
overwhelming the operators with false alerts.

If we can avoid any defect here it will save the manufacturer on rework. Also, there are
components like Integrated Circuit (IC) chips where only one side can be soldered. So,
the component placement is very critical. The Pick and Place is a critical machine in the
line where there may be 1 or more machines in the line based on the product physical
requirements.

Sometimes the components are placed shifted or skewed on the board which will cause
defective boards after permanent assembly (soldering). A whole panel holding multiple
electronic assembly modules might need rework which can take 1 to 48 hours,
depending on what the defects is. Position issues can be detected in downstream
inspection stations such as the Automated Optical Inspection (AOI) machine while
electrical issues are only detected at the final stage at functional integrated circuit
testing, where the boards are already assembled. All these defects affect the OEE of the
plant.


## Solution Overview

The Plan to tighten Nozzle Performance

We assembled a team of AI enthusiasts to create a way of solving the machine-
performance prediction challenge. The team consisted of business personnel and
architects working together to analyze and design a solution. The team decided to solve
the solution by incrementally building up analytics with AI and Machine Learning
approaches.

A descriptive-analytic based solution was initially built to establish a data governance
and analytic platform for visualizing the natural behavior of the machine, nozzle, and
process per build order, as show in Figure 2. The team learned the nozzles’ behavior and
accumulation of defects by observing nozzle-cumulative patterns and performance
metrics indicators, directly from the data. Based on this primary knowledge of the nozzle
behavior, the team was able to define a predictive monitoring algorithm which required
leveraging a modern high-performance computing workbench with AI helpers and
parallel data processing engines.

![alt text](https://github.com/balakreshnan/PickAndPlace/blob/master/images/pic2.png "Nozzle Report")
```
Figure 2 - Descriptive-analytic machine performance
```
Governance from the point of view of data flow, security, usability and data preparation
were fundamental steps for achieving a clear view of the performance. For example, a
significant amount of time was required to establish an understanding of the data and a
methodology to suppress the noise.


The Pick and Place data is configured to refresh every 15 minutes. Each chunk of data
per machine is automatically moved to a data lake repository in the Cloud via a plant-
floor level gateway. The data lake was built using big data components such as Hadoop,
Spark, and Kafka. In the data lake environment, several micro services were created to
handle data governance, ETL, and analytics. Classical data wrangling and data
transformation (supported by spark-based services) were accomplished in the data lake
level. A separate folder contains the curated data for further model development. Power
BI was used to visualize the data from different perspectives and analysis, constituting
the analytic and reporting dashboards.

To facilitate the data organization and selection of significant parameters, the team
collected human operator experience to incorporate additional heuristics into the design
of the predictive solution. Several interviews with the operators took place to gain
insights about other aspects that could also be affecting the pick and place performance.
After the interviewing process, the team collected the data and was able to chart the
performance and envision important data correlations.

It was discovered that a higher accumulation of miss-picks and misplacements always
correlated to a configuration of the nozzles that could be analyzed from a cumulative-
tendency perspective, and where instantaneous measurements were not enough to
unveil the anomalies causing the defects. We learned that the nozzle position relative to
its cumulative rejects is an important indicator. This insight led the team to think in the
direction of an AI-based algorithm that could learn and trace the behavior of individual
nozzles, as shown in Figure 3.


![alt text](https://github.com/balakreshnan/PickAndPlace/blob/master/images/pic3.png "Nozzle Behaviour")
```
Figure 3 – Forecast nozzle tendency
```
We first established a slope-based identification algorithm to detect the outliers. We
then began operationalization of an AI/Machine Learning algorithm to forecast the
future state of the nozzles in this subset of outliers for which case we looked at AI
techniques to automate the discovery process.

After collaborating with expert data scientists, we tested a set of algorithms such as,
ARIMA and Temporal Difference Methods (TD) for Reinforcement Learning as the
primary Machine Learning techniques to predict the nozzle behavior. Since this type of
failure is based on time, we needed a time series-based Machine Learning algorithm.

ARIMA: This is a time series analysis. It stands for Auto Regressive, Integrated, Moving
Average. The intuitive premise of this model is that the prediction in the next time step
is informed by a variable, n past time steps in the past. Auto Regressive refers to the fact
that a shock to the system could be more slowly absorbed, and Moving Average follows
a behavior where shocks to the system (e.g., excess demand) is rapidly absorbed. These
two behaviors tend to interact in a juxtaposed fashion. To understand which is which, we
analyzed charts of Partial Auto Correlation Functions (PACF) for auto regressive behavior
and Auto Correlation Functions (ACF) for moving average behavior. The “I”, in ARIMA
stands for a differencing function, where we can sometimes use this to stationarize a
series. The intuition behind stationarity is that the future behavior will be like the past,
so the data cannot vary over time, and if it does, we must stabilize (stationarize) the
series during training, and then add back any stationarizing modifications we made



when we predict. The next step is to try a multivariate ARIMA as we used a univariate
method for the nozzle positioning.

Reinforcement Learning-Temporal Difference (TD) methods: After the business
described the behavior of the nozzle, we concluded this fits the behavior associated with
temporal difference models and Markov Chains. We chose an algorithm called TD
Lambda, which suits paradigms where each successive time step reveals more about the
time step in the future we are trying to predict. A good example is weather, where on
Monday trying to predict Saturday’s weather is less accurate than predicting Saturday’s
weather on Wednesday. In between Monday and Wednesday, you have more
information revealed by the system to factor in, so we can update our predictions. TD
Lambda uses Markov chains, which are a series of states (positions) that have a transition
probability to the next state. We obtain a Maximum Likelihood Estimate (MLE), that tells
us where the nozzle is likely to be in the future, based on its current position. The
likelihood of the nozzle being at this state is the MLE, which is based on Bellman’s
Equation of Optimality, affectionately referred to as the Bellman Equation. Lambda is a
hyperparameter that can be tuned to manage decay of eligibility traces. This simply
means that we can adjust how important past timesteps are to find the true behavior of
our system.

Prior to AI/ML implementation, we carried out a validation of the slope-based prediction
algorithm. An initial prototype was designed and validated in Azure Databricks notebook
using Spark Scala programing languages. Production data was collected from data lake
repository in a raw format. The Databricks notebook was used to figure out all the steps
to convert the raw data into a usable data set that could be injected into the AI/ML
model. The nozzle outlier detection algorithm triggered alarm notifications into an Azure
notification hub, where the messages were directed to the maintenance team at the
Rockwell Automation production plant, as shown in Figure 4.

Next step is to build the AI/ML model, a deployment plan has been designed to bundle
the Spark-Scala model into a deployable solution that can be executed in the data lake
environment in production. This bundle will connect to the pick and place data streams
to execute the analysis and notification in real time.

As the solution matures, production implementation will continue to grow. Since this is
an AI process, a continuous learning cycle will be introduced to batch train the model
monthly with the new data points and make the model more robust and accurate. As the
model gets more robust, the new model will be deployed to the plant. The score results
for various models will be stored in a central location to other validation purpose.


![alt text](https://github.com/balakreshnan/PickAndPlace/blob/master/images/pic4.png "Architecture")
```
Figure 4 – Azure Databricks-based development
```
A proper development lifecycle will be applied to the process. Moreover, a development
pattern will be established from this effort that can be applied to other machine learning
use cases.




## Remarks

During Pilot runs of the Nozzle Monitoring solution (pre AI/ML), we saw several
improvements related to Productivity and Cost Savings due to earlier detection of nozzle
related issues:

```
 Significantly more detection of a bad nozzle. For example, after
analyzing historical data, it was not uncommon to run on a degraded
nozzle for up to 2 weeks, accumulating 6,000 or more miss-picks before
a successful diagnosis by a technician. Along the way, there would be
several log-downs accruing hours of downtime, and it was found to be
common that a bad nozzle would be re-installed after inspection if clear
damage was not observed.
```
```
 Early identification of a nozzle concern is descriptive, as it points the
technician directly to which nozzle on the machine that is performing
poorly, saving on average 30 minutes of troubleshooting time which
translates directly to downtime.
```
```
 Productivity, each miss-pick average ~1.5 seconds of lost productivity.
Severe cases cause constant machine stoppage as the machine detects
it has run out of parts, when in fact, it cannot pick parts successfully.
These interruptions impact line efficiency up to 15%.
```
```
 Reduction of scrapped components. Each miss-pick is essentially a
scrapped component that accumulates the cost of operation.
```
```
 Reduction of expensed items by letting the performance of the nozzle
dictate when it needs to be inspected and replaced. Nozzles are
wearable items that are often replaced. It was found to be common for
a good nozzle to be replaced because it was believed to be bad after
visual inspection, or the process of elimination has replaced a good
nozzle.
```
```
 Reduction of defects by removing the threat of a degrading nozzle.
Further, defects and performance issues are caught near the process
origin as they occur, which gives insight to correct issues before a
backlog is found at a later operation.
```
As we move into AI/ML development, we expect to be able to detect the failure of a
nozzle before it occurs. If proven successful, we expect the above points to provide even
more value to production.

Additionally, storing historical data, along with the other data that has been collecting in
the data lake has provided other benefits in the analytical space. We have established
other historical and near real time dashboards to track and analyze historical trends


without the need for an engineer to spend hours data mining in Excel, but rather
exploring a comprehensive data model in a dashboard. This minimizes the non-value-
add time an engineer spends and provides insight to opportunities in minutes.


11 An Intelligent, AI Process Control Solution for Automated Pick and Place Equipment in Electronic Assembly

## References

[1] Learning to Predict by the Methods of Temporal Differences Richard, Sutton 1988,
https://pdfs.semanticscholar.org/9c06/865e912788a6a51470724e087853d7269195.pdf

[2] Deep learning - https://en.wikipedia.org/wiki/Deep_learning

[3] LSTM - https://en.wikipedia.org/wiki/Long_short-term_memory

[4] Reinforcement learning – Markov Chain -
https://en.wikipedia.org/wiki/Markov_chain

[5] Hdinsight - https://docs.microsoft.com/en-
us/azure/hdinsight/hadoop/apache-hadoop-introduction

[6] Azure Databricks - https://docs.microsoft.com/en-us/azure/azure-databricks/

[7] Azure SQL - https://docs.microsoft.com/en-us/azure/sql-database/

[8] Azure functions - https://docs.microsoft.com/en-us/azure/azure-
functions/functions-overview

[9] Notification hub - https://docs.microsoft.com/en-us/azure/notification-

hubs/notification-hubs-push-notification-overview

[10] Power BI - https://docs.microsoft.com/en-us/power-bi/service-azure-and-
power-bi

[11] Artificial Intelligence. - https://www.microsoft.com/en-us/ai/default.aspx

[12] ARIMA https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average

## Disclaimer:

(c) 2018 Rockwell Automation/Microsoft Corporation. All rights reserved. This
document is provided "as-is." Information and views expressed in this document,
including URL and other Internet Web site references, may change without notice. You
bear the risk of using it.

This document does not provide you with any legal rights to any intellectual property in
any Microsoft product. You may copy and use this document for your internal, reference

purposes. You may modify this document for your internal, reference purposes.
