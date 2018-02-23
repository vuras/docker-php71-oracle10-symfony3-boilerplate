FROM php:7.1-fpm

# Oracle instantclient
ADD basic-10.2.0.5.0-linux-x64.zip /tmp/
ADD sdk-10.2.0.5.0-linux-x64.zip /tmp/

RUN apt-get update
RUN apt-get install -y unzip
RUN unzip /tmp/basic-10.2.0.5.0-linux-x64.zip -d /usr/local/
RUN unzip /tmp/sdk-10.2.0.5.0-linux-x64.zip -d /usr/local/
RUN ln -s /usr/local/instantclient_10_2 /usr/local/instantclient
RUN ln -s /usr/local/instantclient/libclntsh.so.10.1 /usr/local/instantclient/libclntsh.so
RUN echo 'instantclient,/usr/local/instantclient' | pecl install oci8
RUN echo "extension=oci8.so" > /usr/local/etc/php/oci8.ini
RUN ln -s /usr/local/etc/php/oci8.ini /usr/local/etc/php/conf.d/oci8.ini