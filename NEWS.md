climatrends 0.2 (2022-02-14)
=========================

* Fix an issue in computing large areas with nasapower
* Add paper

climatrends 0.1.7 (2020-05-22)
=========================

* Add suggested CITATION
* Fix documentation typos
* Fix a bug in computing equation 'c' in `GDD()`
* Improve speed of functions `GDD()` and `late_frost()`
* package 'sf' is a suggestion not dependency

climatrends 0.1.6 (2020-05-19)
=========================

### NEW FEATURES

* New function `crop_sensitive()` to compute crop sensitive indices.
* New function `late_frost()` to compute late spring frost.
* Export function `get_timeseries()`
* Enable future modular expansion of data sources using API clients by creating specific functions that are called with the argument `data.from` in `get_timeseries()`
* Enable argument `last.day`, optional to `span`, when indices are retrieved with focus on time series analysis
* Enable data retrieve from large areas in 'nasapower' by clustering the lonlat points with `stats::hclust()`
* Methods for objects of classes 'vector' (default), 'matrix', 'array', 'data.frame' and 'sf'. The last two with focus in retrieve data from external sources.
* Remove dependency from 'tibble' which was basically to provide a 'cool' printing method
* Implement a `print()` method for objects that inherits the class 'clima_df'
* Calls from "nasapower" can be adjusted with argument `pars`, mainly for `temperature()`, `GDD()` and `ETo()`. Details in the function documentation
* New `temperature()` indices provided. Details in the function documentation
* Function `GDD()` applies two equations adjustments for cold zones and one for warm zones with the argument `equation`. Details in the function documentation
* Function `GDD()` now allows to return the raw daily gdd or number of days to reach the accumulated gdd (the default in previous versions) using the argument `return.as`

### CHANGES IN BEHAVIOUR

* New default method in all functions which uses a vector as main input
* Change order of `GDD()` arguments. Previous versions used `GDD(object, day.one = NULL, degree.days = NULL, base = 10, span = 150, ...)`. From now on `GDD()` default behaviour is `GDD(object, ..., base = 10)`, with additional arguments are passed through `...` in each defined method. The function return by default the accumulated degree-days across the series.

climatrends 0.1.0 (2020-02-20)
=========================
* Add examples of data set from local sources `modis()` and `chirp()`
* Add details for the utilisation of data set daylight to compute the percentage of daylight based on lat and month

climatrends 0.0.3 (2020-02-11)
=========================
* Fix mis-spelled words identified in CRAN checks
* Update references in function(s) description
* Update `R` to >= v3.5.0

climatrends 0.0.2 (2020-02-10)
=========================

* Remove non-ASCII characters from Description file
* Submit to CRAN

climatrends 0.0.1 (2020-02-08)
=========================

* Migrated functions from **gosset**