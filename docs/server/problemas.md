# Puerto local del servidor Zabbix

El servidor Zabbix usa normalmente el puerto 10050/10051 por defecto para comunicarse con los agentes, en caso de problemas una de las pruebas más básicas es comprobar que el puerto esta abierto y accesible desde la red, a menudo las IPTABLES de Linux o el FW de MS Win lo bloquean.

Para detectar los puertos TCP abiertos ejecutamos `nestat` en el servidor (conexión SSH), entre los resultados debería figurar el puerto 10051:

```
$ netstat -vatn	
```

Otra prueba un poco más intrusiva es conectarnos directamente al puerto usando Telnet, la conexión se interrumpe pero se observa que por un momento se ha abierto, si lo hacemos desde el propio servidor (lo bonito es hacerlo desde otra máquina para descartar también problemas de red):

```
$ telnet 127.0.0.1 10050
```

# Demonio Zabbix

Logicamente para que el servidor funcione debe estar el demonio o servicio arrancado. El script de arranque del servicio se encuentra en la siguiente ruta: `/etc/init.d/zabbix-server`.

El script `zabbix-server` acepta parámetros como `[start|stop|refresh]` para controlar el demonio.

El siguiente comando obtiene información del estado del servicio, por ejemplo su estado y desde cuando lleva arrancado:

```
$ service zabbix-server status
```




