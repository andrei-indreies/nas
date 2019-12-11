FROM centos:7

RUN set -ex; \
yum install -y https://github.com/MediaBrowser/Emby.Releases/releases/download/4.3.0.30/emby-server-rpm_4.3.0.30_x86_64.rpm; \
yum clean all; \
rm -rf /var/cache/yum; \
rm -rf /tmp/*

USER emby
WORKDIR /opt/emby-server
ENV EMBY_DATA /var/lib/emby

CMD /opt/emby-server/bin/emby-server