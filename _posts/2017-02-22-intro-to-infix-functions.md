---
layout: post
title: 'Looking Both Ways - Infix Functions'
subtitle: Some %R% tips
use_math: false
bigimg: /img/2017-02-22/frogger.jpg
tags: [R]
comments: true
---


In your R journeys you may have come across some interesting functions
like `%*%`  or even `%in%`. One function that is particularly
helpful (and interesting) is the piping operator (`%>%`) from the
[magrittr
pacakge](https://cran.r-project.org/web/packages/magrittr/vignettes/magrittr.html).
You probably noticed that the piping operator is similar to the matrix
multiplication operator `%*%`, in that they are both *sandwich*
functions (may or may not be trying to coin this term right now), as the
function call is/are a symbol(s) enclosed by `%` on both sides. These
sandwich functions in R are actually members of a larger class of
functions, known as *infix*
[functions](https://en.wikipedia.org/wiki/Infix_notation). Most functions in R are *prefix* functions, meaning that the function is called, followed by the function's arguments such as in `mean(heights)`, `apply(w,1,mean)`, or `glm(y ~ x, data = data)`. Infix functions on the other hand are called in between two arguments.

```
param1 %infix_function% param2
```

Infix functions are everywhere in R, and understanding them can really improve intelligibility and development time. The most common infix functions include basic
addition, and subtraction (`+`, `-`) and all your other
arithmetic functions (you use them every day!).

Sometimes we might want to use our own infix functions.
We can define our own as follows:

    `%+2%` <- function(x, y){
    return(x + y + 2)
    }

So, what would `1 %+2% 1` result in?

In short, while these functions are, deep down, just regular functions, they can improve readability considerably in your code - imagine needing
to use `add(x,y)` or `multiply(a,b)` whenever you had to find the sum or product of numbers.

`(2+2) * 10 - 6` would turn into `subtract(multiply(add(2,2),10),6)`.
What a monster!

Some other exciting infix functions include:
`%%` ([binary modulus](https://cran.r-project.org/doc/manuals/r-release/R-lang.pdf)), `%/%` ([binary integer divide](https://cran.r-project.org/doc/manuals/r-release/R-lang.pdf)), `%in%` ([matching operator](https://cran.r-project.org/doc/manuals/r-release/R-lang.pdf)), `%o%` ([outer product](https://cran.r-project.org/doc/manuals/r-release/R-lang.pdf)), `%x%` ([Kronecker product](https://en.wikipedia.org/wiki/Kronecker_product))


For further reading, as always, Hadley has some great [stuff](http://adv-r.had.co.nz/Functions.html).
