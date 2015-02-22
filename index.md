---
title       : Assisted Reproductive Technologies Data Analysis Tool
subtitle    : A Shiny App for visualising ART data
author      : dcfenning
logo        : ART_logo.jpg
framework   : revealjs        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : default      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## 1. Introducing
## ART App
![](ART_logo.jpg)

* ARTApp is a Shiny App that allows users to interact and visualise annual data on Assisted Reproductive Technologies across the US.
* ARTApp enables easy access to the most recent data to support decision making in selecting a Fertility clinic for Assisted Reproductive Technologies. 

--- .class #id 

## 2. What are the key features?
* User can select a key ART statistic to compare their chosen clinic against a state wide average, and all states.
* A user interactive map quickly shows where the averages for a selected statistic are high or low using a fading colour chart.

![](us_map.png)

--- .class #id 

## 3. Why use Shiny Apps?

* User Interactive analysis of ART data provided by the Centres for Disease Prevention and Control
The data provided by the CDC is in an .xls format which requires manipulation before it can be analysed and used for comparisons.
* The majority of users of this data would not be able to manipulate this data in Excel without extensive use of formulas or coding of VBA.
* Shiny Apps is easy to deploy and allows quick interaction for users to compare statistics.

--- .class #id 

## 4. Example of data manipultation
Extract from the raw data provided by CDC:

```
##      state_list FshNDCansRate2
## [1,] "ALABAMA"  "2 / 12"      
## [2,] "ALABAMA"  "18.2"        
## [3,] "ALABAMA"  "2 / 14"      
## [4,] "ALASKA"   "1/15"        
## [5,] "ALASKA"   "16.1"        
## [6,] "ALASKA"   "0 /3"
```
Data after manipulation in R, shows new column with calculations made to it:

```
##      state_list FshNDCansRate2 calc  
## [1,] "ALABAMA"  "2/12"         "0.17"
## [2,] "ALABAMA"  "18.2"         "18.2"
## [3,] "ALABAMA"  "2/14"         "0.14"
## [4,] "ALASKA"   "1/15"         "0.07"
## [5,] "ALASKA"   "16.1"         "16.1"
## [6,] "ALASKA"   "0/3"          "0"
```

--- .class #id 

## 5. ARTApp future developments
* Allow users to select multiple statistics for comparison in the tables
* Collect and merge past CDC data reports to show statistics over time and allow user to interact
<center> 
![](ART_logo.jpg)

ARTApp - Supporting infertility patient's choice </center>
