# R Formatter

[![Build status](https://travis-ci.org/evolutics/RFormatter.svg?branch=master)](https://travis-ci.org/evolutics/RFormatter)
[![CRAN version](http://www.r-pkg.org/badges/version/RFormatter)](http://cran.r-project.org/package=RFormatter)

The R Formatter formats R source code. It is very much based on [formatR](http://yihui.name/formatR), but tries to improve it by heuristics. For example, spaces can be forced around the division operator `/`.

The following features are added to [formatR](http://yihui.name/formatR).

* Removing more trailing whitespace.
* Adding spaces around more operators of your choice.

## Installation

In R, run

    > install.packages("RFormatter")

## Usage

Try

    > RFormatter::format_R_source_code("if (b) { f() }")
    > RFormatter::format_R_source_code("p = 2", list(arrow = TRUE))
    > RFormatter::format_R_source_code("(k/n)^x", spaced_operators = c("/"))

Get more help with

    > ?RFormatter::format_R_source_code

### Command-Line Utility

To format a source file `source.R` via a command-line interface, do the following. **Warning: the original file is overwritten, so better back it up first! Use this at your own risk.** Run

    $ Rscript [utility] source.R

where `[utility]` is the path given by

    > system.file("exec", "utility.R", package = "RFormatter")

## Related Projects

Have a look at Yihui Xie’s [formatR](http://yihui.name/formatR).
