FROM dremio/dremio-oss:20.1.0
#COPY my-mssql-20.0.0-202201050826310141-8cc7162b.jar /opt/dremio/jars/
#COPY calcite-core-1.16.0-202108042226350839-779444f.jar /opt/dremio/jars/3rdparty/
EXPOSE 9047/tcp
EXPOSE 31010/tcp
EXPOSE 45678/tcp

USER dremio
WORKDIR /opt/dremio
ENV DREMIO_HOME /opt/dremio
#ENV DREMIO_JAVA_SERVER_EXTRA_OPTS="-Dsaffron.default.charset=UTF-16LE -Dsaffron.default.nationalcharset=UTF-16LE -Dsaffron.default.collation.name=UTF-16LE$en_US"
ENV DREMIO_PID_DIR /var/run/dremio
ENV DREMIO_GC_LOGS_ENABLED="no"
ENV DREMIO_LOG_DIR="/var/log/dremio"
ENV SERVER_GC_OPTS="-XX:+PrintGCDetails -XX:+PrintGCDateStamps"
ENTRYPOINT ["bin/dremio", "start-fg"]
