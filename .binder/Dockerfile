FROM rocker/binder:3.6.0
LABEL maintainer='your_name'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/robschick/testbuild/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-07-30/')); devtools::install_deps()"
