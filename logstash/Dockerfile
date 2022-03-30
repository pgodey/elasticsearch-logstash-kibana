FROM docker.elastic.co/logstash/logstash:7.5.0

ENV discovery.seed_hosts=logstash
ENV LS_JAVA_OPTS="-Xms512m -Xmx512m"

COPY ./pipeline /usr/share/logstash/pipeline 
COPY ./templates /usr/share/logstash/templates

EXPOSE 5044
EXPOSE 9600

CMD [ "logstash", "-f", "/usr/share/logstash/pipeline/logstash-r1.conf" ]
