# ComandosLinux
Un Resumen de los comandos más utilizado en Consola Linux

Archivos .tar.gz:
Comprimir: tar -czvf empaquetado.tar.gz carpeta
Descomprimir: tar -xzvf archivo.tar.gz

Archivos .tar:
<br>Empaquetar: tar -cvf paquete.tar carpeta
<br>Desempaquetar: tar -xvf paquete.tar

Archivos .gz:
<br>Comprimir: gzip -9 index.php
<br>Descomprimir: gzip -d index.php.gz

Archivos .zip:
<br>Comprimir: zip archivo.zip carpeta
<br>Descomprimir: unzip archivo.zip


EXPORTAR BASE DE DATOS:
````
mysqldump --user=$USUARIO --password=$CLAVE $BD > $ARCHIVO.sql;
````


IMPORTAR BASE DE DATOS:
````
mysql -u $USUARIO -p $BD < $ARCHIVO.sql;
````

# Comandos para Cambiar fecha y hora Servidor
````
timedatectl set-timezone Chile/Continental
timedatectl
date -s "20 SEP 2023 12:00:00"
en php date_default_timezone_set("Chile/Continental");
````

