FROM ubuntu:latest
LABEL org.opencontainers.image.authorSurname="Kobus" \
    org.opencontainers.image.authorEmail="s97637@pollub.edu.pl"
RUN apt-get update && apt-get install -y \
    apache2 \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
COPY index.html /var/www/html/index.html
COPY apache_ports.txt /etc/apache2/ports.conf
COPY apache_default.txt /etc/apache2/sites-available/000-default.conf
EXPOSE 8080
CMD [ "apachectl", "-D", "FOREGROUND" ]