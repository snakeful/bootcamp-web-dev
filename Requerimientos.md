# Requerimientos
Desarrollar una aplicacion que maneje proyectos **[SCRUM](https://es.wikipedia.org/wiki/Scrum_(desarrollo_de_software))**.

La aplicacion debe de poder guardar un proyecto que contenga un **Product Backlog** *(historias)*, **Sprints**, **Sprint Backlog** *(**Tareas**)*, **Estados de **Tareas****, **Origen de Tarea**.

Tambien debera llevar un registro de usuarios y el rol de usuario para los proyectos **SCRUM**.

# Definicion

El **Product Backlog** es el conjunto de historias que tendra el proyecto, las historias deben de tener las siguientes caracteristicas:

* Nombre
* Descripcion
* Prioridad
* Estado
* Arreglo de **Tareas** de Exito

La **Tarea** es la actividad especifica que se desarrolla dentro de un **Sprint**. La **Tarea** debe tener las siguientes caracteristicas:

* Nombre
* Descripcion
* Fecha
* **Tarea** Origen
* Estado
* Usuario Responsable
* Origen **Tarea**
* Puntos
* Puntos Ejecutados
* **Tarea** de Exito

El **Estado de la Tarea** se divide en 4 estados:

* **Por Hacer** *(To Do)*
  * Son todas las **Tareas** que se encuentran definidas pero no estan en ejecucion y estas pueden pasar al estado **En Progreso**.
* **En Progreso** *(In Progress)*
  * Son todas las **Tareas** que se estan ejecuntado despues del SCRUM diario, y estas pueden pasar a estado **Por Hacer**, **Pruebas** o **Treminado**.
* **Pruebas** *(Testing)*
  * Son las **Tareas** que se estan probando, estas solo pueden pasar a solo a estado **Terminado**.
* **Terminado** *(Done)*
  * Son las **Tareas** que se terminaron, estas **Tareas** ya no pueden pasar a otro estado.

La **Tarea** origen es la **Tarea** que origino la nueva **Tarea**, esto pasa cuando una **Tarea** es necesario redefinirla por alguna razon o circunstancia en el proyecto.

El origen de la **Tarea** se puede clasificar de las siguiente manera:

* **Nueva**
  * Clasificacion cuando se crea una nueva **Tarea** nates de empezar el Sprint.
* **Mal Definida**
  * Clasificacion cuando no se definio correctamente la **Tarea** y necesita dividirse en **Tareas** mas especificas.
* **Cambio Proceso**
  * Clasificacion cuando cambiaron los requeriemintos del proyecto y la **Tarea** debe dividirse o convertirse en otra **Tarea** mas especifica.
* **Nuevo Requerimiento**
  * Clasificacion cuando es necesario generar una nueva **Tarea** debido a **Tareas** no especificadas antes del inicio del **Sprint**.

El **Sprint** es la actividad en un intervalo de tiempo donde se hace el ejecuta un proyecto, desglosando las historias en **Tareas** especificas a ejecutar. El **Sprint** debe de tener las siguientes caracteristicas:

* Fecha Inicio **Sprint**
* Fecha Final **Sprint**
* Historias asociadas
  * **Tareas** especificas por historia
* Lista de **SCRUM** diario
  * Fecha
  * Hora Inicio
  * Hora Fin
  * Observaciones

Roles

Los roles para los proyectos **SCRUM** son los siguientes:

* Product Owner
* Scrum Master
* Scrum team

Existen otros roles que son actores auxiliares en un proyecto **SCRUM** y son los siguientes:

* Skateholders
* Administradores

# Funcionalidades

Las funcionalidad del proyecto se describe a continuacion:

## Creacion de proyectos **SCRUM**
* [CRUD](https://es.wikipedia.org/wiki/CRUD) de proyectos **SCRUM**
## Restricciones