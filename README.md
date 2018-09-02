# call-center
Existe un call center donde hay 3 tipos de empleados: operador, supervisory director. El proceso de la atención de una llamada telefónica en primera instancia debe ser atendida por un operador, si no hay ninguno libre debe ser atendida por un supervisor, y de no haber tampoco supervisores libres debe ser atendida por un director.

Debe existir una clase Dispatcher encargada de manejar las llamadas, y debe contener el método dispatchCall para que las asigne a los empleados disponibles.
El método dispatchCall puede invocarse por varios hilos al mismo tiempo.
La clase Dispatcher debe tener la capacidad de poder procesar 10
llamadas al mismo tiempo (de modo concurrente).
Cada llamada puede durar un tiempo aleatorio entre 5 y 10 segundos.
Debe tener un test unitario donde lleguen 10 llamadas
Requisitos
Se quiere Java JDK 8 y Maven, para que el proyecto compile correctamente.

#Compilar
Se recomienda para ejecutar el proyecto.

Click derecho sobre la raiz del proyecto/Maven/Update Project
Click derecho sobre la raiz del proyecto/Run As/Maven clean
Click derecho sobre la raiz del proyecto/Run As/Maven install (En este punto ejecuta los test unitarios)

# Solución
Se implementarón hlos para soportar llamadas simultaneas, para de esta mamera cumplir co el requerimiento.

Los empleados pueden atender llamadas, que son invocaciones (En la solución enviada las llamadas se simulan mediante los test unitarios)

Para soportar más llamadas de las que los empleados pueden manejar, se implemento una cola concurrente en la cual se esperan hasta que algún empleado esté disponible.
