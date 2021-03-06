---
title       : A Body Mass Index calculator
subtitle    : data products project summer 2014
author      : Martin Heath
job         : Student of Computer science in Tampere university
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Table of Content

1. Basic idea of application
2. How to use it
3. How it was made
4. The classification of BMI
5. Why it is good

--- .class #id 

## Basic Idea of Application

The shiny app I decided to make was a very simple BMI(Body Mass Index) calculator.
The user would input their age, weight, height and sex and the app would calculate the BMI and show the results.

The program would react to certain elements, like age and sex. The application would also give the user a classification of their BMI, ranging from underweight to overweight, according to the general limits.

---

## How to use it

The program is quite simple. On the sidebar of the page, there are three numeric input boxes and a pair or radio buttons. The numeric boxes represent age, height and weight respectively. The radio buttons represent sex.

This data is filled and then submitted via a Submit - button.

The data is calculated and the user is given his/her BMI, a notification if needed and a classification of her/his BMI.

Very easy, very simple.

---

## How it was made

The application was very simple, befitting a first-time shiny application. The data is collected from the user input and calculated using the basic BMI formula, which is

Height * (weight squared)

So, let's say I weigh 59kg and my height is 165cm. That would mean

```r
59/(165^2)
```

```
## [1] 0.002167
```
Which, when multiplied appropriately, comes to a BMI of about 21.7, which is healthy.

After this, the application checks if the user is 18 or younger and notifies, that the BMI is not accurate at this age.

Finally, using a simple set of if - else statements, the BMI is classified and the user is given simple feedback.

---

## BMI Classification

The body mass index, or BMI, is a widely used method of measuring weight. Though it cannot be seen as hard science. It is slightly inaccurate and can only provide loose concepts of weight limits. However, this simplicity is what makes it great. Anyone can easily and quicly calculate their BMI and act accordingly.

In this application, the limits are as follows:

under 18 = Clinical underweight
18 - 18.5 = slightly underweight
18 - 25 = Normal BMI, healthy
25 - 30 = slightly overweight
over 30 clinical obesity

so, as our earlier example shows:

```r
BMI = 21.7

if(BMI > 18 & BMI < 25) 
  "Your body is healthy, at least weightwise. Congratulations!"
```

```
## [1] "Your body is healthy, at least weightwise. Congratulations!"
```

---

## Why it is good

A lot of health magazines and websites mention BMI and a few professional medical sites use it as well. 

An easy and simple app can add alot to these sites, letting users try it out and maybe learn something about their health.

The app is very universal and can be easily assimilated into any site or program. The program can also utilise plots or perhaps a link to a help service, if your BMI is looking worrisom.
