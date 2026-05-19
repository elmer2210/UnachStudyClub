# Guía de Estructura y Reglas del Código (Directorio `src/`)

Este directorio contiene todo el código fuente de la aplicación **UnachStudyClub**. Para mantener el proyecto ordenado y evitar conflictos entre los miembros del equipo, por favor sigue esta guía sobre qué va en cada carpeta y cómo nombrar los archivos.

## Organización de Carpetas

### `components/`
Aquí deben ir todos los componentes visuales que son genéricos y se van a **reutilizar** en diferentes partes de la aplicación (por ejemplo: botones universales, barras de navegación, modales, campos de texto).

### `views/`
Esta carpeta contiene las pantallas principales de la aplicación, separadas por sus 5 funciones principales. **Nadie debe trabajar en la carpeta de otro compañero si no le corresponde.**
* **`Admin/`**: Vistas y componentes del panel administrativo (moderación, control de duplicados, sistema de reportes).
* **`Create/`**: Vistas para la creación de grupos de estudio (formulario, selectores de modalidad, límites de integrantes).
* **`Management/`**: Vistas para la gestión interna de un grupo ya creado (chat interno, calendario de reuniones, recordatorios).
* **`Profile/`**: Vistas del perfil del estudiante (materias inscritas, historial de grupos, intereses).
* **`Search/`**: Vistas para la búsqueda de grupos (filtros por materia/horario, tarjetas de resultados).

---

## Nomenclatura de Archivos (Cómo nombrar las cosas)

Para que todo el código sea uniforme, respetaremos las siguientes reglas al crear nuevos archivos:

1. **Componentes y Vistas de React (`.jsx`)**
   * **Regla:** Usar **PascalCase** (La primera letra de cada palabra siempre en mayúscula, sin espacios ni guiones).
   * **Ejemplos:** `Button.jsx`, `GroupCard.jsx`, `SearchFilters.jsx`, `AdminDashboard.jsx`.

2. **Archivos de Estilos (`.css`)**
   * **Regla:** Usar minúsculas. Si son varias palabras, separarlas con un guion medio (**kebab-case**).
   * **Ejemplos:** `global.css`, `search-styles.css`, `profile.css`.

3. **Imágenes y Logos (Ubicados en la carpeta `public/`)**
   * **Regla:** Usar minúsculas y separar con guion medio (**kebab-case**).
   * **Ejemplos:** `logo-unach.png`, `icono-chat.svg`, `fondo-login.jpg`.

---
*Nota para el equipo: Antes de crear un nuevo componente, revisa la carpeta `components/` para asegurarte de que alguien más no haya creado uno que te pueda servir.*