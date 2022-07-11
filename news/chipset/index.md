# Errores críticos de chipset abren millones de dispositivos Android a espionaje remoto

## Se han revelado tres vulnerabilidades de seguridad en los decodificadores de audio de los chips Qualcomm y MediaTek que, si no se resuelven, podrían permitir que un adversario obtenga acceso de forma remota a los medios y las conversaciones de audio desde los dispositivos móviles afectados.

### Según la compañía de ciberseguridad israelí Check Point, los problemas podrían usarse como una plataforma de lanzamiento para realizar ataques de ejecución remota de código (RCE) simplemente enviando un archivo de audio especialmente diseñado.

### El impacto de una vulnerabilidad RCE puede variar desde la ejecución de malware hasta que un atacante obtenga el control de los datos multimedia de un usuario, incluida la transmisión desde la cámara de una máquina comprometida», afirmaron los investigadores a cargo.

### Además, una aplicación de Android sin privilegios podría usar estas vulnerabilidades para escalar sus privilegios y obtener acceso a los datos de los medios y las conversaciones de los usuarios».

### Las vulnerabilidades tienen su origen en un formato de codificación de audio desarrollado originalmente y de código abierto por Apple en 2011. Llamado Apple Lossless Audio Codec (ALAC) o Apple Lossless, el formato de códec de audio se utiliza para la compresión de datos sin pérdida de música digital.

### Desde entonces, varios proveedores externos, incluidos Qualcomm y MediaTek, han incorporado la implementación del códec de audio de referencia proporcionado por Apple como base para sus propios decodificadores de audio.

### Y si bien Apple ha parchado y solucionado constantemente las fallas de seguridad en su versión patentada de ALAC, la variante de código abierto del códec no ha recibido una sola actualización desde que se subió a GitHub hace 11 años, el 27 de octubre de 2011.

### Las vulnerabilidades descubiertas por Check Point se relacionan con este código ALAC portado, dos de los cuales han sido identificados en procesadores MediaTek y uno en conjuntos de chips Qualcomm:

- CVE-2021-0674 (puntaje CVSS: 5.5, MediaTek): un caso de validación de entrada incorrecta en el decodificador ALAC que conduce a la exposición de información sin interacción del usuario.
- CVE-2021-0675 (puntaje CVSS: 7.8, MediaTek): una falla de escalada de privilegios local en el decodificador ALAC derivada de una escritura fuera de los límites..
- CVE-2021-30351 (puntaje CVSS: 9.8, Qualcomm): un acceso a la memoria fuera de límite debido a una validación incorrecta de la cantidad de cuadros que se pasan durante la reproducción de música.

### En un exploit de prueba de concepto ideado por Check Point, las vulnerabilidades permitieron «robar el flujo de la cámara del teléfono», dijo el investigador de seguridad Slava Makkaveev, a quien se le atribuye el descubrimiento de las fallas junto con Netanel Ben Simon.

### Tras la divulgación responsable, los respectivos fabricantes de conjuntos de chips cerraron las tres vulnerabilidades en diciembre de 2021.

### «Las vulnerabilidades eran fácilmente explotables», explicó Makkaveev. «Un actor de amenazas podría enviar una canción (archivo multimedia) y cuando la v´íctima la reproduce, podría haber inyectar código en el servicio de medios privilegiado. El actor de amenazas podría ver lo que el usuario del teléfono móvil ve».

