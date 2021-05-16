FROM sotax/rhel7.3

MAINTAINER Igor Brilhante <igorjosebrilhante@gmail.com>

LABEL description="A custom Apache image"

ADD training.repo /etc/yum.repos.d/training.repo

RUN yum install -y httpd && \
    yum clean all

RUN echo "Hello from Dockerfile" > /usr/share/httpd/noindex/index.html

EXPOSE 80

ENTRYPOINT ["httpd", "-D", "FOREGROUND"]
