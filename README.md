
<!-- README.md is generated from README.Rmd. Please edit that file -->

## Mapgen

<!-- badges: start -->
<!-- badges: end -->

`mapgen` is an R package that performs gene mapping based on
functionally-informed genetic fine mapping.

## Installation

You can install the development version of `mapgen` from
[GitHub](https://github.com/xinhe-lab/mapgen) with:

``` r
# install.packages("devtools")
devtools::install_github("kevinlkx/mapgen")
```

Please install the following dependent R packages: `tidyverse`,
`data.table`, `bigsnpr`, `ggplot2`, `ggrepel`, `ggrastr`, `processx`
from CRAN, as well as `GenomicRanges`, `plyranges`, `rtracklayer` from
Bioconductor.

After installing, check that it loads properly:

``` r
library(mapgen)
```

## Overview of the workflow

**Example workflow from our heart single-cell study:**

We developed an integrated procedure that combines single-cell genomics
with novel computational approaches to study genetics of complex traits.

Main steps:

1.  Obtain cell-type-resolved open chromatin regions (OCRs) using
    scATAC-seq and snRNA-seq.
2.  Assess the enrichment of genetic signals of a trait of interest in
    OCRs across all the cell types.
3.  Perform Bayesian statistical fine mapping on trait-associated loci,
    using a informative prior that favors likely functional variants
    located in OCRs of enriched cell types.
4.  Assign the likely cell type(s) through which the causal variants act
    in most loci using fine-mapped SNPs and its associated cell type
    information.
5.  Use our novel gene mapping procedure to infer causal genes at each
    locus.

<img src="man/figures/workflow.overview.png" title="Overview of the workflow" alt="Overview of the workflow" width="75%" />

Please follow the
[tutorials](https://kevinlkx.github.io/mapgen/articles/index.html) to
learn how to use the package.
