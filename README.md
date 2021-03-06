
<!-- README.md is generated from README.Rmd. Please edit that file -->

[![Last-changedate](https://img.shields.io/badge/last%20change-2020--10--15-brightgreen.svg)](https://github.com/adamhsparks/rice.awd.pests/commits/master)
[![minimal R
version](https://img.shields.io/badge/R%3E%3D-4.0.3-brightgreen.svg)](https://cran.r-project.org/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3889800.svg)](https://doi.org/10.5281/zenodo.3889800)

Research compendium for a report on the effects of using alternate wetting and drying irrigation techniques and nitrogen rates on sheath blight disease in rice paddies.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Compendium DOI:

<a href="http://dx.doi.org/xxxxxxx" class="uri">http://dx.doi.org/xxxxxxx</a>

The files at the URL above will generate the results as found in the
publication. The files hosted at
<a href="https://github.com/adamhsparks/rice-awd-shb" class="uri">https://github.com/adamhsparks/rice-awd-shb</a>
are the development versions and may have changed since the report was
published.

### Data DOI:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3889800.svg)](https://doi.org/10.5281/zenodo.3889800)

The raw data from this project are released and publicly available from
Zenodo under a [Creative Commons Attribution 4.0
International](http://creativecommons.org/licenses/by/4.0/legalcode)
licence.

### Authors of this repository:

Adam H. Sparks
(<a href="mailto:adam.sparks@usq.edu.au" class="email">adam.sparks@usq.edu.au</a>)

Nancy P. Castilla
(<a href="mailto:n.castilla@irri.org" class="email">n.castilla@irri.org</a>)

B. Ole Sander
(<a href="mailto:b.sander@irri.org" class="email">b.sander@irri.org</a>)

Michael Noel

### Published in:

Sparks, A, xxxxx

### Overview of contents

This repository is our research compendium for our analysis of the
effects of alternate wetting and drying irrigation technology on rice
sheath blight disease. The compendium contains all data, code, and text
associated with the publication. The `Rmd` files in the
`analysis/paper/` directory contain details of how all the analyses
reported in the paper were conducted, as well as instructions on how to
rerun the analysis to reproduce the results. The `data/` directory in
the `analysis/` directory contains all the raw data. The `data-raw`
directory contains extra files to check weather for differences between
seasons, that are not included in the actual analysis.

### The supplementary files

The `data-raw` directory contains:

-   a IRRI\_weather\_data.R, a file used to check weather data from IRRI
    weather stations to ensure that there was no significant difference
    in weather between seasons

The `analysis/` directory contains:

-   the manuscript as submitted (in MS Word format) and it’s Rmd source
    file

-   supplementary information source files (in R markdown format) and
    executed versions

-   all the figures that are included in the paper (in the `figures/`
    directory)

### The R package

This repository is organized as an R package. Mostly I used the R
package structure to help manage dependencies, to take advantage of
continuous integration for automated code testing, and so I didn’t have
to think too much about how to organise the files.

To download the package source as you see it on GitHub, for offline
browsing, use this line at the shell prompt (assuming you have Git
installed on your computer):

    git clone https://github.com/adamhsparks/rice-awd-shb.git

Once the download is complete, open the `rice.awd.shb.Rproj` in RStudio
to begin working with the package and compendium files.

The package has a number of dependencies on other R packages, and
programs outside of R. These are listed at the bottom of this README.
Installing these can be time-consuming and complicated, so we’ve used a
Docker image. The Docker image includes all the necessary software, code
and data to run our analysis. The Docker image may give a quicker entry
point to the project, and is more self-contained, so might save some
fiddling with installing things.

### The Docker image

A Docker image is a lightweight GNU/Linux virtual computer that can be
run as a piece of software on Windows and OSX (and other Linux systems).
To capture the complete computational environment used for this project
we have a Dockerfile that specifies how to make the Docker image that we
developed this project in. The Docker image includes all of the software
dependencies needed to run the code in this project, as well as the R
package and other compendium files. To launch the Docker image for this
project, first, [install Docker](https://docs.docker.com/installation/)
on your computer. Then at a command line prompt, use the following
commands to start the instance.

    docker pull adamhsparks/rice-awd-shb
    docker run -dp 8787:8787 adamhsparks/rice-awd-shb

This will start a server instance of RStudio. Then open your web browser
at localhost:8787 or or run `docker-machine ip default` in the shell to
find the correct IP address, and log in with rstudio/rstudio.

Once logged in, use the Files pane (bottom right) open the folder for
this project, and open the `.Rproj` file for this project. Once that’s
open, you’ll see the `analysis/paper` directory in the “Files” pane
where you can find the Rmarkdown document, and knit it to produce the
results in the paper. More information about using RStudio in Docker is
available at the [Rocker](https://github.com/rocker-org)
[wiki](https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image)
pages.

We developed and tested the package on this Docker container, so this is
the only platform that we’re confident it works on, and so recommend to
anyone wanting to use this package to generate the vignettes, etc.

Citation
--------

Please cite this compendium as:

> Authors, (2020). *Reproducible Research Compendium for Analysing
> Effects of Water Management and Nitrogen on Rice Sheath Blight*.
> Accessed 15 Oct 2020. Online at
> <a href="https://doi.org/xxx/xxx" class="uri">https://doi.org/xxx/xxx</a>

Licenses
--------

Manuscript: [CC-BY-4.0](http://creativecommons.org/licenses/by/4.0/)

Code: [MIT](http://opensource.org/licenses/MIT) year: 2020, copyright
holder: Adam Sparks

Data: [CC-4.0](http://creativecommons.org/licenses/by/4.0/legalcode)
attribution requested in reuse

Dependencies
------------

I used [RStudio](http://www.rstudio.com/products/rstudio/) on MacOS. See
the colophon section of the docx file in `analysis/paper` for a full
list of the packages that this project depends on.

Contact
-------

Adam Sparks, Associate Professor, Centre for Crop Health  
University of Southern Queensland, West St.  
Toowoomba, Qld 4350 Australia

(+61) 7.4631.1948
<a href="mailto:adam.sparks@usq.edu.au" class="email">adam.sparks@usq.edu.au</a>  
<a href="https://adamhsparks.com/" class="uri">https://adamhsparks.com/</a>
