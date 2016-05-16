---
title       : Project in Data Products class as part of the DataScience specialization at coursera.org
subtitle    : MPG estimation Shiny app
author      : Andrei Kuebar
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Shiny app created for this project 
URL:https://ierdna.shinyapps.io/project/

This app allowes the user to estimate the Mileage per Gallon of gas of a car based on three parametes:
 - horse power
 - 1/4 mile time
 - transmission type

--- .class #id 
## Model
To estimate the MPG value a multivariable linear regression model was created

R dataset 'mtcars' was used as the data source

```r
data(mtcars)
dim(mtcars)
```

```
## [1] 32 11
```

--- .class #id
## Model fit

Linear model was fitted as follows:

```r
fit <- lm( mpg ~ hp + qsec + am , mtcars)
summary(fit)$coefficient
```

```
##                Estimate  Std. Error    t value     Pr(>|t|)
## (Intercept) 16.63206916 11.16841513  1.4892059 0.1476115618
## hp          -0.04912325  0.01342505 -3.6590752 0.0010398097
## qsec         0.46130309  0.51338361  0.8985544 0.3765524637
## am           5.98311261  1.33812628  4.4712616 0.0001174983
```

--- .class #id
## Shiny app and source
 - MPG Shiny app is found here: https://ierdna.shinyapps.io/project/
 - GitHub source for the app: https://github.com/andreikubar/dataproducts/tree/master/project




