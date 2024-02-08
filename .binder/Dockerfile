FROM rocker/binder:4.3.2
LABEL maintainer='Michael Weylandt'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/michaelweylandt/STA9750-2024S/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2024-02-08/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
