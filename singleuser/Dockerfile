
ARG DOCKER_NOTEBOOK_IMAGE
FROM $DOCKER_NOTEBOOK_IMAGE

# USER root

# # Ubuntu 18.04 have tesseract-ocr v4 in the main repository, hence no need to add the tesseract repository on it.
# RUN if [ "${UBUNTU_VERSION}" = "16.04" ]; then \
#         echo "VERSION ${UBUNTU_VERSION}. Adding repository for tesseract 4." \
#         && apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CEF9E52D \
#         && echo "deb http://ppa.launchpad.net/alex-p/tesseract-ocr/ubuntu xenial main\ndeb-src http://ppa.launchpad.net/alex-p/tesseract-ocr/ubuntu xenial main " >> /etc/apt/sources.list; \
#     else \
#         echo "VERSION ${UBUNTU_VERSION}. Skipping repository adding."; \
#     fi \
#     && apt-get update \
#     && apt-get install tesseract-ocr -y \
#     && apt-get install -y python3-pip \
#     && apt-get install -y poppler-utils \
#     && pip3 install jupyter -U && pip3 install jupyterlab && pip3 install pandas \
#     && apt-get clean \
#     && apt-get autoremove
    
ARG JUPYTERHUB_VERSION
RUN python3 -m pip install --no-cache jupyterhub==$JUPYTERHUB_VERSION
