---
title       : Printing and Mailing Cost Calculator
subtitle    : Pitch Presentation
author      : Thomas Wire
job         : Developing Data Products Course
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## About the Printing and Mailing Cost Calculator
Th Printing and Mailing Cost Calculator is a Shiny application that can be used to calculate the printing and mailing costs to be charged by the firm XYZ Mailings to mail a set of packages. 

Without having to manually reference the prices associated with printing and mailing, you can quickly and easily determine costs. The calculator is quick and reliable. 

--- .class #id 

## How to Use the Calculator

1. In the side panel to the left, select the envelope type (6x9 envelopes or #10 envelopes)
2. Select the number of packages 
3. Select the number of additional pages. Note that 'additional pages' are any pages in a package beyond the first page. So, the value for 'additional pages' is calculated as the total number of pages minus the number of packages.

---

## Rates Used by the Calculator

The following rates are used to make the calculation:
* For 6x9 envelopes, each package has a cost of $0.279, with $0.029 for each additional page
* For #10 envelopes, each package has a cost of $0.179, with $0.029 for each additional page

---

## A Look Inside the Calculator
Let's look inside how the cost calculation executes by using an example. Suppose that the envelope type is 6x9 and that we need to calculate the cost for 1000 packages with 1000 additional pages. The calculator executes R code as follows:


```r
numPackages <- 1000
numAdditionalPages <- 1000
costForPackages <- numPackages * 0.279
costForAdditionalPages <- (numAdditionalPages) * 0.029
costForPackages + costForAdditionalPages
```

```
## [1] 308
```

