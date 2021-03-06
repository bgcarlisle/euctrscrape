# euctrscrape

## To install and use

Get `euctrscrape` from Github:

```
install.packages("devtools")
library(devtools)
install_github("bgcarlisle/euctrscrape")
library(euctrscrape)
```

Download registration dates for a EUCTR record:

```
> euctr_reg_dates("2004-000083-27")
[1] "2004-07-27" "2004-09-16" "2004-09-23" "2004-10-19" "2005-02-11"
```

Get the earliest registration date:

```
> dates <- euctr_reg_dates("2004-000083-27")
> dates[1]
[1] "2004-07-27"
```

Download the start date for a EUCTR record:

```
> euctr_start_date("2004-000083-27")
[1] "2004-09-19"
```

Get trial results for a EUCTR record:

```
> euctr_results_posted("2012-001661-32") ## This trial has results
$trial_results
[1] TRUE

$pub_date
[1] "2021-12-13"
```

```
> euctr_results_posted("2020-005087-66") ## This trial has no results
$trial_results
[1] FALSE

$pub_date
[1] NA
```
