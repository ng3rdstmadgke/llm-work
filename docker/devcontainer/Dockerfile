FROM mcr.microsoft.com/devcontainers/python:3.11-bullseye

RUN apt-get update && \
    apt-get install -y \
    bash-completion \
    iputils-ping \
    net-tools \
    make \
    gcc \
    jq \
    fzf \
    vim \
    git \
    curl \
    wget \
    less \
    groff \
    locales \
    default-mysql-client 

# ロケール設定
RUN echo 'ja_JP.UTF-8 UTF-8' >> /etc/locale.gen && \
    locale-gen && \
    update-locale LANG=ja_JP.UTF-8
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

# aws cli インストール
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install

COPY requirements.txt /tmp/requirements.txt
RUN pip install --upgrade pip && pip install -r /tmp/requirements.txt