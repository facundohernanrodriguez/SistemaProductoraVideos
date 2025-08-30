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

- **RF01. Administración de proyectos:** El sistema debe permitir **crear y editar proyectos**, registrando al menos: nombre, cliente, fechas de inicio y fin estimadas, estado actual y observaciones.  

- **RF02. Gestión de etapas:** El sistema debe permitir **agregar y modificar etapas** en un proyecto, indicando responsable, estado (Pendiente, En curso, Finalizada), fechas estimadas y observaciones.

- **RF03. Tablero de control:** El sistema debe mostrar un **panel general** donde se visualice el estado de todos los proyectos y sus etapas, indicando si están en curso, finalizados o pausados y el responsable de cada etapa.
  
- **RF04. Notificaciones automáticas:** El sistema debe **enviar notificaciones automáticas** (por mail y WhatsApp) al responsable cuando:  
  - Se le asigna una nueva etapa.  
  - Cambia el estado de su etapa.  
  - Una etapa a su cargo pasa a “Finalizada”.

- **RF05. Registro estadístico:** El sistema debe permitir **consultar métricas** de proyectos y etapas, incluyendo:  
  - Cantidad de proyectos entregados por mes.  
  - Duración promedio de proyectos y etapas.  
  - Proyectos filtrados por cliente o tipo.
    
- **RF06. Historial de tareas:** El sistema debe **registrar automáticamente** qué usuario completó cada tarea y los cambios de estado de cada etapa.

### Requisitos no funcionales:

- **RNF01. Accesibilidad multiplataforma:** El sistema debe estar disponible desde **navegadores web de escritorio y móviles** (Chrome, Edge, Safari) y ser responsive en pantallas de al menos 5” de ancho.

- **RNF02. Facilidad de uso:** El sistema debe permitir que **un usuario nuevo realice su primera acción (crear proyecto o etapa)** en menos de **10 minutos de aprendizaje autónomo**, con menús y filtros accesibles.

- **RNF03. Disponibilidad:** El sistema debe estar disponible al menos el **99% del tiempo**, excluyendo mantenimientos planificados.

- **RNF04. Escalabilidad:** El sistema debe soportar la gestión de al menos **100 proyectos en simultáneo**, con posibilidad de extender a nuevas funciones como facturación sin rediseño completo.

- **RNF05. Guardado de datos:** El sistema debe guardar automáticamente cada cambio en proyectos y etapas en menos de **2 segundos**, garantizando persistencia aunque se recargue la página.

- **RNF06. Rendimiento:** El sistema debe permitir consultar y filtrar proyectos sin que el tiempo de respuesta supere **3 segundos** en escenarios con hasta **50 proyectos activos y 200 etapas**.

## Casos de uso

Desarrollo de los cinco casos de uso (modelador de casos de uso)

## Boceto inicial del diseño de clases

Incluir una imagen incrustada en el archivo y un enlace para visualizarla en linea (Diseñador de clases iniciales)