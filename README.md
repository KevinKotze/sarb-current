
<!-- README.md is generated from README.Rmd. Please edit that file -->

## SARB Quarterly Bulletin Data - Current Release

This R package provides convenient access to the current data that
accompanies the South African Reserve Bank Quarterly Bulletin. Variables
that are of the same frequency have been converted to `tibble` format
and have been saved as `.RData` files. The names for each of these files
is as follows:

  - “sarb\_annual.RData”
  - “sarb\_quarter.RData”
  - “sarb\_month.RData”
  - “sarb\_week.RData”
  - “sarb\_day.RData”

Note that the weekly data has also been converted into monthly data for
your convenience.

The most recent description file that is provided by the SARB has been
saved in the “data-raw” sub-folder. It is included in both original
`.xlsx` and converted `.rds` format. The layout is consistent with the
way in which this data is provided.

## Installation

To install the repository from GitHub:

``` r
# install.packages("devtools")
devtools::install_github("KevinKotze/sarbQB")
```

## Usage

To view all of the data objects that are included in the package:

``` r
library(sarbQB)
data(package = 'sarbQB')
```

To look at how the data has been stored, where the column headers relate
to each of the alpha-numeric codes that are used by the SARB. The first
column is reserved for the date, which was created with the `lubridate`
package.

``` r
library(tidyverse)
sarb_quarter %>% 
  select(1:5) %>% 
  tail()
```
