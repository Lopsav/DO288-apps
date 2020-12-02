# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 80

LABEL	io.openshift.expose-service="8080:http"\
	io.ks8.description="A description" \
	io.ks8.display-name="apache server" \
	io.openshift.expose-services="8080:http" \
	io.openshift.tags="httpd,apache, http"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001


