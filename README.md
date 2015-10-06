# R Formatter

[![Travis-CI Build Status](https://travis-ci.org/evolutics/RFormatter.svg?branch=master)](https://travis-ci.org/evolutics/RFormatter)

The R Formatter formats R source code. It is very much based on [formatR](http://yihui.name/formatR), but tries to improve it by heuristics. For example, spaces can be forced around the division operator `/`.

## Installation

In R, run

    > install.packages("RFormatter")

## Usage

Try

    > writeLines(RFormatter::format_R_source_code("if (b) { f() }"))

Get more help with

    > ?RFormatter::format_R_source_code

### Command-Line Utility

To format a source file `source.R` via a command-line interface, do the following. **Warning: the original file is overwritten, so better back it up first! Use this at your own risk.** Call

    $ Rscript [utility] source.R

where `[utility]` is the path given by

    > system.file("exec", "utility.R", package = "RFormatter")

## Related Projects

Have a look at Yihui Xie’s [formatR](http://yihui.name/formatR).
