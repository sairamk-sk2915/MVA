Social Media
================
Satya Shiva Sai Ram Kamma
2024-03-25

## Social Media

``` r
library(readxl)
```

    ## Warning: package 'readxl' was built under R version 4.3.2

``` r
data <- read_excel("social_media_cleaned.xlsx")
data <- data[, -1]
distance = as.matrix(dist(scale(data)))
sum(distance[17,])
```

    ## [1] 76.43928
