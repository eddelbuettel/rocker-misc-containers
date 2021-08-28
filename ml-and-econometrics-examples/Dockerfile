## Emacs, make this -*- mode: sh; -*-

## We use bspm to get R packages autoMAGICally as r-cran-* packages.  See
## Ucar and Eddelbuettel (2021) at https://arxiv.org/abs/2103.08069 for more
FROM rocker/r-bspm:20.04

LABEL org.opencontainers.image.licenses="GPL-2.0" \
      org.opencontainers.image.source="https://github.com/eddelbuettel/rocker-adjoc-ml/" \
      org.opencontainers.image.authors="Dirk Eddelbuettel <edd@debian.org>"

## refresh package cache
RUN apt-get update -qq
## && apt-get install -y -t unstable --no-install-recommends \

## install packages
RUN install.r \
    Hmisc \
    R.utils \
    biglm \
    data.table \
    ggplot2 \
    grf \
    lfe \
    lmtest \
    mlogit \
    mltools \
    randomForest \
    readr \
    readxl \
    sandwich \
    stringi \
    stringr \
    xlsx \
    zoo 

## if needed follow up with other packages via
##   install.r aa bb cc
##   installGithub. dd/ee ff/gg

## Commenting this out means we start by default in R
##CMD ["bash"]
