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

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/1.1.PNG)  

Instalo nginx y configuro la página por defecto  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/1.2.PNG)  

Modifico el fichero /etc/hosts y le añado la página que he creado  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/2.PNG)

Compruebo desde el navegador 

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/2.2.PNG)
  
## Máquina 2 (ana2062)  

Para esta máquina laconfiguración es la misma que para la máquina 1. Añado la tarjeta de red de red interna con la IP 192.168.100.20  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/3.PNG)  

Instalo nginx y configuro la página por defecto  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/4.PNG)  

Modifico el fichero /etc/hosts y le añado la página que he creado   

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/5.PNG)  

Compruebo desde el navegador  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/6.PNG)
  
## Máquina 3 (balanceador de carga)  

Para esta máquina, al igual que las otras dos, le añado la tarjeta de red interna con la IP 192.168.100.30  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/8.PNG)  

Instalo nginx. Elimino el archivo de configuración por defecto y creo el nuevo archivo de configuración del balanceador de carga.  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/9.PNG)  

Edito el fichero y le añado los dos servidores  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/13.PNG)

Compruebo la sintaxis con el comando  

>> nginx -t  

Una vez que la sintaxis está correcta, modifico el fichero /etc/hosts añadiendo la IP del balanceador de carga y la página www.ana206.com  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/10.PNG)  

Reincio el servicio de nginx y compruebo desde el navegador que está balanceando la carga.  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/11.PNG)  

![a](https://github.com/anamontejo95/nginx/blob/main/imagenes/12.PNG)

