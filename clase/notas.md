# Registro de Trabajo en Clase - Taller 2

## Fecha de la sesión
08/08/2026 (Virtual)

## Integrantes presentes
- Jorge Steven Doncel Bejarano

## Actividades realizadas en clase

Durante la primer parte de la sesión el profesor explico los temas, en la ultima hora se desarrollaron los dos diagramas del caso base Clínica Salud Viva:

- Modelo Entidad-Relación (ERD).
- Diagrama de contexto de negocio.

Se utilizó draw.io para elaborar los diagramas.

## Decisiones de modelado

### Modelo Entidad-Relación

Se identificaron las entidades:

- Paciente.
- Cita.
- Médico.
- Especialidad.
- Factura.

Se definieron los atributos y claves primarias de cada entidad. También se modelaron las relaciones:

- Paciente agenda Cita (1:N).
- Cita es con Médico (N:1).
- Cita es de Especialidad (N:1).
- Cita genera Factura (1:1).

### Diagrama de contexto

Se identificaron como actores externos:

- Paciente.
- Médico.
- Asistente Administrativo.

Como sistemas internos de Clínica Salud Viva se modelaron:

- Sistema de Agendamiento.
- Notificador (SMS / Email).
- ERP Clínico.

La Aseguradora se modeló como sistema externo. Se etiquetaron los flujos de información relacionados con solicitud y confirmación de cita, consulta de disponibilidad, notificaciones, validación de datos y validación de cobertura.

## Archivos realizados

- `modelo-er-borrador.drawio`
- `contexto-borrador.drawio`
