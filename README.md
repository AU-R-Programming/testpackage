
# An example for office hours

Explain what your package is doing here:

``` r
library(testpackage)
set.seed(1)
gender <- sample(c(0,1), size = 100, replace = TRUE) # x1 (input)
age <- round(runif(100, 18, 80)) # x2 (input)
xb <- 3.5*gender + 0.2*age - 9 # w1*x1 + w2*xw + b
p <- 1/(1 + exp(-xb))
y <- rbinom(n = 100, size = 1, prob = p) # output
regr <- cbind(gender, age) # create matrix of inputs
```

Find the weights for the neural net:

``` r
weights <- neural_net(y = y, X = regr)
weights
```

    ## [1]   881.77986    42.63734 -1883.78980
