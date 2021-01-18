FROM node:8.11
MAINTAINER Brian Douglass

RUN apt-get update
RUN apt-get install -y \
    libstdc++6 \
    binutils \
    python3-apt \
    python3-debian \
    python3-lxml \
    python3-magic \
    python3-simplejson \
    python3-xdg \
    python3-yaml \
    squashfs-tools
RUN npm install supervisor -g
RUN wget https://launchpad.net/~bhdouglass/+archive/ubuntu/clickable/+files/click-reviewers-tools_0.50_all.deb && \
    dpkg -i click-reviewers-tools_0.50_all.deb && \
    rm click-reviewers-tools_0.50_all.deb
RUN mkdir /srv/screenshots

EXPOSE 8080
WORKDIR /srv/openstore
CMD ["npm", "run", "dev"]
