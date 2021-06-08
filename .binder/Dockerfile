FROM rocker/binder:4.0.2
LABEL maintainer='Unknown'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/libjohn/workshop_webscraping/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2021-06-08/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
