# Práctica 1 - Introducción

## 1. ¿Qué es una red? ¿Cuál es el principal objetivo para construir una red?

Una red es un conjunto de dispositivos interconectados que pueden comunicarse e intercambiar información entre sí. Estos dispositivos incluyen computadoras, servidores, impresoras, smartphones, routers, switches y otros equipos de red.

El principal objetivo para construir una red es permitir el intercambio de recursos y la comunicación entre dispositivos distribuidos geográficamente. Los objetivos específicos incluyen:

- Compartir recursos (archivos, impresoras, aplicaciones, bases de datos)
- Facilitar la comunicación entre usuarios (email, mensajería, videoconferencias)
- Acceso remoto a información y servicios
- Distribución de cargas de procesamiento
- Respaldo y redundancia de datos
- Reducción de costos mediante el uso compartido de recursos

## 2. ¿Qué es Internet? Describa los principales componentes que permiten su funcionamiento.

Internet es una red global de redes interconectadas que utiliza el conjunto de protocolos TCP/IP para conectar dispositivos en todo el mundo. Es una infraestructura de comunicación que permite el intercambio de información entre millones de dispositivos.

Los principales componentes que permiten su funcionamiento son:

- **Sistemas finales (End Systems):** Dispositivos conectados a Internet como PCs, servidores, smartphones, tablets
- **Enlaces de comunicación:** Medios físicos que transportan datos (fibra óptica, cobre, radioenlaces, satélites)
- **Conmutadores de paquetes:** Routers y switches que dirigen el tráfico de datos
- **Protocolos de comunicación:** Conjunto de reglas que gobiernan el intercambio de datos (TCP/IP, HTTP, DNS, etc.)
- **Proveedores de servicios de Internet (ISP):** Organizaciones que proporcionan acceso a Internet
- **Infraestructura de nombres de dominio (DNS):** Sistema que traduce nombres de dominio a direcciones IP
- **Aplicaciones y servicios:** Software que utiliza la infraestructura de red (web, email, transferencia de archivos)

## 3. ¿Qué son las RFCs?

Las RFCs (Request for Comments) son documentos técnicos que describen métodos, comportamientos, investigaciones o innovaciones aplicables al funcionamiento de Internet y sistemas conectados a Internet.

**Características principales:**

- Son el mecanismo principal para definir estándares de Internet
- Cada RFC tiene un número único que lo identifica
- Una vez publicado, un RFC nunca se modifica; las actualizaciones se publican como nuevos RFCs
- Son desarrollados y mantenidos por el IETF (Internet Engineering Task Force)
- Cubren desde protocolos fundamentales hasta aplicaciones específicas
- Algunos ejemplos importantes: RFC 791 (IPv4), RFC 793 (TCP), RFC 2616 (HTTP/1.1)

**Tipos de RFC:**

- **Standards Track:** Especificaciones técnicas que se convierten en estándares
- **Informational:** Documentos informativos sobre temas relacionados con Internet
- **Experimental:** Especificaciones experimentales
- **Best Current Practice:** Guías de mejores prácticas

## 4. ¿Qué es un protocolo?

Un protocolo es un conjunto de reglas y estándares que definen cómo los dispositivos de red se comunican entre sí. Especifica el formato, la sincronización, la secuenciación y el control de errores en el intercambio de datos.

**Elementos que define un protocolo:**

- **Sintaxis:** Formato y estructura de los datos (encabezados, campos, longitudes)
- **Semántica:** Significado de cada campo y las acciones a realizar
- **Temporización:** Cuándo enviar datos y qué tan rápido pueden ser enviados

**Funciones principales:**

- Establecimiento de conexión
- Transferencia de datos
- Detección y corrección de errores
- Control de flujo
- Terminación de conexión

**Ejemplos de protocolos:**

- **HTTP:** Para transferencia de páginas web
- **TCP:** Para comunicación confiable
- **IP:** Para direccionamiento y enrutamiento
- **DNS:** Para resolución de nombres de dominio
- **SMTP:** Para envío de correo electrónico

Los protocolos permiten que dispositivos de diferentes fabricantes y sistemas operativos puedan comunicarse de manera efectiva.

