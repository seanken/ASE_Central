# Central repo for allele specific expression related tools
In order to perform all the analysis tasks we had to perform for our allele specific expression manuscript (link to be added), we had to build many tools, each with it's own repo. This repo is one central location for all of the others.

## ASE upstream pipelines

In order to perform analysis of our data at the allele specific expression level we had to build a pipeline to extract ASE information from single nuclei data (works with single cell and (some) spatial data as well). This pipeline is available [here](https://github.com/seanken/ASE_pipeline). Note this repo has a more updated version of the pipeline, but the original pipeline used in the paper is also present. The script to extract ASE data from long read data is also available in that repo.

## Downstream analysis tools

For downstream analysis, we built tools in R and python.

For R, we built a R package we call scAlleleExpression, which can be found [here](https://github.com/seanken/scAlleleExpression). This package is built to load data from our ASE pipeline (see above) into R, as well as to perform downstream statistical analysis.

For python we are in the process of building a python package, scASE_py, that is meant to work in a similar way to scAllleleExpression, except in python. The package can be found [here](https://github.com/seanken/scASE_py). So far the package can load the output of our pipeline into python (as pandas data frames). The downstream analysis is still a work in progress, so far only works with scDali (though it does run into issues when doing so).

## Figures for the paper

A repo with information about how the different figures in the paper were generated (both scripts to generate the underlying data and, in many cases, the code to create the figures themselves) is available [here](https://github.com/seanken/ASE_Plots). It is loosely organized by figure and subfigure. Note as of this writing it still has local paths from our cluster, so won't work out of the box, and instead are meant as a way to share the code for others to repurpose/read.

## Other repos

Not built only for this paper, but we also built a QC tool that was used in this analysis (and can be used in any CellRanger experiment) which can be found [here](https://github.com/seanken/CellLevel_QC).

Will add pointers to some repos related to the upstream processing of the long read data as well.

