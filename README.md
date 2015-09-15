cleanoccs
=========



[![Build Status](https://travis-ci.org/sckott/cleanoccs.svg?branch=master)](https://travis-ci.org/sckott/cleanoccs)
[![codecov.io](http://codecov.io/github/sckott/cleanoccs/coverage.svg?branch=master)](http://codecov.io/github/sckott/cleanoccs?branch=master)

__Clean Biological Occurrence Records__

Clean using the following use cases:

* Impossible lat/long values: e.g., latitude 75
* Incomplete cases: one or the other of lat/long missing
* Unlikely lat/long values: e.g., points at 0,0
* Political centroids: unlikely that occurrences fall exactly on these points, more likely a 
default position
* Herbaria/Museums: many specimens may have location of the collection they are housed in
* Habitat type filtering: e.g., fish should not be on land; marine fish should not be in fresh water
* Deduplication: try to identify duplicates, esp. when pulling data from multiple sources, e.g., can try to use occurrence IDs, if provided
* Check for contextually wrong values: That is, if 99 out of 100 lat/long coordinates are within the continental US, but 1 is in China, then perhaps something is wrong with that one point
* Outside political boundary: User input to check for points in the wrong country, or points outside of a known country
* ...

## Install


```r
devtools::install_github("sckott/cleanoccs")
```


```r
library("cleanoccs")
```

## Meta

Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
