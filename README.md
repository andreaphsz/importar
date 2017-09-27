# importar

The goal of 'importar' is to prevent namespace conflicts by having loaded a lot of R packages. So 'importar' makes it easy to assign a (short) alias to a package or a function.

## Installation

You can install 'importar' from GitHub with:

``` r
devtools::install_github("andreaphsz/importar")
```

or from CRAN with:

``` r
install.packages("importar")
```

## Example

This is an example which shows you how to assign a short alias to the 'dplyr' package.

``` r
## assign 'd' to 'dplyr' and use 'dplyr' functions by invoking the '$' operator.
import(dplyr, d)
df <- data.frame(a=1:3, b=4:6)
df %>% d$filter(a == 2)
```

You can also assign an alias to functions to prevent namespace conflicts.
```r
import_fun(dplyr, filter, fil)
df <- data.frame(a=1:3, b=4:6)
fil(df, a == 2)
```
