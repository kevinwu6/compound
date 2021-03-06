---
title       : Compound Interest Calculator
subtitle    : 
author      : Kevin Wu
job         : 
framework   : html5slides   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]     # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
github      :
    user    : kevinwu6
    repo    : compound
---

## Compound Interest

**Compound interest** is the interest calculated on *both* an initial principal deposit or loan *and* any accumulated interest.

Some features of compound interest:

1. The amount or value grows faster than with simple interest.
2. The effective interest rate depends on compounding frequency, i.e. number of periods.
3. The higher the frequency, the greater the compound interest.

---

## Compound Interest Calculator

The **Compound Interest Calculator** app allows you to calculate the total future value of a deposit or loan after compounding. Simply enter the following inputs:

* Principal Amount (dollars)
* Annual Interest Rate (annual %)
* Time Period (years)

The Calculator assumes annual compounding.

---

## Calculator Benefits

The **Compound Interest Calculator** makes calculating compound interest easy. You can use it to determine the value of an investment.

Benefits of using an app:

1. No manual calculations
2. No need to memorize formulas
3. Easy to use as a savings tool

---

## Calculator Function

The Calculator uses the following compound interest formula:

$$Future\ Value = Principal \times (1 + Rate)^{Time}$$

Here is the function in R. When you hit the “submit” button, the app runs this function based on the parameters you enter.


```r
future_value <- function(principal, rate, time) {
    principal * (1 + rate / 100)^(time)
}
```

---

## Compound Interest Example

Now we can test out the function using example values. Below, we calculate the future value of an initial investment of $10,000 for 5 years at 3.875%.


```r
## Initialize variables
principal <- 10000
rate <- 3.875
time <- 5

## Run function
future_value(principal, rate, time)
```

```
## [1] 12093.59
```

The future value is $12093.59.

<sub><sup>For .Rmd file, see: https://github.com/kevinwu6/compound/blob/gh-pages/index.Rmd</sup></sub>
