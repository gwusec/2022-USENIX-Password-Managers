# Why Users (Don't) Use Password Managers at a Large Educational Institution -Supplemental material

This repository contains supplemental material to aid in the replication of our study as it was submitted to the [artifact evaluation process of USENIX Security](https://www.usenix.org/conference/usenixsecurity22/call-for-artifacts). Specifically, the following four items can be found in this repo:

* The survey as QSF-file
* Data set cleaned from identifiable information
* The analysis script for the quantitative analyses
* The codebook for the qualitative analyses

## The Survey As QSF-File

The [QSF-file](./password_manager_survey.qsf) contains all questions exported from [Qualtrics](https://www.qualtrics.com) and can be easily re-imported there. The survey has multiple sections as outlined in the paper. These sections are modeled in the Qualtrics survey. Refer to the [Qualtrics documentation](https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/import-and-export-surveys/) in order to learn how to import the survey back into Qualtrics.

## Data Set Cleaned From Identifiable Information

The data set is in CSV format, but using [semicolons](https://projectsemicolon.com/about-project-semicolon/) ";" as separators. This increases the compatibility with [Apple Numbers]() which we used to create the graphs. The first section of our analysis script will handle the parsing. If you want to use the data in your own script use the following syntax:

```R
read.csv("data_cleaned.csv",header=TRUE,sep=";",stringsAsFactors=TRUE,check.names = FALSE)
```

Use the (in the easiest case imported) QSF-file as reference for the dataset headers.

## The Analysis Script for the Quantitative Analyses

The script with all analyses run for the paper. The execution of this script requires R. It was tested with R version `4.2.0` running in [RStudio](https://www.rstudio.com/products/rstudio/download/) `2022.02.3 Build 492`. The following packages are needed to run the script: dplyr, AICcmodavg.

## The Jupiter Notebook Script with Statistical Tests

This script will perform a chi-squared test for password re-use across different techniques, followed by a post-hoc analysis. Using Jupiter Notebook, browse and open the file chi_test.ipynb and run it and it should print out the results.

## The Codebook for the Qualitative Analyses

The codebook of the qualitative analysis with counts for each of the codes.

## Reference

Peter Mayer, Collins W. Munyendo, Michelle L. Mazurek, and Adam J. Aviv. *Why Users (Don't) Use Password Managers at a Large Educational Institution*. 31st USENIX Security Symposium (USENIX Security 22). 2022. [https://www.usenix.org/conference/usenixsecurity22/presentation/mayer](https://www.usenix.org/conference/usenixsecurity22/presentation/mayer).