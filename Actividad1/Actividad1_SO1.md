Universidad San Carlos de Guatemala 
Facultad de Ingeniería 
Escuela de Ciencias y Sistemas
Sistemas Operativos 1 sección A
Ing. Jesús Alberto Gaznan Polanco
<br>
<br>
### <center> Actividad 1 </center>
<br>
<br>

| Nombre | Carnet |
| -- | -- |
| Henry Gabriel Peralta Martinez| 201712289 |

##
## Tipos de kernel y sus diferencias

### Kernel Monolítico
Estos sistemas tienen un núcleo grande y complejo, que engloba todos los servicios del sistema. Está programado de forma no modular, y tiene un rendimiento mayor que un micronúcleo. Sin embargo, cualquier cambio a realizar en cualquier servicio requiere la recompilación del núcleo y el reinicio del sistema para aplicar los nuevos cambios.

Un sistema operativo con núcleo monolítico concentra todas las funcionalidades posibles (planificación, sistema de archivos, redes, controladores de dispositivos, gestión de memoria, etc) dentro de un gran programa. El mismo puede tener un tamaño considerable, y deberá ser recompilado por completo al añadir una nueva funcionalidad.

Un error en una rutina puede propagarse a todo el núcleo.

### Micro kernel
El microkernel se ha diseñado intencionadamente de un tamaño pequeño para que en caso de fallo no paralice todo el sistema operativo. No obstante, para que pueda asumir las mismas funciones que un kernel grande, está dividido en varios módulos. Como ejemplo de aplicación solo existe el componente Mach de OS X, ya que hasta ahora no hay ningún sistema operativo con microkernel.

### Kernel Hibrido
Núcleo híbrido es una arquitectura basada en la combinación de microkernel y núcleo monolítico, estas arquitecturas son utilizadas dentro de las computadoras por medio de los sistemas operativos

Una característica especial con que cuenta el núcleo híbrido es que incluyen código extra con el objetivo de mejorar el rendimiento.

A diferencia de los núcleos monolíticos tradicionales, los controladores de dispositivos y las extensiones al sistema operativo se pueden cargar y descargar fácilmente como módulos, mientras el sistema continúa funcionando sin interrupciones. También, a diferencia de los núcleos monolíticos tradicionales, los controladores pueden ser prevolcados (detenidos momentáneamente por actividades más importantes) bajo ciertas condiciones. Esta habilidad fue agregada para gestionar correctamente interrupciones de hardware, y para mejorar el soporte de Multiprocesamiento Simétrico.

La Mayoría de los Sistemas Operativos modernos contienen un Núcleo Híbrido.

### Exonúcleos
Los exonúcleos, también conocidos como sistemas operativos verticalmente estructurados, representan una aproximación radicalmente nueva al diseño de sistemas operativos. La idea subyacente es permitir que el desarrollador tome todas las decisiones relativas al rendimiento del hardware. Los exonúcleos son extremadamente pequeños, ya que limitan expresamente su funcionalidad a la protección y el multiplexado de los recursos. Se llaman así porque toda la funcionalidad deja de estar residente en memoria y pasa a estar fuera, en librerías dinámicas.

## 
## User vs Kernel mode

| Criterios | Kernel mode | User Mode | 
| -- | -- | -- |
|Modo Kernel vs Modo Usuario|En modo kernel, el programa tiene acceso directo y sin restricciones a los recursos del sistema.| En modo usuario, el programa de aplicación se ejecuta y se inicia.|
|Interrupciones| En el modo Kernel, todo el sistema operativo puede dejar de funcionar si se produce una interrupción.| En el modo de usuario, un solo proceso falla si ocurre una interrupción.|
|Modos| El modo kernel también se conoce como modo maestro, modo privilegiado o modo de sistema.|  El modo de usuario también se conoce como modo sin privilegios, modo restringido o modo esclavo.| 
|Espacio de direcciones virtuales| En modo kernel, todos los procesos comparten un único espacio de direcciones virtuales.| En el modo de usuario, todos los procesos obtienen un espacio de direcciones virtuales separado.|
|Nivel de privilegio| En el modo kernel, las aplicaciones tienen más privilegios que en el modo usuario.| Mientras está en modo usuario, las aplicaciones tienen menos privilegios.|
|Restricciones| Como el modo kernel puede acceder tanto a los programas del usuario como a los programas del kernel, no hay restricciones.| Mientras que el modo de usuario necesita acceder a los programas del kernel, ya que no puede acceder a ellos directamente.|
|Valor de bit de modo| El bit de modo de kernel-mode es 0.| El bit de modo del modo de usuario es 1.|
|Referencias de memoria| Es capaz de hacer referencia a ambas áreas de memoria.| Solo puede hacer referencias a la memoria asignada para el modo de usuario.|
|Fallo del sistema| Un bloqueo del sistema en modo kernel es grave y complica las cosas.| En el modo de usuario, se puede recuperar un bloqueo del sistema simplemente reanudando la sesión.|
|Acceso| Solo la funcionalidad esencial puede operar en este modo.| Los programas de usuario pueden acceder y ejecutarse en este modo para un sistema determinado.|
|Funcionalidad| El modo kernel puede hacer referencia a cualquier bloque de memoria en el sistema y también puede dirigir la CPU para la ejecución de una instrucción, lo que lo convierte en un modo muy potente y significativo.| El modo usuario es un modo de visualización estándar y típico, lo que implica que la información no puede ejecutarse por sí sola ni hacer referencia a ningún bloque de memoria; necesita una interfaz de protocolo de aplicación (API) para lograr estas cosas.
