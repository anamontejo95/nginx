# Caso práctico  

Compruebo cual es mi versión de nginx  con el comando

>>nginx -v  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/Captura5.PNG)  

Los ficheros de configuración se encuentran en /etc/nginx  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/Captura6.PNG)

Para personalizar la página web por defecto tenemos que ir al fichero index.nginx-debian.html. Lo abrimos con el editor de texto y modificamos la página. Antes de comprobarlo reiniciamos el servicio. 

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/Captura7.PNG)  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/Captura8.PNG)

# Balanceo de carga desde https  

Para esta práctica necesito tres máquinas virtuales. Dos harán de servidores y una de balanceador de carga.  

## Máquina 1 (ana2061)  

En primero lugar, le añado a la máquina una tarjeta de red interna con la IP 192.168.100.10  

![a]()  

Instalo nginx y configuro la página por defecto  

![a]()  

Modifico el fichero /etc/hosts y le añado la página que he creado  

![a]()
