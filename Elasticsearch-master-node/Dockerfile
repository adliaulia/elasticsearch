FROM elasticsearch:8.12.0
ENV REGION ap-southeast-1
ADD elasticsearch.yml /usr/share/elasticsearch/config/
USER root
RUN chown 1000:0 config/elasticsearch.yml
RUN bin/elasticsearch-plugin install -b discovery-ec2 && bin/elasticsearch-plugin install -b repository-s3
USER elasticsearch