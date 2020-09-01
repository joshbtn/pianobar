#See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.134.1/containers/debian/.devcontainer/base.Dockerfile
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# ** [Optional] Uncomment this section to install additional packages. **
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    libao-dev \
    libavcodec-dev \
    libavfilter-dev \
    libavformat-dev \
    libavutil-dev \
    libcurl4-gnutls-dev \
    libgcrypt20-dev \
    libjson-c-dev \
    libpth-dev \
    pkg-config \
    build-essential

RUN cd /tmp && \
    wget https://golang.org/dl/go1.15.1.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.15.1.linux-amd64.tar.gz && \
    ln -s /usr/local/go/bin/go /usr/bin/go && \
    ln -s /usr/local/go/bin/gofmt /usr/bin/gofmt