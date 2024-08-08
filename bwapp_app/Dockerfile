FROM php:8.0.30-apache-buster

RUN apt update && \
    apt install -y unzip wget && docker-php-ext-install mysqli

RUN wget -O /tmp/bwapp.zip https://sourceforge.net/projects/bwapp/files/bWAPP/bWAPPv2.2/bWAPPv2.2.zip && \
	unzip /tmp/bwapp.zip -d /var/www/html/ && \
	rm /tmp/bwapp.zip && \
    chmod 777 /var/www/html/bWAPP/passwords/ && \
	chmod 777 /var/www/html/bWAPP/images/ && \
	chmod 777 /var/www/html/bWAPP/documents/ && \
	mkdir /var/www/html/bWAPP/logs/ && \
	chmod 777 /var/www/html/bWAPP/logs/

EXPOSE 80

CMD ["apache2-foreground"]
