Aprendiendo GGplot2
================

## Librerias

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✓ ggplot2 3.3.5     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.4     ✓ dplyr   1.0.7
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   2.0.1     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(devtools)
```

    ## Loading required package: usethis

``` r
library(usethis)
```

## Correr Siempre

``` r
 usethis::use_git(message = "V1")
```

    ## ✓ Setting active project to '/cloud/project'

## leyendo Dtos

``` r
# View(mpg) #leyendo datos
attach(mpg)
# str(mpg)
```

## Scatter plot

[figuras](https://www.dropbox.com/s/h18nmf5vahdidzs/figuras.Rmd?dl=0)

``` r
d <- ggplot(mpg, aes(displ,hwy)) # PASO 1
(d + geom_point())
```

![](README_files/figure-gfm/graf-disp-hwy-1.png)<!-- -->

``` r
(d + geom_point(shape=23, size=4, color="red",fill="yellow") )
```

![](README_files/figure-gfm/graf-disp-hwy2-1.png)<!-- -->

``` r
names(mpg)
```

    ##  [1] "manufacturer" "model"        "displ"        "year"         "cyl"         
    ##  [6] "trans"        "drv"          "cty"          "hwy"          "fl"          
    ## [11] "class"

``` r
d <- ggplot(mpg, aes(displ,hwy,col=cyl)) # PASO 1
(d + geom_point())
```

![](README_files/figure-gfm/graf-cilindros-1.png)<!-- -->

``` r
(d + geom_point(aes(color=class),size=4))
```

![](README_files/figure-gfm/grafica-color-1.png)<!-- -->

``` r
(d + geom_point(aes(color=drv),size=4))
```

![](README_files/figure-gfm/grafica-color-2.png)<!-- -->

``` r
 gitcreds::gitcreds_set()
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
```

``` r
gh::gh_whoami()
```
