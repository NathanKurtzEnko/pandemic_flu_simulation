# Introduction

This repository contains the code and data for the project of ISYE 6644, Summer 2025. This project pertains to deterministic simulation of pandemic influenza in the United States and the impact of intervention strategies. 

# Respository Contents

Relevant data for the analysis are found in the `data` directory.

Notes on referenced scholarly articles and other documents related to the project are located in the `docs` directory.

The `renv` directory and `renv.lock` file are used for managing R package dependencies. These should mainly be ignored unless you need to rebuild the R environment needed to run the code in the project report.

The main code for this project is the `project_report.qmd` file. This contains all code and analysis for the final report.

References for the project are recorded in BibTeX format in the `references.bib` file.

# Prerequisites

This project requires R (version 4.2 or higher) and Quarto. 

Instruction for installing R can be found at https://cran.r-project.org/.

Instructions for installing Quarto can be found at https://quarto.org/docs/get-started/.

# Setting Up the Environment

This project uses the `renv` package to manage R package dependencies. To set up the R environment, follow these steps:

```
install.packages("renv")  # Install renv if not already installed
renv::restore()           # Restore the project environment
```

This will install all the necessary R packages as specified in the `renv.lock` file.

Unfortunately, sometimes there are issues installing individual packages. If you encounter issues, you can try installing the packages manually.

```
renv::install(c("dplyr", "tidyr", "purrr", "readr", "ggplot2"))
renv::install(c("finalsize", "epiparameter"))
renv::install("epidemics", repos = 'https://epiverse-trace.r-universe.dev')
renv::install(c("tidycensus", "knitr"))
renv::install("quarto")
```

# Getting Necessary Data

Most data are accessed via function from the package dependencies. However, contact data was obtained from the study [Breen et al. (2022)](https://doi.org/10.1371/journal.pcbi.1010742). The data is available at https://osf.io/aecwn/. If need by, you can request access to the data, download it, unzip any compressed files, and place them in the `data` directory accordingly.
