# ¿Qué es Zabbix?

[Zabbix](https://www.zabbix.com/) es un software de monitorización de equipos en red, basado en **software abierto** recaba información de los sistemas controlados por un agente y muestra la información centralizada en un frontend Web en el servidor.

# Características principales

Zabbix ofrece una solución **flexible** que permite monitorizar diferentes infraestructuras y elementos presentes en una red. El estudio de los [casos de uso](https://www.zabbix.com/case_studies) y sus aplicaciones practicas que describen en la Web oficial dan una idea de su capacidad de adaptación. **Uno de los casos más comunes es evidentemente monitorizar servidores y servicios críticos** de una empresa, este caso será el más estudiado en este manual que lees.

Uno de los fuertes de Zabbix es una interface Web del servidor muy cuidada donde se presenta la información con diferentes vistas y formatos, cuadro de mando central, gráficos, mapas de red, reportes.

![](https://assets.zabbix.com/img/screenshots/3.0/monitoring/Custom_screens.png)

Para recolectar los datos necesarios en el servidor existen agentes que funcionan como clientes para diferentes sistemas operativos, **el agente se instala como servicio o demonio (se ejeucta en segundo plano), es muy liviano y consume muy pocos recursos, la configuración del agente se realiza en un fichero de texto plano lo que hace que el agente sea altamente portable**. El agente ya contempla una serie de checks o items a monitorizar como por ejemplo: interface de red, CPU, memoria, disco, sistema, logs... ([ver lista completa en la Web oficial](https://www.zabbix.com/documentation/3.0/manual/config/items/itemtypes/zabbix_agent)). Pero además de eso lo que lo hace muy flexible es que **el usuario puede definir parámetros personalizados**.

Cuando instalamos el servidor viene **precargado con plantillas (templates) para los tipos de sistemas operativos del agente más típicos**, MS Windows server, Win7, máquinas virtualizadas, etc.. Las plantillas contienen items o elementos que podemos modificar o añadir nuevos para monitorizar nuevos parámetros no contemplados.






















