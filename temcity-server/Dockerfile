FROM java:7

ENV TEAMCITY_DATA_PATH /data/teamcity
ENV TEAMCITY_PACKAGE TeamCity-9.1.1.tar.gz
ENV TEAMCITY_DOWNLOAD http://download.jetbrains.com/teamcity

RUN apt-get install -y wget

RUN wget $TEAMCITY_DOWNLOAD/$TEAMCITY_PACKAGE && \
    tar xvf $TEAMCITY_PACKAGE -C /opt && \
    rm -rf $TEAMCITY_PACKAGE

EXPOSE 8111
VOLUME ["/data/teamcity"]
CMD ["/opt/TeamCity/bin/teamcity-server.sh", "run"]
