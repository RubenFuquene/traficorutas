# Sistema de Base de Datos para Tráfico

## Resumen General

Este proyecto presenta el diseño e implementación de un sistema distribuido de bases de datos de alto rendimiento, orientado a una plataforma de navegación de tráfico inspirada en Waze. El sistema está concebido para ingerir y procesar grandes volúmenes de datos en tiempo real, generar sugerencias de rutas inteligentes y ofrecer información útil tanto a usuarios individuales como a conductores y administradores.

**Capacidades esperadas del sistema:**

- `137,957` segmentos viales por ciudad  
- Actualizaciones cada `2 minutos`  
- Más de `198 millones` de registros diarios por ciudad  
- Tiempos de respuesta `<140ms` para hasta `180 millones` de usuarios

---

## Características Clave

### Arquitectura de Tres Capas

- **MongoDB**: ingesta en tiempo real para almacenamiento inicial y eventos crudos.  
- **PostgreSQL**: almacenamiento histórico estructurado para consultas analíticas.  
- **Redis**: datamart de acceso rápido para consultas frecuentes y en tiempo real.

### Historias de Usuario Implementadas

- Actualizaciones de tráfico en tiempo real  
- Alternativas de ruta según congestión  
- Estimación de llegada de transporte público  
- Rutas ecológicas y analítica premium  
- Rastreo de flotas y tableros de control administrativos

### Componentes Modulares del Sistema

- Gestión de usuarios y sesiones  
- Búsqueda de rutas y navegación  
- Notificaciones y alertas  
- Integración de fuentes de datos externas  
- Transacciones y suscripciones  
- Seguridad y registro de auditoría

---

## Tecnologías Utilizadas

| Tecnología    | Rol                                                                 |
|---------------|----------------------------------------------------------------------|
| MongoDB       | Área de staging para datos sin estructurar                          |
| PostgreSQL    | Almacén de datos para consultas analíticas estructuradas            |
| Redis         | Datamart para respuestas rápidas y consultas frecuentes             |
| ETL Pipeline  | Transformación y carga desde MongoDB hacia PostgreSQL               |

---

## Autor

**Rubén Darío Fúquene Castiblanco**  
`20192020004`  
Estudiante de Ingeniería de Sistemas - Universidad Distrital Francisco José de Caldas  
Enfoque en inteligencia artificial, ciencia de datos y diseño de arquitecturas distribuidas para aplicaciones urbanas.

---
