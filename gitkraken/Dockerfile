FROM debian:9

RUN apt-get update && apt-get -y install \
        wget \
        gconf2 \
        libgtk2.0-0 \
        libnotify4 \
        libnss3 \
        xdg-utils \
        gvfs-bin \
        libxtst6 \
        libxkbfile1 \
        libx11-xcb-dev \
        libxss1 \
        libasound2 \
        libgnome-keyring-common \
        libgnome-keyring-dev \
        curl \
        libcurl3 \
        firefox-esr \
        libcanberra-gtk-module \
        libcanberra-gtk3-module \
        packagekit-gtk3-module \
        libcurl3-gnutls \
        python

COPY gitkraken-amd64.deb /gitkraken-amd64.deb
RUN dpkg -i /gitkraken-amd64.deb \
        && rm /gitkraken-amd64.deb

COPY run.sh /run.sh
RUN chmod +x /run.sh

CMD ["/run.sh"]

