FROM centos/httpd-24-centos8
USER root
RUN dnf install -y python38.x86_64
RUN pip3 install psycopg2-binary
ADD ./cgi.conf /etc/httpd/conf.d/cgi.conf
ADD ./hostDateNoDb.py /var/www/cgi-bin/hostDate.py
EXPOSE 8080
USER 1001
CMD run-httpd
