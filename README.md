
<!-- README.md is generated from README.Rmd. Please edit that file -->

# industRial

<!-- badges: start -->
<!-- badges: end -->

`{industRial}` is the companion package to the book [industRial Data
Science](https://j-ramalho.github.io/industRial/index.html). It provides
data sets and functions to complete the case studies and contains the
book original files and exercises.

## Installation

<!-- You can install the released version of industRial from [CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("industRial")
```
-->

You can install the development version from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("J-Ramalho/industRial")
```

## Example

The *Pareto* case study explores the creation of pareto charts and how
to make use of them in a day to day situation.

``` r
library(industRial)
library(qicharts2)
d_type <- dial_control %>% pull(Defect) %>% as.character()
paretochart(
  d_type,
  title = "Watch Dial polishing",
  subtitle = "Pareto chart",
  ylab = "Percentage of deffects",
  xlab = "Deffect type",
  caption = "Source: Dial Production Team"
) +
  theme_industRial()
```

<img src="man/figures/README-example-1.png" width="80%" />

<!-- You'll still need to render `README.Rmd` regularly, to keep `README.md` up-to-date. `devtools::build_readme()` is handy for this. You could also use GitHub Actions to re-render `README.Rmd` every time you push. An example   can be found here: <https://github.com/r-lib/actions/tree/master/examples>.
In that case, don't forget to commit and push the resulting figure files, so they display on GitHub and CRAN.
-->

## Issues

To report any bug or make suggestions please open an issue:
[industRialds/issues](https://github.com/J-Ramalho/industRial/issues)
