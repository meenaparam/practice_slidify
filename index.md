---
title       : Practising slidify    
subtitle    : 
author      : Meenakshi Parameshwaran
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
ext_widgets:: {rCharts: [libraries/nvd3]}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Read-And-Delete

1. Edit YAML front matter
2. Write using R Markdown
3. Use an empty line followed by three dashes to separate slides!

--- .class #id 

## Slide 2

Some practice stuff

--- &radio

## Question 1

What is $x^2$ when $x$ is 9?

1. 89
2. 90
3. 99
4. _81_

*** .hint What is $9 times 9$?

*** .explanation When $x$ is 9, $x^2$ is $9^2$, which is $9 times 9$.

---
## Interactive Chart

``{r echo = F, results = 'asis'}
require(rCharts)
haireye = as.data.frame(HairEyeColor)
n1 <- nPlot(Freq ~ Hair, group = 'Eye', type = 'multiBarChart',
  data = subset(haireye, Sex == 'Male')
)
n1$print('chart1')
```