## 5. ¿Por qué dos máquinas con distintos sistemas operativos pueden formar parte de una misma red?

Dos máquinas con distintos sistemas operativos pueden formar parte de una misma red debido a la estandarización de protocolos de comunicación y el modelo de capas de red.

**Razones principales:**

- **Estándares de protocolos universales:** Todos los sistemas operativos implementan los mismos protocolos estándar (TCP/IP, HTTP, DNS, etc.) definidos por organizaciones como IETF

- **Modelo de capas:** La arquitectura de red está organizada en capas, donde cada capa tiene funciones específicas independientes del sistema operativo subyacente

- **Abstracción de hardware:** Los protocolos de red operan a un nivel de abstracción que es independiente del sistema operativo específico

- **APIs estándar:** Los sistemas operativos proporcionan interfaces de programación estándar (como sockets BSD) que permiten a las aplicaciones comunicarse sin importar la plataforma

- **Formato común de datos:** Los protocolos definen formatos de datos estándar que son interpretados de la misma manera por todos los sistemas

**Ejemplo práctico:** Un servidor web Apache ejecutándose en Linux puede servir páginas web a navegadores ejecutándose en Windows, macOS, Android o iOS, porque todos utilizan HTTP sobre TCP/IP de manera estándar.

## 6. ¿Cuáles son las 2 categorías en las que pueden clasificarse a los sistemas finales o End Systems? Dé un ejemplo del rol de cada uno en alguna aplicación distribuida que corra sobre Internet.

Los sistemas finales se pueden clasificar en dos categorías principales:

**1. Clientes (Clients):**

- Son sistemas que inician la comunicación solicitando servicios
- Generalmente tienen direcciones IP dinámicas
- Suelen estar conectados de forma intermitente
- Típicamente no se comunican directamente entre sí

**2. Servidores (Servers):**

- Son sistemas que proporcionan servicios respondiendo a solicitudes
- Tienen direcciones IP fijas (estáticas)
- Están conectados permanentemente a la red
- Están preparados para atender múltiples clientes simultáneamente

**Ejemplo de aplicación distribuida - Navegación Web:**

**Cliente:** Navegador web (Chrome, Firefox, Safari) ejecutándose en una PC o smartphone

- **Rol:** Solicita páginas web mediante peticiones HTTP al servidor

**Servidor:** Servidor web (Apache, Nginx, IIS) ejecutándose en un centro de datos

- **Rol:** Responde a las peticiones HTTP enviando las páginas web solicitadas

**Ejemplo de aplicación distribuida - Correo electrónico:**

**Cliente:** Cliente de email (Outlook, Thunderbird, Gmail app)

- **Rol:** Envía y recibe mensajes de correo electrónico

**Servidor:** Servidor de correo (Exchange, Postfix)

- **Rol:** Almacena, reenvía y entrega mensajes de correo entre usuarios

## 7. ¿Cuál es la diferencia entre una red conmutada de paquetes de una red conmutada de circuitos?

**Red conmutada de circuitos:**

- Se establece un circuito dedicado entre origen y destino antes de la transmisión
- El ancho de banda del circuito se reserva completamente durante toda la conexión
- Los recursos están garantizados pero pueden quedar subutilizados
- Delay constante y predecible
- No hay almacenamiento intermedio de datos
- **Ejemplo:** Red telefónica tradicional (PSTN)

**Características:**

- Establecimiento de llamada necesario
- Recursos dedicados durante toda la sesión
- Facturación típicamente por tiempo de conexión
- Adecuada para tráfico de tiempo real con requisitos estrictos

**Red conmutada de paquetes:**

- Los datos se dividen en paquetes que se envían independientemente
- No se establece un circuito dedicado previo
- Los recursos se comparten dinámicamente entre múltiples comunicaciones
- Delay variable e impredecible
- Almacenamiento y reenvío en nodos intermedios
- **Ejemplo:** Internet

**Características:**

- No hay establecimiento de llamada
- Recursos compartidos estadísticamente
- Mayor eficiencia en el uso de recursos
- Tolerante a fallos y rutas alternativas
- Adecuada para tráfico de datos con ráfagas

