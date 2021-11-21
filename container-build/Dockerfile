# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent


EXPOSE 8080 
LABEL io.openshift.expose-services="8080:http" \
		io.openshift.tags="apache,httpd" \
		io.k8s.display-name="Apache HTTP Server" \
		io.k8s.description="A basic Apache HTTP Server child image, uses ONBUILD"
 	

RUN sed i- "s/^Listen 80/8080/' /etc/httpd/conf/httpd.conf && \
	chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R g=u /var/log/httpd /var/run/httpd



user 1001
