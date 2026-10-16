README



Este documento se actualizará progresivamente conforme surjan nuevas observaciones, recomendaciones o aclaraciones relacionadas con el HomeLab y las prácticas desarrolladas.



***1. Uso de la documentación y validación de comandos***

Parte de la documentación de los módulos ha sido generada con herramientas de inteligencia artificial. Debido a esto, es posible que algunos bloques de texto contengan errores o inconsistencias menores.

En caso de encontrar diferencias entre los comandos mostrados en las capturas de pantalla y los incluidos en los bloques de texto, se debe dar prioridad a los comandos visibles en las imágenes, ya que representan la ejecución real de la práctica.



***2. Áreas y módulos trabajados en el laboratorio***

Dentro de este entorno de laboratorio se desarrollarán prácticas correspondientes a las siguientes asignaturas y módulos:


Adrián -- Sistemas Operativos III (SO3)

Adrián -- Fundamentos de Seguridad

Juan Alexander -- Seguridad de Sistemas Operativos (SSO)



***3. Consideraciones sobre el firewall***

En la mayoría de las prácticas, no será necesario habilitar reglas de firewall específicas, debido a que gran parte de los ejercicios se ejecutan dentro de una misma máquina o entorno aislado.

Sin embargo, existen escenarios donde sí será obligatorio configurar el firewall, especialmente cuando intervienen múltiples equipos o servicios de red, por ejemplo:

Samba Active Directory
Keepalived
Pacemaker
Servicios cliente-servidor entre Linux y Windows


En estos casos, la comunicación entre nodos o sistemas externos requiere permitir explícitamente determinados puertos y servicios.


Como se trata de un entorno de laboratorio, se recomienda aplicar las reglas de firewall indicadas en las prácticas siempre que aparezcan, incluso si en algunos casos el sistema pudiera funcionar sin ellas.




***4. Uso de snapshots y reutilización de máquinas virtuales***

En prácticas como:

Samba Active Directory
Ansible
Pacemaker
Keepalived


Es importante comprender que normalmente solo existirá un servidor maestro por entorno, mientras que las demás máquinas actuarán como clientes o nodos secundarios.


Por esta razón, cuando se observe la misma práctica realizada sobre diferentes distribuciones (por ejemplo Fedora y RHEL), no significa que ambas configuraciones coexistían simultáneamente. El procedimiento correcto consiste en reutilizar las máquinas cliente mediante snapshots.


Ejemplo práctico:

a. Crear un dominio en RHEL 8.
b. Vincular Windows 10 al dominio.
c. Verificar el funcionamiento.
d. Restaurar una snapshot de Windows 10 previa a la unión al dominio.
e. Apagar el servidor RHEL 8.
f. Crear el dominio nuevamente, esta vez en Fedora Server 42.
g. Vincular Windows 10 al nuevo dominio.
h. Verificar el funcionamiento.
i. Finalizar la práctica.


Este método permite reutilizar los mismos clientes sin necesidad de crear nuevas máquinas virtuales para cada escenario.

De igual forma, es recomendable siempre que después de cada práctica, guardes una snapshot, por si surje algún inconveniente poder regresar a la snapshot más cercana pero sin perder tampoco tanto progreso.




***5. Compatibilidad entre Fedora y RHEL***

En muchas prácticas, los comandos ejecutados en RHEL también serán funcionales en Fedora, debido a la similitud entre ambas distribuciones.

Por ello:

Si se observan muchas capturas de RHEL y pocas de Fedora, significa que la mayoría de los pasos son compatibles entre ambas plataformas.

Las capturas específicas de Fedora solo muestran los cambios mínimos necesarios para adaptar la práctica a dicha distribución.

Si no existe ninguna aclaración diferenciando Fedora de RHEL, se debe asumir que los comandos funcionan correctamente en ambas distribuciones.




***6. Compatibilidad entre dispositivos***

Todas las practicas desarrolladas funciona de manera tal que los archivos HTML se pueden ver tanto en la computadora como en el celular.
