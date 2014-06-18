---
title       : Shiny Calculator for BMI
subtitle    : Check your Weight and Healt Risk
author      : Predrag Jovanovic
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## Body Mass Index (BMI)

- Measure of relative weight based on an individual's mass and height
- Simple method to assess how much an individual's body weight departs from what is normal or desirable 
- Overweight and obese individuals are at increased risk : Hypertension,  Dyslipidemia, Type 2 diabetes, Coronary heart disease, Stroke


## Formula

$$BMI = \frac {mass(kg)}{height(m)^2}$$

for US customary unit factor 703.07 should be used

$$BMI = \frac {mass(lb)}{height(in)^2} \cdot 703.07 $$

---

## Categories
Variations how categories are set 

Shiny calculator uses following categories:

BMI | Category
-----------|--------------------------
 < 18.5  | Underweight
18.5-22.9| Normal Range
18.5-22.9| Normal Range
23.0-24.9| Overweight - At Risk
  >=25| Overweight - Obese
  
- Calculator works only for adults.

- BMI is used differently for children.

---

## R code

Here is implementation of BMI calculation and category



```r
m <- 82; h <- 184
bmi <- BMI(m,h)
bmi
```

```
## [1] 24
```

```r
catBMI(bmi)
```

```
## [1] "Normal"
```

Apart from BMI calculation shiny project contains **dynamic plot** with given detail (mass, high) as point on chart

--- 

## Conclusion

> - Pros:
    -  Simple and quick way to check healty weight
    -  More accurate at approximating degree of body fatness than weight alone
    -  There is a range within each classification to allow for different body types and shapes

> - Cons:
    -  Debate regarding  which value of the BMI scale the threshold for overweight and obese should be set  
    -  Muscular individuals often fall into the overweight category
    -  Measuring BMI for very short people or pregnant women is not appropriate.
