FROM debian:9

RUN apt-get update && apt-get -y install \
        gconf2 \
        libnotify4 \
        libnss3 \
        xdg-utils \
        gvfs-bin \
        libxkbfile1 \
        libxss1 \
        libasound2 \
        libcanberra-gtk-module \
        libcanberra-gtk3-module \
        packagekit-gtk3-module

COPY gitkraken-amd64.deb /gitkraken-amd64.deb
RUN dpkg -i /gitkraken-amd64.deb \
        && rm /gitkraken-amd64.deb

COPY run.sh /run.sh
RUN chmod +x /run.sh

CMD ["/run.sh"]

