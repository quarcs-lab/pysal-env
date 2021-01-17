## Open notebooks for learning data science with R studio

RStudio: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/quarcs-lab/r-env/main?urlpath=rstudio)

RShiny: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/quarcs-lab/r-env/main?urlpath=shiny/bus-dashboard/)



## Permanent Online Environment

The notebooks can be executed online at [GESIS Notebooks](https://notebooks.gesis.org). Just copy the URL of this repository and paste it on the [BINDER form](https://notebooks.gesis.org/binder/)

- To open a virtual R Studio session, make sure you change you click on `File` and change it to `URL`. Then, write `rstudio` in the field `URL to open (optional)`. Finally, click on `launch`.  



This environment contains the package `ExPanDaR` and its dependencies

- https://cran.r-project.org/web/packages/ExPanDaR/index.html
- https://joachim-gassen.github.io/ExPanDaR/
- https://joachim-gassen.github.io/ExPanDaR/reference/index.html
- https://cran.r-project.org/web/packages/ExPanDaR/vignettes/ExPanD_notebook.html
- https://cran.r-project.org/web/packages/ExPanDaR/vignettes/ExPanDaR-functions.html
- https://cran.r-project.org/web/packages/ExPanDaR/vignettes/use_ExPanD.html


Binder supports using R and RStudio, with libraries pinned to a specific
snapshot on [MRAN](https://mran.microsoft.com/documents/rro/reproducibility).


---


## Terms of Use

Materials are licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).


[![Creative Commons Lizenzvertrag](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)


---

**Note:** We recommend to follow [r-conda](https://github.com/binder-examples/r-conda) instead. Especially if you want to use a specific version of R or need faster build times.

**Note:** Another alternative is to use the [holepunch package for R](https://karthik.github.io/holepunch/articles/getting_started.html).

### Requirements and suggestions

You need to have a `runtime.txt` file that is formatted like:

```
r-<YYYY>-<MM>-<DD>
```

where YYYY-MM-DD is a snapshot at MRAN that will be used for installing
libraries. In this line, you can request a [specific
version of R](https://github.com/jupyter/repo2docker/pull/772#issue-313426641). To do this list the version between the 'r'
and the year, as in `r-3.6-2019-09-24`. Right now the default version of R is 3.6.

> We recommend using https://github.com/binder-examples/r-conda for faster installs than using a `install.R`

To install R libraries (or packages) you can add an [`install.R`](install.R) file that specifies one library to install per line.

Both [RStudio](https://www.rstudio.com/) and [IRKernel](https://irkernel.github.io/)
are installed by default, so you can use either the Jupyter notebook interface or
the RStudio interface.

This repository also contains an example of a [Shiny app](https://github.com/binder-examples/r/tree/master/bus-dashboard).

### URL addresses for RStudio and Shiny environments

The Binder repository can be used to allow anyone to access an RStudio environment containing our code and data right
in their web browser. It also allows hosting a Shiny app. For those purposes, we have to append a bit of text to the
URL of our Binder repository, which we can find out at [mybinder.org](https://mybinder.org/) when we enter
the URL of our original repository from GitHub or Figshare, etc.

- For the RStudio environment, we must add the following at the end of the URL: `?urlpath=rstudio`

  - Example: http://mybinder.org/v2/gh/quarcs-lab/r-env/main?urlpath=rstudio

- For the Shiny app environment, we must add the following at the end of the URL: `?urlpath=shiny`. In this case, we
also have to note that if the Shiny app files are located in a folder, this folder should be specified in the URL,
after a slash. We would then also have to put in a trailing slash at the end of the URL, and to avoid spaces in the
name of the repository, placing instead a hyphen (the reason is that spaces are converted to `%20`).

  - Example 1: http://mybinder.org/v2/gh/quarcs-lab/r-env/main?urlpath=shiny/bus-dashboard/
  - Example 2: http://mybinder.org/v2/gh/binder-examples/r/master?urlpath=shiny/bus-dashboard/
