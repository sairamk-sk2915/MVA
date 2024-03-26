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

``` r
library(readxl)
data <- read_excel("social_media_cleaned.xlsx")
data <- data[, -1]
scale <- scale(data)

classcov <- cor(data)
classmean <- colMeans(data)

scale <- mahalanobis(data, classmean, classcov)
scale
```

    ##  [1] 452.02507  37.01885  55.02136  13.47693 118.18625  96.57180  10.41160
    ##  [8]  23.16155  70.73080 110.83654  39.59404  15.65044 223.96974  14.98973
    ## [15]  48.57144  20.12693 125.24411  13.00150  39.64637 162.38246  66.56728

``` r
print(scale[17])
```

    ## [1] 125.2441
