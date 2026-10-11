# Ejercicio 6 - Modelo Entidad-Relación de un Sistema de Gestión de Proyectos

## Descripción

Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión de proyectos. El modelo permite administrar proyectos, empleados, fases, tareas, horas trabajadas y recursos materiales, representando las relaciones entre estos elementos.

## Entidades y atributos

### 1. Proyecto

Representa los proyectos administrados por la organización.

* **id_proyecto:** identificador del proyecto.

* **nombre:** nombre del proyecto.

* **descripcion:** detalle o alcance del proyecto.

### 2. Empleado

Representa a los trabajadores asignados a los proyectos.

* **id_empleado:** identificador del empleado.

* **nombre:** nombre del empleado.

* **apellido:** apellido del empleado.

* **puesto:** rol o cargo dentro de la empresa.

### 3. Fase

Representa las etapas o fases en las que se divide un proyecto.

* **id_fase:** identificador de la fase.

* **nombre:** nombre de la fase (ej. Planificación, Desarrollo, Pruebas).

* **id_proyecto:** identificador del proyecto al que pertenece.

### 4. Tarea

Representa las actividades o asignaciones específicas a realizar.

* **id_tarea:** identificador de la tarea.

* **descripcion:** detalle de la tarea a ejecutar.

* **estado:** estado actual de la tarea (ej. Pendiente, En proceso, Completada).

### 5. Horas trabajadas

Representa el registro del tiempo invertido por los empleados en las tareas de un proyecto.

* **id_registro:** identificador del registro de horas.

* **id_empleado:** identificador del empleado que realiza el trabajo.

* **id_tarea:** identificador de la tarea realizada.

* **cantidad_horas:** total de horas destinadas.

* **fecha:** fecha en la que se registraron las horas.

### 6. Recurso material

Representa los insumos, herramientas o materiales asignados a los proyectos.

* **id_recurso:** identificador del recurso material.

* **nombre:** nombre o tipo del recurso.

* **cantidad:** cantidad de recursos asignados o disponibles.

## Relaciones y cardinalidades

* **Proyecto – Empleado:** un proyecto puede contar con varios empleados asignados, y un empleado puede participar en diferentes proyectos ($1:N$).

* **Proyecto – Fase:** un proyecto se compone de múltiples fases o etapas ($1:N$).

* **Proyecto – Recurso material:** un proyecto utiliza o requiere diversos recursos materiales ($1:N$).

* **Empleado – Horas trabajadas:** un empleado registra progresivamente las horas dedicadas a sus labores ($1:N$).

* **Horas trabajadas – Tarea:** el registro de horas se imputa o vincula a tareas específicas ($1:N$).

## Objetivo

Diseñar una base de datos que permita organizar la gestión de proyectos, controlar el personal asignado, hacer seguimiento del avance por fases y tareas, auditar las horas trabajadas por empleado y administrar los recursos materiales requeridos.

## Herramienta utilizada

* Herramienta de modelado gráfico para la elaboración del diagrama Entidad-Relación.

## Archivo del ejercicio

* `ejercicio 6.jpg`: diagrama Entidad-Relación del sistema de gestión de proyectos.