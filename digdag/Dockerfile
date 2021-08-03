FROM openjdk:11.0-jdk-slim-buster

ENV DIGDAG_VERSION=0.10.1
WORKDIR /src

RUN apt-get update \
  && apt-get install -y \
    bash \
    curl \
    git \
    wget \
    postgresql-client \
    ca-certificates \
    make \
    zip \
    python3-dev \
    python3-pip \
    ruby \
    ruby-dev \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* \
 && pip3 install --upgrade pip \
 && pip3 install awscli \
 && ln -s /usr/bin/python3 /usr/bin/python \
 && curl -o /usr/local/bin/digdag --create-dirs -L "https://dl.digdag.io/digdag-${DIGDAG_VERSION}" \
 && chmod +x /usr/local/bin/digdag


ENTRYPOINT ["java", "-jar", "/usr/local/bin/digdag"]
