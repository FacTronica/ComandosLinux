# Comandos GnuLinux
Un Resumen de comandos básicos Consola GnuLinux  

## CREAR Y BORRAR USUARIO
````
useradd juanperez
userdel juanperez
````
## Espacio utilizado por cada carpeta
````
du -sm * > listado.txt
````

## Borrar archivos recursivamente filtrando con comodin
````
cd /var/www/html/public_html/
find . -name *.txt -delete
````

## Comprimir y Descomprimir Archivos .tar.gz:
````
tar -czvf empaquetado.tar.gz carpeta
tar -xzvf archivo.tar.gz
````

## PERMISOS => MYSQL
````
mariadb -u root -p
CREATE USER 'usuario'@'localhost' IDENTIFIED BY 'suclave';
GRANT ALL PRIVILEGES ON *.* to 'usuario'@'localhost';
FLUSH PRIVILEGES;
quit;
````

## EXPORTAR E IMPORTAR BASE DE DATOS:
````
mysqldump --user=$USUARIO --password=$CLAVE $BD > $ARCHIVO.sql;
mysql -u $USUARIO -p $BD < $ARCHIVO.sql;
````

### EJECUTAR COMANDOS SQL DESATENDIDO DESDE CONSOLA
````
mysql --host=localhost --user=usuariobd --password=clavebd -e "create database basedatos";
mysql --host=localhost --user=usuariobd --password=clavebd -e "truncate table basedatos.tbl_tabla";
````

## DIVIDIR ARCHIVOS DE TEXTO
````
split -d -b 10m direccion_formateada.csv direcciones_
````

## Comandos para Cambiar fecha y hora Servidor
````
timedatectl set-timezone Chile/Continental
timedatectl
date -s "20 SEP 2023 12:00:00"
en php date_default_timezone_set("Chile/Continental");
````

## Ver logs de Apache2 Vsftp
````
tail -f /var/log/apache2/access.log
tail -f /var/log/apache2/error.log
tail -f /var/log/apache2/other_vhosts_access.log
````

## Ver logs de Vsftp
````
tail -f /var/log/apache2/other_vhosts_access.log
tail -

## Ver logs de Cron
````
journalctl
````