> **Ventaja principal de paquetes:** Mayor eficiencia en el uso de recursos  
> **Ventaja principal de circuitos:** Garantías de rendimiento y delay predecible

## 8. Analice qué tipo de red es una red de telefonía y qué tipo de red es Internet.

**Red de telefonía tradicional:**

- **Tipo:** Red conmutada de circuitos
- **Funcionamiento:** Cuando se realiza una llamada telefónica, se establece un circuito físico dedicado entre el origen y el destino que permanece reservado durante toda la conversación

**Características:**

- Ancho de banda fijo y garantizado
- Delay constante y predecible
- Recursos reservados exclusivamente para esa llamada
- Calidad de servicio garantizada
- Eficiencia menor cuando no se está transmitiendo (silencios)

**Internet:**

- **Tipo:** Red conmutada de paquetes
- **Funcionamiento:** Los datos se dividen en paquetes que viajan independientemente por la red, pudiendo tomar rutas diferentes y siendo ensamblados en el destino

**Características:**

- Ancho de banda compartido dinámicamente
- Delay variable e impredecible
- Recursos utilizados estadísticamente por múltiples conexiones
- No hay garantías de calidad de servicio (best effort)
- Mayor eficiencia en el uso de recursos de red
- Tolerancia a fallos mediante rutas alternativas

**Implicaciones:**

- La telefonía tradicional prioriza la calidad y predictibilidad de la comunicación
- Internet prioriza la eficiencia y flexibilidad en el uso de recursos
- Las comunicaciones VoIP sobre Internet representan un híbrido que intenta combinar ambos enfoques

## 9. Describa brevemente las distintas alternativas que conoce para acceder a Internet en su hogar.

**Tecnologías de acceso residencial:**

**1. Banda ancha por cable (Cable Modem):**

- Utiliza la infraestructura de televisión por cable existente
- Tecnología DOCSIS
- Velocidades asimétricas (mayor bajada que subida)
- Ancho de banda compartido en el vecindario

**2. DSL (Digital Subscriber Line):**

- Utiliza líneas telefónicas de cobre existentes
- Tecnologías: ADSL, VDSL
- Acceso dedicado por usuario
- Velocidad disminuye con la distancia a la central

**3. Fibra óptica:**

- **FTTH (Fiber to the Home):** Fibra hasta el hogar
- **FTTC (Fiber to the Curb):** Fibra hasta la esquina
- Velocidades simétricas muy altas
- Mayor estabilidad y menor latencia

**4. Acceso inalámbrico:**

- Wi-Fi de largo alcance (WiMAX)
- Redes celulares (3G, 4G LTE, 5G)
- Internet satelital
- Acceso fijo inalámbrico (Fixed Wireless Access)

**5. Dial-up (Obsoleto):**

- Conexión por módem telefónico
- Velocidades muy bajas (56 Kbps máximo)
- Bloquea la línea telefónica durante el uso

**6. Tecnologías emergentes:**

- Internet satelital de baja órbita (Starlink)
- Powerline communications (PLC)
- Acceso mediante redes de cable eléctrico

## 10. ¿Qué ventajas tiene una implementación basada en capas o niveles?

La implementación basada en capas o niveles proporciona múltiples ventajas fundamentales:

**1. Modularidad:**

- Cada capa tiene una función específica y bien definida
- Facilita el desarrollo y mantenimiento del software
- Permite trabajar en cada capa de forma independiente

**2. Abstracción:**

- Cada capa oculta la complejidad de las capas inferiores
- Las capas superiores no necesitan conocer detalles de implementación de las inferiores
- Simplifica el diseño de aplicaciones y protocolos

**3. Reutilización:**

- Los servicios de una capa pueden ser utilizados por múltiples capas superiores
- Evita duplicación de funcionalidades
- Reduce el tiempo de desarrollo

**4. Mantenimiento y actualización:**

- Cambios en una capa no afectan necesariamente a las otras
- Facilita la corrección de errores y mejoras
- Permite evolución gradual del sistema

**5. Estandarización:**

- Cada capa puede tener estándares independientes
- Facilita la interoperabilidad entre diferentes fabricantes
- Permite competencia en cada nivel

