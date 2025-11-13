FROM ubuntu:latest

RUN apt-get update && apt-get install -y apache2

# Copy Website folder
COPY Website/ /var/www/html/

# Enable Apache directory listing
RUN a2enmod autoindex

# Set proper permissions
RUN chown -R www-data:www-data /var/www/html

EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]

