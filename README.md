# Ejercicio 17 - Modelo Entidad-Relación de un Sistema de Gestión Veterinaria

## Descripción
Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión veterinaria. El modelo permite administrar tutores, mascotas, veterinarios, consultas médicas, vacunas y el registro de la aplicación de vacunas.

## Entidades y atributos

### 1. Tutor
Representa a los dueños o responsables legales de las mascotas.
- **id_tutor**: identificador único del tutor.
- **dni**: documento nacional de identidad.
- **nombre**: nombre y apellido del tutor.
- **direccion**: dirección física de residencia.
- **telefono**: número de contacto.
- **tipo mascota**: categoría o tipo de animales a su cargo.

### 2. Mascota
Representa a los animales de compañía registrados en la veterinaria.
- **id_mascota**: identificador único de la mascota.
- **nro historia clinica**: número de historia clínica asignado.
- **dni tutor**: documento del tutor responsable.
- **nombre**: nombre de la mascota.
- **especie**: especie animal (ej. canino, felino).
- **raza**: raza de la mascota.
- **sexo**: género del animal.

### 3. Veterinaria
Representa al personal médico veterinario profesional.
- **id_veterinaria**: identificador único del veterinario.
- **matricula profesional**: número de matrícula habilitante.
- **nombre**: nombre y apellido del profesional.
- **telefono**: número de contacto.
- **especialidad**: área de especialización médica.

### 4. Consulta
Representa las visitas médicas y atenciones clínicas realizadas a las mascotas.
- **id_consulta**: identificador único de la consulta.
- **nro historia clinica**: historia clínica de la mascota atendida.
- **matricula profesional**: matrícula del veterinario tratante.
- **fecha hora**: marca temporal de la consulta.
- **motivo consulta**: razón de la visita médica.
- **peso actual**: peso registrado del animal.
- **temperatura corporal**: temperatura medida durante el chequeo.
- **diagnostico**: conclusión médica o tratamiento indicado.

### 5. Vacuna
Representa las vacunas disponibles en el catálogo de inmunización.
- **id_vacuna**: identificador único de la vacuna.
- **codigo vacuna**: código identificador.
- **nombre comercial**: nombre comercial de la vacuna.
- **laboratorio**: laboratorio fabricante.
- **numero lote**: número de lote del producto.

### 6. Aplicacion vacuna
Entidad asociativa que registra la aplicación de una vacuna específica a una mascota.
- **nro historia clinica**: historia clínica de la mascota vacunada.
- **codigo vacuna**: código de la vacuna aplicada.
- **fecha aplicacion**: fecha en que se suministró la dosis.
- **fecha proximo refuerzo**: fecha estimada para la siguiente dosis.

## Relaciones y cardinalidades
- **Tutor – Mascota (Tiene / 1:N)**: un tutor puede tener a su cargo una o varias mascotas.
- **Mascota – Consulta (Va / 1:N)**: una mascota registra múltiples consultas médicas a lo largo de su vida.
- **Veterinaria – Consulta (Realiza / 1:N)**: un veterinario lleva a cabo y suscribe diversas consultas clínicas.
- **Mascota – Aplicacion vacuna (Necesita / 1:N)**: una mascota recibe distintas aplicaciones de vacunas como parte de su plan sanitario.
- **Aplicacion vacuna – Vacuna (1:1)**: vincula el registro de aplicación con los datos específicos de la vacuna suministrada.

## Objetivo
Diseñar una base de datos para una clínica veterinaria que permita administrar la información de los tutores y sus mascotas, llevar un control riguroso de las historias clínicas a través de consultas médicas, registrar al personal profesional y administrar de forma organizada el historial de vacunación y refuerzos.