**6. Flexibilidad:**

- Diferentes implementaciones de la misma capa pueden coexistir
- Permite optimizaciones específicas para diferentes entornos
- Facilita la migración tecnológica

**7. Depuración y análisis:**

- Facilita la localización de problemas
- Permite análisis independiente de cada capa
- Simplifica las pruebas y validación

**8. División del trabajo:**

- Diferentes equipos pueden especializarse en diferentes capas
- Permite desarrollo paralelo de componentes

## 11. ¿Cómo se llama la PDU de cada una de las siguientes capas: Aplicación, Transporte, Red y Enlace?

Las PDUs (Protocol Data Units) de cada capa en el modelo TCP/IP son:

**1. Capa de aplicación:**

- **PDU:** Mensaje (Message)
- Contiene los datos generados por la aplicación
- **Ejemplos:** página web HTTP, email SMTP, archivo FTP

**2. Capa de transporte:**

- **PDU:** Segmento (Segment) para TCP o Datagrama (Datagram) para UDP
- Contiene el mensaje de aplicación más el encabezado de transporte
- Incluye información de puertos, control de flujo, números de secuencia (TCP)

**3. Capa de red:**

- **PDU:** Paquete (Packet) o Datagrama IP (IP Datagram)
- Contiene el segmento/datagrama de transporte más el encabezado IP
- Incluye direcciones IP de origen y destino, información de enrutamiento

**4. Capa de enlace:**

- **PDU:** Trama (Frame)
- Contiene el paquete IP más el encabezado y trailer de enlace
- Incluye direcciones MAC, detección de errores, información de control de acceso al medio

**Resumen:**

- **Aplicación →** Mensaje
- **Transporte →** Segmento (TCP) / Datagrama (UDP)
- **Red →** Paquete / Datagrama IP
- **Enlace →** Trama

> Cada PDU contiene la PDU de la capa superior más su propia información de control (encabezados y posibles trailers).

## 12. ¿Qué es la encapsulación? Si una capa realiza la encapsulación de datos, ¿qué capa del nodo receptor realizará el proceso inverso?

**Encapsulación:**

La encapsulación es el proceso por el cual cada capa del modelo de red agrega su propia información de control (encabezado y posiblemente trailer) a los datos recibidos de la capa superior, creando una nueva unidad de datos para transmitir a la capa inferior.

**Proceso de encapsulación (Emisor):**

1. **Aplicación:** Genera el mensaje
2. **Transporte:** Agrega encabezado TCP/UDP → Segmento/Datagrama
3. **Red:** Agrega encabezado IP → Paquete
4. **Enlace:** Agrega encabezado y trailer → Trama
5. **Física:** Convierte a señales para transmisión

**Proceso inverso - desencapsulación (Receptor):**

Cada capa del nodo receptor realiza el proceso inverso de la capa correspondiente del emisor:

1. **Física:** Convierte señales a bits
2. **Enlace:** Remueve encabezado y trailer de enlace → extrae Paquete
3. **Red:** Remueve encabezado IP → extrae Segmento/Datagrama
4. **Transporte:** Remueve encabezado TCP/UDP → extrae Mensaje
5. **Aplicación:** Procesa el mensaje original

**Principio fundamental:**

La capa N del receptor desencapsula lo que encapsuló la capa N del emisor. Es decir:

- Si la capa de Transporte encapsula → la capa de Transporte del receptor desencapsula
- Si la capa de Red encapsula → la capa de Red del receptor desencapsula
- Y así sucesivamente

> Esto mantiene la simetría y permite que cada capa procese únicamente la información que le corresponde.

## 13. Describa cuáles son las funciones de cada una de las capas del stack TCP/IP o protocolo de Internet.

El stack TCP/IP se compone de cinco capas principales:

**1. Capa física:**

- Transmisión de bits individuales a través del medio físico
- Define características eléctricas, mecánicas y de temporización
- Especifica voltajes, frecuencias, conectores
- **Ejemplos:** cables de cobre, fibra óptica, ondas de radio
- No procesa información, solo transporta señales

**2. Capa de enlace (Data Link):**

