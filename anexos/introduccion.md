# Anexo - Introducción al Diseño Orientado a Objetos

El paradigma orientado a objetos (abreviado POO), es un modelo de programación que organiza y forma al sistema como un conjunto de objetos los cuales representan entidades del mundo real o conceptos abstractos. Los objetos poseen atributos (datos o propiedades) los cuales describen su estado y como es el objeto, y métodos (funcionalidades y comportamientos) los cuales definen que cosas puede hacer el objeto.
Una de las mayores ventajas del POO es que los programas se centran en clases (tipos) y objetos (instancias), encapsulando datos y operaciones para reducir complejidad y facilitar mantenimiento y reutilización.

## Los cuatro fundamentos del POO

### 1. Abstracción
**Concepto:** identificar y representar solo las características esenciales de un objeto del mundo real en el sistema, dejando de lado los detalles innecesarios para el contexto.

**Ejemplo:**  
En el sistema, un supuesto **ProyectoAudiovisual** se abstrae como un objeto con atributos como *nombre, cliente, fechas, etapas, estado*.  
No es necesario modelar detalles irrelevantes como el color del logo del cliente, el modelo de cámara usada en la grabación o la tipografía del contrato.  
La abstracción permite enfocarse en lo que es relevante para gestionar y dar seguimiento a un proyecto, sin cargar el sistema con datos irrelevantes que no aportan al objetivo.

---

### 2. Encapsulamiento
**Concepto:** proteger los datos de un objeto controlando el acceso mediante métodos.  

**Ejemplo:**  
Una supuesta clase **Etapa** guardaría los valores `estado` y `responsable`.  
Estos valores no tendrían que poder ser modificados directamente, salvo mediante métodos como `cambiarEstado()` o `asignarResponsable()`, asegurando consistencia.

---

### 3. Herencia
**Concepto:** crear nuevas clases a partir de otras, reutilizando atributos y métodos comunes.  

**Ejemplo:**  
Una clase **Usuario** general, de la cual heredan **Productor**, **Editor**, **Asistente**, y más adelante **Cliente**.  
Cada uno puede tener atributos y permisos adicionales.

---

### 4. Polimorfismo
**Concepto:** distintas clases pueden responder de manera diferente al mismo mensaje o método.  

**Ejemplo:**  
Un supuesto método `notificar()` puede enviar un **mail** si el responsable prefiere correo, o un **mensaje de WhatsApp** si así está configurado.  
Es el mismo método, pero distinto comportamiento según el objeto.

## Requisitos iniciales del sistema

### Requisitos funcionales:

- 1. **Administración de proyectos:** creación y edición de proyectos, además de gestión de datos de los proyectos (nombre, fechas estimadas de finalización, estado, observaciones).
- 2. **Gestión de etapas:** responsable de cada etapa, fecha, estado (pendiente, en curso, finalizada) y observaciones.
- 3. **Tablero de control:** Para ver todos los proyectos y etapa en que se encuentra.
- 4. **Notificaciones automáticas:** vía mail y WhatsApp para avisar cuando se termina una etapa, cuando se asigna una nueva tarea o cuando se asigna un nuevo responsable.
- 5. **Registro estadístico:** en donde se pueda consultar la cantidad de proyectos entregados por mes, duración promedio de proyectos y etapas y que tipo de proyecto se hace más. También filtrar por cliente, por tipo de proyecto y ver cuanto demora cada etapa en promedio.
- 6. **Historial de tareas:** Registrar automáticamente que usuario completó cada tarea.

### Requisitos no funcionales:

- 1. **Accesibilidad multiplataforma:** disponible tanto en web como en celular.
- 2. **Facilidad de uso:** Interfaz simple e intuitiva de uso, con listas y filtros de proyectos y etapas.
- 3. **Disponibilidad:** Accesible las 24 horas del día desde cualquier dispositivo.
- 4. **Escalabilidad** Debe permitir agregar etapas de ser necesario, asi como agregar nuevas funcionalidades, por ejemplo, facturación.
- 5. **Guardado de datos** Todo tiene que ser guardado sin pérdida de datos.
- 6. **Rendimiento** Se tiene que poder gestionar múltiples proyectos en simultaneo sin bajar el rendimiento del sistema.