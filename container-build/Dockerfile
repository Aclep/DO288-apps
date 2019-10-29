# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
LABEL io.openshift.expose-services="8080:http"
LABEL io.k8s.descriptor="A basic Apa,uses ONBUILD" io.k8s.display-name="Apache" io.openshift.expose-services="8080:http" io.openshift.tags="apache, httpd"
RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/htppd.conf
RUN chrgrp -R 0 var/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd
USER 1001
