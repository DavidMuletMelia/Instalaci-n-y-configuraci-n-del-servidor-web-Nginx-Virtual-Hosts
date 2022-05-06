# Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts

## - INSTALACIÓN -

### Instalamos

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/0.PNG)

- Comprobamos que se haya instalado correctamente poniendo la ip del servidor en nuestro navegador

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/1.PNG)

- Localizamos la ruta de nginx (`etc/nginx`) y localizamos los 2 directorios que vamos a usar a continuación, `sites-available` y `sites-enabled`

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/2.PNG)


- Creamos creamos los 2 hosts que vayamos a usar copiando el `default` con el comando `cp`. Una vez acabemos podemos controlar que se haya hecho correctamente con el comando `ll`

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/6.PNG)

- Una vez hecho esto, editamos con el comando `nano` los 2 diferentes hosts y el procedimiento es el siguiente: eliminamos el `default` de los `listen` de ambos hosts, cambiamos el root por el nombre de nuestro host, añadimos nuestro dominio al server_name

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/7.PNG)
![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/8.PNG)
![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/9.PNG)



- Nos dirigimos ahora a `sites-enabled` y aqui crearemos 2 enlaces simbolicos para relacionar los directorios que hemos creado en `sites-availables`. El comando usado es `ln -s ../sites-available/david.davidmulet.com` // `ln -s ../sites-available/david2.davidmulet.com`

![Image text](https://github.com/DavidMuletMelia/Instalaci-n-y-configuraci-n-del-servidor-web-Nginx-Virtual-Hosts/blob/main/practica%20maximo%202/17.PNG)


- Recargamos nginx con el comando `sudo -s reload nginx`

### HTML

- Para introducir nuestro codigo html nos dirigimos a `/var/www` y a continuación creamos los directorios correspondientes a cada web `sudo mkdir david` y `sudo mkdir david2`

- Una vez creados, nos metemos dentro de cada uno de ellos y creamos un archivo que alojara nuestro html (`sudo touch index.html`)

- Volvemos a recargar nginx (`sudo -s reload nginx`)


