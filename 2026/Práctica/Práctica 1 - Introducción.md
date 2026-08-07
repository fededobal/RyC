# **Práctica 1 \- Introducción**

**1\. ¿Qué es una red? ¿Cuál es el principal objetivo para construir una red?**  
Desde el punto de vista sistémico una red es un grupo de computadoras/dispositivos interconectados por algún medio, por ejemplo: cableado físico. Los dispositivos pueden comunicarse entre sí para compartir recursos: dispositivos, información, servicios. El conjunto computadoras, software de red, medios y dispositivos de interconexión forma un sistema de comunicación. Ejemplos: red de la sala de PCs, red Universitaria, Internet.

**2\. ¿Qué es Internet? Describa los principales componentes que permiten su**  
**funcionamiento.**  
El Internet es una red de redes de computadoras, descentralizada, pública, que ejecutan el conjunto abierto de protocolos (suite) TCP/IP.  
\-  Routers: dirigen los paquetes de datos entre redes.   
\-  Servidores: almacenan y procesan información.   
\-  Proveedores de Servicios de Internet (ISP): conectan a los usuarios con Internet.   
\-  Infraestructura física: cables de fibra óptica, satélites, redes móviles, etc.   
\-  Protocolos: TCP/IP, HTTP, DNS, etc., que permiten la comunicación entre   
dispositivos.

**3\. ¿Qué son las RFCs?**  
Son los documentos asociados a los estándares de Internet definidos por la IETF (Internet Engineering Task Force). RFC significa Request for Comments (Solicitud de Comentarios) y son documentos técnicos fundamentales que definen los estándares, protocolos (como HTTP, TCP/IP), y procedimientos de Internet.

**4\. ¿Qué es un protocolo?**  
Un protocolo es el conjunto de conductas y normas a conocer, respetar y cumplir no sólo en el medio oficial ya establecido, sino también en el medio social, laboral, etc. El mismo define el formato, el orden de los mensajes intercambiados y las acciones que se llevan a cabo en la transmisión y/o recepción de un mensaje u otro evento.

**5\. ¿Por qué dos máquinas con distintos sistemas operativos pueden formar parte de una misma red?**  
Dos máquinas con distintos sistemas operativos pueden formar parte de una misma red porque utilizan protocolos de comunicación estándar como TCP/IP que permiten la interoperabilidad independientemente del sistema operativo.

**6\. ¿Cuáles son las 2 categorías en las que pueden clasificarse a los sistemas finales o End Systems? Dé un ejemplo del rol de cada uno en alguna aplicación distribuida que corra sobre Internet.**  
Clientes y Servidores. Los clientes son los dispositivos de los usuarios finales. Su función principal es establecer el primer contacto con el Servidor.  
En cambio, los Servidores son equipos informáticos diseñados para alojar información y proveer servicios. Su función principal es esperar pasivamente las solicitudes de los clientes para procesarlas y enviarles una respuesta.

Ejemplo: servicio de streaming que ofrece YouTube. El cliente (por ej. un teléfono móvil) inicia una conexión con un servidor y solicita reproducir X video. Los servidores, al recibir una solicitud, localizan el video requerido en sus bases de datos y comienzan a enviar (transmitir) los fragmentos de video de regreso al teléfono móvil para que se pueda visualizar en tiempo real.

**7\. ¿Cuál es la diferencia entre una red conmutada de paquetes de una red conmutada de circuitos?**  
La diferencia radica en cómo se gestionan y transmiten los datos entre los dispositivos de la red.

* Red Conmutada de Paquetes  
  - Los datos se dividen en pequeños bloques llamados paquetes antes de ser enviados a través de la red.	  
  - Cada paquete puede tomar diferentes rutas para llegar a su destino.  
  - Una vez que todos llegan, se reensamblan para reconstruir el mensaje original.  
* Red Conmutada de Circuitos  
  - Se establece un circuito dedicado entre el emisor y el receptor antes de que comience la comunicación.  
  - Este circuito queda reservado exclusivamente para esa comunicación durante toda su duración.  
  - Todos los datos viajan siempre por el mismo camino fijo.

**8\. Analice qué tipo de red es una red de telefonía y qué tipo de red es Internet.**

* Red de telefonía: Red Conmutada de Circuitos.  
  - Utilizan técnicas de multiplexación como FDM (Multiplexación por División de Frecuencia) o TDM (Multiplexación por División de Tiempo).  
  - Proveen servicios orientados a la conexión, estableciendo circuitos físicos o virtuales fijos durante toda la sesión.  
