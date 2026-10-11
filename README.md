# Ejercicio 5 - Modelo Entidad-Relación de un Sistema de Gestión Académica

## Descripción
Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión académica. El modelo permite administrar alumnos, profesores, asignaturas, comisiones, carreras y planes de estudio, representando las relaciones entre estos elementos educativos.

## Entidades y atributos

### 1. Alumno
Representa a los estudiantes matriculados en la institución.
- **id_alumno**: identificador del alumno.
- **nombre**: nombre del alumno.
- **apellido**: apellido del alumno.
- **materias**: materias asociadas al alumno.
- **horario_cursado**: horario de cursado del alumno.

### 2. Profesor
Representa al personal docente de la institución.
- **id_profesor**: identificador del profesor.
- **nombre**: nombre del profesor.
- **apellido**: apellido del profesor.
- **materias**: materias que imparte el profesor.
- **horario_laboral**: horario laboral del profesor.

### 3. Asignaturas
Representa las materias o asignaturas que forman parte de la oferta académica.
- **id_asignatura**: identificador de la asignatura.
- **nombre**: nombre de la asignatura.
- **id_profesor**: identificador del profesor asociado.
- **id_alumno**: identificador del alumno asociado.
- **id_correlativa**: identificador de la asignatura correlativa.

### 4. Comisión
Representa las comisiones o divisiones de cursada para las clases.
- **id_comision**: identificador de la comisión.
- **nombre**: nombre de la comisión.
- **turno**: turno de cursado.

### 5. Carrera
Representa las distintas carreras que ofrece la institución.
- **id_carrera**: identificador de la carrera.
- **nombre**: nombre de la carrera.
- **establecimiento**: establecimiento o facultad donde se dicta.
- **id_asignaturas**: identificador de las asignaturas que componen la carrera.

### 6. Plan de estudio
Representa la estructura curricular y organizativa de los estudios.
- **id_planDeEstudio**: identificador del plan de estudio.
- **metodologia**: metodología de enseñanza o evaluación.
- **horarios**: distribución de horarios del plan.
- **materias**: conjunto de materias del plan.

### 7. Ciclo lectivo
Representa los periodos o ciclos académicos en los que se divide el año escolar.
- **id_ciclo**: identificador del ciclo lectivo.
- **año**: año correspondiente.
- **periodo**: periodo del año lectivo.
- **fecha**: fecha de inicio o referencia.

### 8. Correlatividad
Entidad o relación que gestiona los requisitos previos entre las asignaturas.
- **id_asignatura**: identificador de la asignatura principal.
- **id_correlativa**: identificador de la asignatura requerida.

## Relaciones y cardinalidades
- **Alumno – Comisión (Inscripción / Necesita)**: un alumno se inscribe en comisiones, y una comisión está conformada por varios alumnos (relación de muchos a muchos gestionada mediante la inscripción).
- **Alumno – Asignaturas (Aprenden)**: los alumnos cursan o aprenden diversas asignaturas.
- **Profesor – Asignaturas (Dictado)**: un profesor puede dictar varias asignaturas, y una asignatura es impartida por un profesor.
- **Asignaturas – Carrera (Contiene / Requiere)**: una carrera contiene múltiples asignaturas, estructuradas mediante planes de correlatividad.
- **Alumno – Plan de estudio (Consigue)**: permite vincular el perfil del alumno con su respectivo plan de estudio.
- **Alumno – Ciclo lectivo (Tiene)**: asocia al alumno con el ciclo lectivo en curso según una fecha determinada.

## Objetivo
Diseñar una base de datos que permita organizar la información institucional de una entidad educativa, gestionar la inscripción de alumnos a comisiones, controlar el plantel docente y las asignaturas dictadas, y estructurar los planes de estudio y sus correlatividades.