- Transferencia confiable de datos entre nodos adyacentes
- Detección y corrección de errores en el enlace físico
- Control de acceso al medio (MAC) en redes compartidas
- Direccionamiento a nivel de enlace (direcciones MAC)
- **Protocolos:** Ethernet, Wi-Fi (802.11), PPP
- **Funciones:** framing, detección de errores, control de flujo local

**3. Capa de red (Network):**

- Enrutamiento de paquetes desde origen hasta destino
- Direccionamiento lógico global (direcciones IP)
- Determinación de rutas óptimas a través de múltiples redes
- Fragmentación y reensamblado de paquetes
- **Protocolos principales:** IP (IPv4/IPv6), ICMP, IGMP
- Manejo de congestión y control de tráfico

**4. Capa de transporte:**

- Comunicación confiable o no confiable entre procesos
- Multiplexado y demultiplexado usando números de puerto
- Control de flujo y detección de errores extremo a extremo
- **TCP:** servicio confiable, orientado a conexión, control de congestión
- **UDP:** servicio no confiable, sin conexión, mínima sobrecarga
- Segmentación y reensamblado de mensajes grandes

**5. Capa de aplicación:**

- Servicios de red directamente utilizables por aplicaciones
- Interfaces de programación para desarrolladores
- Protocolos específicos para diferentes servicios
- **Ejemplos:** HTTP/HTTPS (web), SMTP (email), DNS (resolución de nombres), FTP (transferencia de archivos), SSH (acceso remoto)
- Manejo de formatos de datos, compresión, cifrado a nivel de aplicación

## 14. Compare el modelo OSI con la implementación TCP/IP.

**Comparación entre modelo OSI y TCP/IP:**

**Estructura de capas:**

**Modelo OSI (7 capas):** 7. Aplicación 6. Presentación 5. Sesión 4. Transporte 3. Red 2. Enlace de datos

1. Física

**Modelo TCP/IP original (4 capas):** 4. Aplicación (combina capas 7, 6, 5 de OSI) 3. Transporte 2. Internet (Red)

1. Acceso a la red (combina Enlace + Física de OSI)

**Modelo TCP/IP moderno/didáctico (5 capas):** 5. Aplicación 4. Transporte 3. Red 2. Enlace

1. Física

**Principales diferencias:**

**1. Número de capas:**

- **OSI:** 7 capas bien diferenciadas
- **TCP/IP:** 4 capas en el modelo original (RFC 1122), 5 capas en versiones didácticas modernas

**2. Desarrollo:**

- **OSI:** Modelo teórico desarrollado por ISO antes de su implementación
- **TCP/IP:** Desarrollado junto con Internet, basado en implementación real

> **Nota sobre las capas TCP/IP:** El modelo TCP/IP original definido en RFC 1122 tiene 4 capas. En enseñanza moderna se usa frecuentemente un modelo de 5 capas. La diferencia está en si se separa "Acceso a la red" en "Enlace" y "Física". Ambas versiones son correctas según el contexto.

**3. Separación de funciones:**

- **OSI:** Separación más granular (Presentación y Sesión como capas independientes)
- **TCP/IP:** Funciones de presentación y sesión integradas en la capa de aplicación

**4. Adopción:**

- **OSI:** Principalmente usado como modelo de referencia y enseñanza
- **TCP/IP:** Implementación real dominante en Internet y redes modernas

**5. Flexibilidad:**

- **OSI:** Más rígido en la separación de funciones
- **TCP/IP:** Más flexible, permite que las aplicaciones manejen funciones de múltiples capas OSI

**6. Protocolos:**

- **OSI:** Define el modelo pero los protocolos OSI no se adoptaron ampliamente
- **TCP/IP:** Los protocolos (IP, TCP, UDP, HTTP, etc.) son los estándares de facto

**Ventajas de cada modelo:**

**OSI:**

- Mejor herramienta pedagógica
- Separación más clara de responsabilidades
- Útil para análisis y diseño teórico

**TCP/IP:**

- Implementación práctica y probada
- Simplicidad y eficiencia
- Amplia adopción mundial
- Evolución continua basada en necesidades reales
