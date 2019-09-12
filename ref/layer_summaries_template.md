---
output:
  html_document:
    toc: true
    toc_float: true
---

```{r setup, echo = FALSE, message = FALSE, warning = FALSE}
source(file.path(here::here(), "R", "setup.R"))
short_layer_web <- file.path(bhiprep_gh_raw, "master", "ref", "layer_summaries") # bhiprep_gh_raw defined in setup.R
```

## LAYERFULLNAME

[LAYERNAME](https://github.com/OHI-Science/bhi/blob/master/baltic/layers/LAYERFILENAME.csv)
*Units: UNITS*
*Category:*
*Subcategory:*
*Index Dimension: INDEXDIMENSION*
*Goal Targets: GOALTARGETS*

<br>

```{r, echo = FALSE, results = "hide"}
tmp <- tempfile(fileext = "Rmd")
on.exit(unlink(tmp))
download.file(file.path(short_layer_web, "LAYERNAME.Rmd"), tmp) 
```

```{r, child = tmp, echo = FALSE, results = "asis"} 
``` 

See [**THISGOAL**](link/to/dataprep/or/something) for more information about data and methods.

<br>

---- 