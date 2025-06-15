FROM ghcr.io/lescai-teaching/bigdata-rstudio:latest

ENV NB_USER=rstudio

# Installa Python, pip e JupyterLab
RUN apt-get update && apt-get install -y python3 python3-pip \
 && pip3 install --upgrade pip \
 && pip3 install jupyterlab

EXPOSE 8888

# Avvia JupyterLab
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--no-browser"]

USER ${NB_USER}
WORKDIR /home/${NB_USER}
