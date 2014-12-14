# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

Extract zipped data, load them in R (function 'read.csv') and check dataframe structure.



```r
myfiles <- unzip(zipfile = "activity.zip", list = T) # read file name

unzip(zipfile = "activity.zip") # unzip the file

mydata <- read.csv(file = myfiles[1,1]) # load the file into R

str(mydata)
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Factor w/ 61 levels "2012-10-01","2012-10-02",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```


It would be better to have 'date' coded as a date in R format. I create a new variable


```r
mydata$date_r <- as.POSIXct(mydata$date)
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
