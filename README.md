# TaskFlow 
## Badges
![GitHub last commit](https://img.shields.io/github/last-commit/JairoDny/TaskFlow) \
![GitHub issues](https://img.shields.io/github/issues/JairoDny/TaskFlow) \
![GitHub stars](https://img.shields.io/github/stars/JairoDny/TaskFlow)

## Descripción
Aplicación para administrar tareas en equipo. Puedes hacer apuntes de las reuniones, he incluso programarlas en la misma aplicación de TaskFlow. Este Software tiene diversos usos y es completamente gratuita e intuitiva. 

## Tabla de Contenidos:
-[Descripción](#descripción) \
-[Funcionalidades](#funcionalidades) \
-[Badges](#badges) \
-[Instalación](#instalación) \
-[Capturas](#capturas-de-pantallas) \
-[Tecnologías](#tecnologias) \
-[Uso](#uso) \
-[Requisito](#requisitos) \
-[CheckList](#una-checklist-de-funcionalidades)
-[Arquitectura](#arquitectura)
-[Estructura](#estructura-interna-del-proyecto) \
-[Licencia](#licencia)
-[Contribuidores](#contribuidores) \

## Funcionalidades.
- Organiza tareas en equipo.
- Reúnete con tu equipo.
- Planea tus tareas.
- Acelera el trabajo en equipo.

## Una Checklist de funcionalidades.
- [x] Registrar Tareas.
- [x] Editar Tareas.
- [ ] Eliminar Taras
- [ ] Asignar tareas a usuarios.

## Tecnologias.
- Python
- JAVA
- Html

## Requisitos.
- 1 GB de espacio.
- 16 GB de RAM.
- Windows 11
- Conección a Internet.

## Instalación
1. Clonar el repositorio.
2. Configurar la base de datos.
3. Configurar las variables necesarias.
4. Ejecutar la aplicación.

## Uso
- Agenda tus tareas
- Conversa con tu equipo.
- Planea tu siguiente paso.

## Capturas de pantallas.

### Pantalla Principal
![PantallaPrincipal](img/Captura%20de%20pantalla%202026-09-15%20154520.png)

### Pantalla de registro o inicio de sesión.
![Registro](img/Captura%20de%20pantalla%202026-09-15%20154830.png)

### Pantalla principal de la funcionalidad
![Registro](img/Captura%20de%20pantalla%202026-09-15%20155100.png)

### Calendario del Software
![Registro](img/Captura%20de%20pantalla%202026-09-15%20155503.png)

## Arquitectura

La aplicación esta hecha de diversos elementos. Todos estos en conjunto permiten la funcionalidad correcta del Software presentado. A continuación se describirá un poco de este:

```mermaid
flowchart  LR
    U[Usuario] --> F[Frontend]
    F --> API[API]
    API --> AUTH[Autenticación]
    API --> DAO[DAO]
    DAO --> DB[(MySQL)]
    API --> LOG[Registro de actividad]
```

## Estructura Interna del proyecto
```java
class Tarea {
    int id;
    String titulo;
    String descripcion;
    String estado; // pendiente, en progreso, completada
    LocalDate fechaLimite;
    Usuario asignado;

    void marcarCompletada() { ... }
    void reprogramar(LocalDate nuevaFecha) { ... }
}
class Proyecto {
    int id;
    String nombre;
    List<Tarea> tareas;
    List<Usuario> miembros;

    void agregarTarea(Tarea t) { ... }
    void invitarMiembro(Usuario u) { ... }
}
```


## Licencia
El software le pertenece a Jairo Daniel Ninahuanca Yarasca

## Contribuidores
- Jairo
- Daniel
- Jose
- Miguel