* Internet: Red Conmutada de Paquetes.  
  - Utiliza el conjunto abierto de protocolos TCP/IP.  
  - En lugar de establecer circuitos dedicados, la información se divide y se envía mediante paquetes.  
  - Se basa en servicios NO orientados a conexión, utilizando datagramas.

**9\. Describa brevemente las distintas alternativas que conoce para acceder a Internet en su hogar.**  
La fibra óptica o el cable de cobre proviene de la calle y se conecta al router doméstico. Para poder conectar un dispositivo, hay dos principales alternativas:

* En dispositivos móviles, los dos casi únicos medios son el Wi-Fi (emitido por el router) o la red móvil (4G/5G), aunque esta última no viene del router, sino de un proveedor de datos móviles.  
* Por otro lado, casi todas las computadoras tienen un puerto Ethernet. Algunas también soportan Wi-Fi y datos, al igual que los dispositivos móviles.

**10\. ¿Qué ventajas tiene una implementación basada en capas o niveles?**

* Reduce complejidad en componentes más pequeñas.  
* Las capas de abajo ocultan la complejidad a las de arriba: abstracción.  
* Las capas de arriba utilizan servicios de las de abajo: Interfaces, similar a APIs.  
* Los cambios en una capa no deberían afectar a las demás si la interfaz se mantiene.  
* Facilita el desarrollo, evolución de las componentes de red asegurando interoperabilidad.  
* Facilita aprendizaje, diseño y administración de las redes.

**11\. ¿Cómo se llama la PDU de cada una de las siguientes capas: Aplicación, Transporte, Red y Enlace?**

* Para las capas de aplicación: PDU de datos  
* Para las capas de transporte: PDU de segmento  
* Para las capas de red: PDU de paquete  
* Para las capas de enlace: PDU de trama

**12\. ¿Qué es la encapsulación? Si una capa realiza la encapsulación de datos, ¿qué capa del nodo receptor realizará el proceso inverso?**

* El encapsulamiento es el proceso mediante el cual cada capa de un modelo de red define y crea su propia Unidad de Datos de Protocolo (PDU, por sus siglas en inglés) al procesar la información que debe transmitirse.  
* Si una capa específica realiza la encapsulación en el nodo emisor, será esa misma capa homóloga (o capa par) la que realizará el proceso inverso en el nodo receptor.  
  - Esto se debe a que la arquitectura de estos modelos de red se basa en una comunicación par-a-par (peer-to-peer) entre los niveles.  
  - Cada capa del modelo se comunica lógicamente de forma exclusiva con la capa del otro extremo. Al recibir los datos, la capa correspondiente en el destino procesa el encabezado que añadió su par en el origen, lo retira y pasa la información restante a la capa inmediatamente superior.

**13\. Describa cuáles son las funciones de cada una de las capas del stack TCP/IP o**  
**protocolo de Internet.**

* Capa de Aplicación: Define protocolos de comunicación específicos para aplicaciones (HTTP, SMTP, FTP).   
* Capa de Transporte: Garantiza la entrega de datos y el control de flujo (TCP, UDP).   
* Capa de Red: Encaminamiento y direccionamiento de paquetes (IP, ICMP).   
* Capa de Enlace: Manejo del acceso al medio físico y transmisión de datos (Ethernet, Wi-Fi).

**14\. Compare el modelo OSI con la implementación TCP/IP.**

* Similitudes:  
  - Ambos se dividen en capas.  
  - Ambos tienen capas de aplicación, aunque incluyen servicios distintos.  
  - Ambos tienen capas de transporte similares.  
  - Ambos tienen una capa de red similar pero con distinto nombre.  
  - Se supone que la tecnología es de conmutación de paquetes (no de conmutación de circuitos).  
  - Es importante conocer ambos modelos.  
* Diferencias:  
  - TCP/IP combina las funciones de la capa de presentación y de sesión en la capa de aplicación.  
  - TCP/IP combina la capas de enlace de datos y la capa física del modelo OSI en una sola capa.  
  - TCP/IP más simple porque tiene menos capas.  
  - Los protocolos TCP/IP son los estándares en torno a los cuales se desarrolló Internet, de modo que la credibilidad del modelo TCP/IP se debe en gran parte a sus protocolos.  
  - El modelo OSI es un modelo "más" de referencia, teórico, aunque hay implementaciones.