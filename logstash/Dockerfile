FROM docker.elastic.co/logstash/logstash:7.5.0

ENV discovery.seed_hosts=logstash
ENV LS_JAVA_OPTS="-Xms512m -Xmx512m"

COPY /usr/share/logstash/pipeline ./pipeline
COPY /usr/share/logstash/templates ./templates

EXPOSE 5044

CMD [ "logstash", "-f", "/usr/share/logstash/pipeline/logstash-r1.conf" ]
