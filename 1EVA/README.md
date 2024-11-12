  # SERVIDOR WEB DE APLICACIONES

usamos el servidor web **Apache** con alguno de los empaquetados con XAMPP:
- MySQL
- PHP
- Filezilla (servidor FTP)
- Servidor de correo
- Apache Tomcat
- phpMyAdmin

## Instalación en Linux *[distribución Debian]*

### Instalación de servidores

- Apache2 como servidor de fronted:
```sudo apt-get install apache2 apache2-utils```

- Tomcat como servidor de backend
```sudo apt-get install tomcat9 tomcat8.```

 .

--> una vez instalado, nos encontramos con dos aspectos:
- en la ruta ```/etc/apache2``` ==> se almacenarán los ficheros de configuración
- en la ruta ```/var/www/html``` ==> carpeta configurada que Apache tiene por defecto para almacenar las páginas webs del sitio principal

### Montando nuestro proyecto de prueba: ```prueba.com```

--> nos vamos a ```cd /etc/apache2/sites-available```

--> y creamos ```sudo mkdir nombre_proyecto.com```

--> creamos el archivo ```nano nombre_proyecto.com.conf``` y le metemos:

```
<VirtualHost *:80>
	# Email de contacto del administrador
	ServerAdmin webmaster@prueba.com

	# Carpeta Raiz del host "prueba.com"
	DocumentRoot "/var/www/html/prueba.com"
	
  	# Nombre del servidor
	ServerName prueba.com
	
  	# Los distintos nombres que pueden usarse para acceder a "prueba.com"
	ServerAlias www.prueba.com
	
  	# El archivo de log de errores
	ErrorLog "${APACHE_LOG_DIR}/prueba.com-error.log"
	
  	# El archivo del log de accesos
	CustomLog "${APACHE_LOG_DIR}/prueba.com-access.log" combined
</VirtualHost>
```

--> lo levantamos ```sudo a2ensite prueba.com```







--> para visualizar mi proyecto.. en ```nano /etc/hosts``` ==> me va a dar la dir para visualizarlo en el navegador
