---
layout: post_ak
title: Minimal Example
root: "../../../../"
comments: true
---

A quote:

> Markdown is not LaTeX.

To compile me, run this in R:

    library(knitr)
    knit('001-minimal.Rmd')

See [output here](https://github.com/yihui/knitr-examples/blob/master/001-minimal.md).

## code chunks

A _paragraph_ here. A code chunk below (remember the three backticks):

{% highlight r %}
1+1
.4-.7+.3 # what? it is not zero!
{% endhighlight r %}

## graphics

It is easy. I did not really show the plot here; if you want it, remove the option `eval=FALSE` from the chunk header below.


```r
plot(1:10)
hist(rnorm(1000))
```


## inline code

Yes I know the value of pi is `3.1416`, and 2 times pi is `6.2832`.

## math

Sigh. You cannot live without math equations. OK, here we go: $\alpha+\beta=\gamma$. Note this is not supported by native markdown. You probably want to try RStudio, or at least the R package **markdown**, or the function `knitr::knit2html()`.

## nested code chunks

You can write code within other elements, e.g. a list

1. foo is good
    
    ```r
    strsplit("hello indented world", " ")[[1]]
    ```
    
    ```
    ## [1] "hello"    "indented" "world"
    ```


2. bar is better

## conclusion

Nothing fancy. You are ready to go. When you become picky, go to the [knitr website](http://yihui.name/knitr/).

![knitr logo](http://yihui.name/knitr/images/knit-logo.png)
