# INTRODUCCION
Este repositorio lo tengo para almacenar el firmware de mi ender 3 modificada y mantener anotados los cambios realizados.

## MEJORAS FISICAS

* Fleje magnético en la cama caliente.
* Cambio de placa madre a una skr mini E3 v3.0
* Bltouch para autonivelado (Es necesario pues mi cama caliente está curvada).
* Tensor de correa en el eje X.
* Mejora a un extrusor directo trianglelab matrix lite.

## MEJORAS Y CAMBIOS EN EL FIRMWARE

* AUTONIVELADO: Se ha activado el autonivelado en el firmware (auto bed leveling bilinear), utilizando una grilla de 5x5 y usando el bltouch como endstop para el eje z.
* Z PROBE WIZARD: Se ha activado z probe wizard para así facilitar el ajuste del desface en z del bltouch.
* PID: Se ha activado la opción de pid autotune para calibrar el pid de forma automática desde la misma impresora sin necesidad de utilizar proterface.
*  AREA DE IMPRESION Y POSICIONES DE ORIGEN: Debido a la instalación del trianglelab matrix lite, la cama caliente no ha quedado centrada, para solucionar esto los valores de Y_MIN_POS y X_MIN_POS han sido cambiados a -24 y -25 respectivamente. También con se ha perdido algo del área de impresión, siendo los nuevos valores en X e Y 226 y 215 respectivamente.
* FIRMWARE RETRACTION: Se ha activado la retracción por firmware para en caso de ser necesario poder ajustar las retracciones durante una impresión en curso.
* LINEAR ADVANCE: Se ha activado el linear advance para hacer más constante el flujo de filamento durante la impresión, disminuyendo inconsistencias de impresión en velocidades altas.
* INPUT SHAPING: Se ha activado el input shaping para reducir las vibraciones durante velocidades y aceleraciones altas, mejorando la calidad y aumentado en gran medida la velocidad de impresión.
* AJUSTES PARA EL EXTRUSOR: Para que el extrusor matrix lite funcione correctamente, he puesto INVER_E0_DIR en false y el cambiado los pasos por mílimetro a 336.