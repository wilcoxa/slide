---
title       : Developing Data Products Presentation
subtitle    : Population Statistics!
author      : wilcoxa
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap, shiny, interactive}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Australian population statistics

What does the app do?


This shiny app reads Australian Bureau of Statistics population data and produces a customisable data table that can also export the data into a csv file.

The population figures can be classified by:

  * Gender
  * State
  * Age

---


## 3101.0 - Australian Demographic Statistics

Where does the data come from?

About this release

"Quarterly estimates of total population for states, territories and Australia. Includes the most recent estimates of the population in five-year age groups; numbers (and some rates) of births, deaths, infant deaths, interstate and overseas movements. Quarterly and/or annual time series tables throughout. Also includes projected resident populations, projected population in households, projected number of households and projected average household size for states, territories and Australia. Periodically, articles on specific demographic topics will be released on the ABS web site in conjunction with this publication."

---



## An easier way to extract the data you need

Turn raw data


```r
print(head(RAWERP))
```

  V1           State  Sex Age Population
1  1 New South Wales Male   0      51651
2  2 New South Wales Male   1      50831
3  3 New South Wales Male   2      49094
4  4 New South Wales Male   3      49785
5  5 New South Wales Male   4      49167
6  6 New South Wales Male   5      48973

into aggregated form without typing any code!


```r
aggregate(Population ~ State, data= RAWERP, FUN = sum)
```

                         State Population
1                    Australia   23133712
2 Australian Capital Territory     381469
3              New South Wales    7409592
4           Northern Territory     241196
5                   Queensland    4655011
6              South Australia    1670689
7                     Tasmania     513124
8                     Victoria    5738876
9            Western Australia    2520573


---

## Where to find it

Check out the app here:
[https://wilcoxa.shinyapps.io/APP1/](https://wilcoxa.shinyapps.io/APP1/)

And code available here:
[https://github.com/wilcoxa/Developingdataproducts](https://github.com/wilcoxa/Developingdataproducts)


