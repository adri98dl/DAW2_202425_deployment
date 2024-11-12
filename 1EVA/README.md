  # SERVIDOR WEB DE APLICACIONES

usamos el servidor web **Apache** con alguno de los empaquetados con XAMPP:
- MySQL
- PHP
- Filezilla (servidor FTP)
- Servidor de correo
- Apache Tomcat
- phpMyAdmin

### Instalación en Linux

distribución debian

---

--> instalamos el servidor y todas sus dependencias:
```sudo apt-get install apache2 apache2-utils```

--> una vez instalado, nos encontramos con dos aspectos:
- en la ruta ```/etc/apache2``` ==> se almacenarán los ficheros de configuración
- en la ruta ```/var/www/html``` ==> carpeta configurada que Apache tiene por defecto para almacenar las páginas webs del sitio principal

### Montando nuestro proyecto de prueba: ```prueba.com```

--> nos vamos a ```cd /etc/apache2/sites-available```

--> y creamos ```sudo mkdir nombre_proyecto.com```

--> creamos el archivo ```nano nombre_proyecto.com.conf```








--> para visualizar mi proyecto.. en ```nano /etc/hosts``` ==> me va a dar la dir para visualizarlo en el navegador
