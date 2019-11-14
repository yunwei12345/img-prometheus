FROM centos:latest
ADD ./prometheuss /usr/local/
RUN  mkdir /prometheus-data && \
        chmod +x /usr/local/prometheus
EXPOSE     9090
WORKDIR /prometheus-data
ENTRYPOINT [ "/usr/local/prometheus" ]
CMD        [ "--config.file=/usr/local/prometheus.yml", \
             "--storage.tsdb.path=/prometheus-data", \
             "--storage.tsdb.retention=180d" ]
            


