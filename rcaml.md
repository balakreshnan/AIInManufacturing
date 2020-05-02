# Root cause analysis for manufacturing engineering and operations

### Embracing Industry 4.0 Digital Transformation  
### Published Febraury 2020 

## Authors:
- Athinarayanan, Ragu (Purdue University)
- Richards, Grant P (Purdue University,)
- Joseph M. Zaccaria (Rockwell Automation)
- Michael Cook (Rockwell Automation)
- Francisco P Maturana (Rockwell Automation)
- Balamurugan Balakreshnan (Microsoft)
- Michael Walton (Microsoft)
- Priya Aswani (Microsoft)
- Sundar Ramakrishnan (Microsoft)
- Gaurav Nanda (Purdue University)
- Hauchao Mao (Purdue University)
- Jhareswar Maiti (IIT Kharagpur)

## An Intelligent system to detect root cause of a failure in manufacturing engineering and operations

- Introduction Table of Contents
- Root Cause Analysis
- Process Overview
- Solution Overview
- Remarks
- References
- Disclaimer:

## Introduction

Root cause ananlysis - which is an area where all manufacturing customers are always interested in. How can we apply new aritifical intelligence or machine/deep/reinforcement learning to find root cause on failures that cause downtime. 

For Example: OOE - operation equipment efficiency Uptime, Yield, Availbility, Downtime are some of the KPI that is monitored for any assembly line or automated process. Larger the uptime more the production so it directly corelates to increase in production which in tern increases revenue.

The way to reduce downtime and increase uptime is where most of the manufacturing operations are looking for. One way to avoid downtime is to find the most downtime failure which causes the largest the down time and ability to find their root cause and abilityt to predict the failure before on hand so that manufacturer can be prepared by finding the technician, order the parts needed and find the more less used time to schedule the repair work and avoid down time.

Different manufacturing operations might have different downtime based on how complex the down time can cost them. For example in mining knowing what is going to fail is important since parts are not available in shelf had to be made to order when needed. 

So does the parts in Assembly line machine which could be a simgle vendor or multiple vendor integrated machines in the line. 

## Root Cause Analysis

So finding the root cause when failure happens and finding the right root cause is necessary. It becomes so challenging since every SI vendor or manufacturers of line machine have their own way to finding failures and report in a user friendly way which means only they can understand where the failure is. But what would be the process and solution to tackle the root cause failure detection based on available data.

The other challenge is do we have all the data for root cause analysis. Most line manufacturer design their state machine and the control system logic defines the faults. Every vendor does their own way. But when we create a assembly lines with multiple vendor and ability to find the root cause and able fix is a huge advantage for every manufacturing company.

The other challenge is can machine or deep learning help in terms of find the root cause and apply reinforcement learning to take actions. Once we find the root cause ability to create a repair order and send it to management for scheduleing the repair would be great. Of course for this all equipments have to be connected and there should be a seamless data available from all machines in lines in a central data repository.

For Example:
Say for example if there is a Assembly line which has like 5 different machine to do the manufacturing process. Each machine has lots of components like motor, belt, sensors, PLC etc. It also has workflow that makes the machine running as per defined programming. Take 1 machine as example say there is robot that takes the part and attaches to a frame. Say the frame didn't make it time but the robot takes the part and then it stops saying coudn't find frame (which means it could be anything). But the actual root cause here was because the frame didn't make it time in the converyor belt. Ability to find that we couldn't process because frame didn't make it time and report that might be very useful since the techinician doesn't have to go and check the line since we the operator know it stopped because the frame was not available. This also is true when there are multiple components and lots of sensors in a machine and as control logic check every component it can be follows a logic and that can change the actual root cause.

## Process Overview

Root cause analysis is a systematic process to elimanate every processing unit and finding the right cause. 
There is also 5 why's technique which is widely used

https://en.wikipedia.org/wiki/Five_whys

https://en.wikipedia.org/wiki/Ishikawa_diagram

From the above our approach is to look and see if we can apply machine learning technique like decision trees or other means to find the root cause.

The research would be also to see if deep learning can also be applied.

![alt text](https://github.com/balakreshnan/AIInManufacturing/blob/master/images/rcadiag.jpg "Architecture")

## Architecture

![alt text](https://github.com/balakreshnan/AIInManufacturing/blob/master/images/IndustrialIoT-Kepware1.jpg "Architecture")
```
Note: please note this is still under development.
```
