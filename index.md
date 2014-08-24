---
title       : Slidify Project
subtitle    : Test
author      : Herden
job         : in R
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## R expression

```r
## Exponentiation followed by multiplication 
4*5^2
```

[1] 100

```r
## Area of a circle of radius r=5
pi*5^2
```

[1] 78.54

```r
## Natural logarithm of 1 multiplied by exponential (function) evaluated at 0
log(1)*exp(0)
```

[1] 0





---

## Slide3



```r
library(shiny)
```

```
## Warning: package 'shiny' was built under R version 3.1.1
```

```r
library(markdown)
load(url("http://s3.amazonaws.com/assets.datacamp.com/course/dasi/nc.Rdata"))
slidifyUI(
  navbarPage("App Title",
                   tabPanel("Plot",
                            
                            sidebarLayout(
                              
                              # Application title
                              headerPanel("Newborn weight"),
                              
                              sidebarPanel(
                                selectInput("variable", "Variable:",
                                            list("Habit " = "habit", 
                                                 "Gender" = "gender", 
                                                 "Whitemom" = "whitemom",
                                                 "Mature" = "mature")),
                                
                                checkboxInput("outliers", "Show outliers", FALSE)
                              )
                            )
                            
                   ),
                   
                   mainPanel(
                     h3(textOutput("caption")),
                     plotOutput("weightPlot")
                   ),

                   navbarMenu("More",
                   tabPanel("About",
    fluidRow(
      column(6,
          includeMarkdown("about.txt")
      )
                  )
             )
          )

))
```

```
## Error: could not find function "slidifyUI"
```


--- .class #id 

## Slide4

---


