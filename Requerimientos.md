# **Requerimientos**
Desarrollar una aplicación que maneje proyectos **[SCRUM](https://es.wikipedia.org/wiki/Scrum_(desarrollo_de_software))**.

La aplicación debe de poder guardar un proyecto que contenga un **Product Backlog** *(historias)*, **Sprints**, **Sprint Backlog** *(**Tareas**)*, **Estados** de **Tareas**, **Origen de Tarea**.

También deberá llevar un registro de usuarios y el rol de usuario para los proyectos **SCRUM**.

# **Definición**

El **Product Backlog** es el conjunto de historias que tendrá el proyecto, las historias deben de tener las siguientes características:

* Nombre
* Descripción
* Prioridad
* Estado
* Arreglo de **Tareas** de Finalización

Las **Prioridades** de las historias se definirán de 0 a 10 puntos, tomando en cuenta 0 como la prioridad más importante y 10 la menos importante.

La **Tarea** es la actividad específica que se desarrolla dentro de un **Sprint**. La **Tarea** debe tener las siguientes características:

* Nombre
* Descripción
* Fecha
* **Tarea** Origen
* Estado
* Usuario Responsable
* Origen **Tarea**
* Puntos
* Puntos Ejecutados
* **Tarea** de Finalización

Los **Estados de la Tarea** se dividen en 4:

* **Por Hacer** *(To Do)*
  * Son todas las **Tareas** que se encuentran definidas pero no están en ejecución y estas pueden pasar al estado **En Progreso**.
* **En Progreso** *(In Progress)*
  * Son todas las **Tareas** que se están ejecutando después del SCRUM diario, y estas pueden pasar a estado **Por Hacer**, **Pruebas** ó **Terminado**.
* **Pruebas** *(Testing)*
  * Son las **Tareas** que se están probando, estas solo pueden pasar a solo a estado **Terminado**.
* **Terminado** *(Done)*
  * Son las **Tareas** que se terminaron, estas **Tareas** ya no pueden pasar a otro estado.

La **Tarea** origen es la que se origino la nueva **Tarea**, esto pasa cuando la **Tarea** es necesario redefinirla por alguna razón o circunstancia en el proyecto.

El origen de la **Tarea** se puede clasificar de las siguiente manera:

* **Nueva**
  * Clasificación cuando se crea una nueva **Tarea** antes de empezar el **Sprint**.
* **Mal Definida**
  * Clasificación cuando no se definió correctamente la **Tarea** y necesita dividirse en **Tareas** mas específicas.
* **Cambio Proceso**
  * Clasificación cuando cambiaron los requerimientos del proyecto y la **Tarea** debe dividirse o convertirse en otra **Tarea** más específica.
* **Nuevo Requerimiento**
  * Clasificación cuando es necesario generar una nueva **Tarea** debido a **Tareas** no especificadas antes del inicio del **Sprint**.

El **Sprint** es la actividad que se ejecutarán las historias en un intervalo de tiempo, desglosando las historias en **Tareas** específicas a ejecutar. El **Sprint** debe de tener las siguientes características:

* Fecha Inicio **Sprint**
* Fecha Final **Sprint**
* Historias asociadas
  * **Tareas** específicas por historia
* Lista de **SCRUM** diario
  * Fecha
  * Hora Inicio
  * Hora Fin
  * Observaciones

# **Burndown Chart**
* Es una gráfica que se muestra públicamente donde se miden los puntos asociados a cada **Tarea** y cuantos han sido ejecutados durante la duración del **Sprint**.
* Ejemplo de una gráfica [Burndown Chart](https://upload.wikimedia.org/wikipedia/commons/thumb/2/23/EjemploDeDiagramaBurnDown.svg/1024px-EjemploDeDiagramaBurnDown.svg.png)

# **Roles**

Los roles para los proyectos **SCRUM** son los siguientes:

* Product Owner
* Scrum Master
* Scrum Team

Existen otros roles que son actores auxiliares en un proyecto **SCRUM** y son los siguientes:

* Skateholders
* Administradores

# **Funcionalidades**

Las funcionalidad del proyecto se describen a continuación:

## **Proyectos SCRUM**
* [CRUD](https://es.wikipedia.org/wiki/CRUD) de proyectos **SCRUM**
### **Restricciones**
* No se pueden borrar proyectos que tengan historias o usuarios asignados.

## **Historias**
* CRUD de historias por proyecto
* Las **Tareas** de Finalización es un listado de **Tareas** las cuales se generarán automáticamente al iniciar el **Sprint**, y determinarán si la historia ha sido finalizada por completo.

## **Estados de la Tarea**
* Definición de los 4 estados de tareas que se asignaran a cada tarea generada:
  * **Por Hacer** *(To Do)*
  * **En Progreso** *(In Progress)*
  * **Pruebas** *(Testing)*
  * **Terminado** *(Done)*

## **Origen de Tareas**
* CRUD de Origen de Tareas adicionales

### **Restricciones**
* No se pueden borrar los origenes de tarea ya descritos en el proyecto.

## **Sprint**
* CRUD de **Sprint** para la ejecución del proyecto.
* Inicio del **Sprint Backlog**.
  * Asociar historias que no esten asociadas a un **Sprint**.
  * Crear tareas para la ejecución de la historia.
* Dar inicio al **Sprint**.
* Las **Tareas** pueden generar nuevas **Tareas**, a este proceso se le asignarán a las nuevas **Tareas** creadas la **Tarea** con la que se creó esta nueva **Tarea** o varias **Tareas** y deberán tener un **Origen de Tarea** diferente a **Nueva** (Tomar en cuenta si la **Tarea** es una **Tarea** de Finalización, estas tambien hay que asignarles que son **Tareas** de Finalización).
* Para determinar que un **Sprint** ha sido terminado, todas las **Tareas** de Finalización deben estar completadas.
* Las **Tareas** de Finalización deben ser las últimas en pasar a estado **Terminado**.

### **Restricciones**
* Después de iniciado el **Sprint**, todas las nuevas tareas que no se hayan definido se crearán con el **Origen de Tarea** *Nuevo Requerimiento*.
* Debe haber al menos una **Tarea** de Finalización que no este en estado **Terminado** para poder actualizar todas las **Tareas** a **Terminado** que no sea de finalización.

## **Burndown Chart**
* Se debe mostrar una gráfica ó diagrama donde se muestre los puntos ejecutados contra los puntos ejecutados por día de todo el **Sprint** y por Scrum Team.