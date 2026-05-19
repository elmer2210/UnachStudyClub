# UnachStudyClub

Plataforma web interactiva diseñada para la organización, gestión y localización rápida de grupos de estudio estudiantiles.

## Objetivo
El objetivo principal de **UnachStudyClub** es proporcionar a la comunidad estudiantil una herramienta digital centralizada y accesible que facilite la creación, publicación y búsqueda de grupos de estudio de forma ágil. Con esto se busca incentivar el aprendizaje colaborativo, mejorar el rendimiento académico y optimizar el tiempo de estudio de los alumnos dentro de la institución.

## Problema que resuelve
En el entorno educativo, los estudiantes suelen enfrentarse a dificultades para encontrar compañeros que cursen sus mismas asignaturas, compartan disponibilidad de horarios o tengan intereses académicos afines. Actualmente, la coordinación de estos grupos se realiza de manera dispersa mediante redes sociales o aplicaciones de mensajería instantánea, donde la información se satura, se pierde con facilidad y no llega a todo el público interesado.

**UnachStudyClub** soluciona esta fragmentación unificando en un solo espacio la oferta y demanda de grupos de estudio, permitiendo realizar filtros por materias, temas específicos y horarios, logrando una organización mucho más estructurada y eficiente.

## Público Objetivo
Este proyecto está dirigido específicamente a los **estudiantes de la institución educativa (Universidad Nacional del Chimborazo - UNACH)** de todas las facultades, carreras y semestres, que tengan el deseo de potenciar su aprendizaje, resolver dudas de forma grupal, preparar evaluaciones o compartir conocimientos con sus pares.

## Integrantes y Roles
El desarrollo y gestión del proyecto está a cargo del siguiente equipo de trabajo:

| Integrante | Rol | Responsabilidades Principales |
| :--- | :--- | :--- |
| **Anahy Cóndor** | Líder de Proyecto | Planificación estratégica, coordinación general del equipo, control de cronogramas y toma de decisiones clave. |
| **Natasha Nuñez** | Diseñador Digital | Creación de la identidad visual, diseño de la interfaz de usuario (UI), optimización de la experiencia de usuario (UX) y prototipado. |
| **Alan Rodriguez** | Documentador | Redacción del marco teórico, manuales técnicos, registro de especificaciones, requerimientos del sistema y actas del proyecto. |
| **Elmer Rivadeneira** | Administrador GitHub | Configuración del repositorio, definición de políticas de ramas (*Git Flow*), control de versiones, revisión de *Pull Requests* y resolución de conflictos de código. |

## Estructura del Repositorio
El repositorio de **UnachStudyClub** se organiza de la siguiente manera para facilitar la gestión y el acceso a los diferentes componentes del proyecto:

```text
unachstudyclub/
├── public/                 # Archivos estáticos básicos (logos, favicon)
└── src/
    ├── components/         # Componentes reutilizables globales
    │   ├── Button.jsx       # Botón genérico
    │   ├── Input.jsx        # Campos de texto y selectores
    │   └── Navbar.jsx       # Barra de navegación superior
    │
    ├── views/              # Carpetas organizadas por las 5 funciones principales
    │   ├── Search/         # 1. Búsqueda (Materia, Tema, Semestre, Horarios)
    │   │   ├── GroupCard.jsx
    │   │   └── SearchFilters.jsx
    │   │
    │   ├── Create/         # 2. Creación de grupos (Formulario, Modalidad, Límite)
    │   │   └── GroupForm.jsx
    │   │
    │   ├── Management/     # 3. Gestión interna (Chat, Calendario, Recordatorios)
    │   │   ├── GroupChat.jsx
    │   │   └── MeetingCalendar.jsx
    │   │
    │   ├── Profile/        # 4. Perfil del estudiante (Materias, Intereses, Historial)
    │   │   └── StudentDetails.jsx
    │   │
    │   └── Admin/          # 5. Panel administrativo (Moderación, Reportes, Duplicados)
    │       └── ReportTable.jsx
    │
    ├── App.jsx             # Componente raíz que conecta todas las vistas
    └── main.jsx            # Punto de entrada de la aplicación 
```
## Políticas de Ramas y Flujo de Trabajo (Git Flow)

Para mantener el orden y evitar conflictos en el código, el equipo trabajará bajo el siguiente esquema de ramas:

* **`main`**: Contiene únicamente código estable y funcional (Producción). **Nadie debe hacer commits directos aquí.**
* **`develop`**: Es la rama principal de desarrollo e integración. Todo el código nuevo se une aquí antes de pasar a `main`.

### ¿Cómo trabajar en una nueva tarea?
1. Siempre crea tu rama partiendo desde `develop`.
2. Utiliza la nomenclatura **`feature/nombre-de-la-tarea`** (ejemplo: `feature/login-estudiantes` o `feature/vista-busqueda`).
3. Si estás corrigiendo un error, utiliza **`bugfix/nombre-del-error`**.
4. Cuando termines tu tarea, sube tu rama y crea un **Pull Request (PR)** hacia la rama `develop`.
5. El **Administrador de GitHub** revisará los cambios, aprobará el PR y fusionará el código.

## Guía de Instalación y Ejecución Local

Para clonar y correr este proyecto en tu entorno de desarrollo local, sigue estos pasos:

### 1. Prerrequisitos
Asegúrate de tener instalado en tu sistema:
* [Node.js](https://nodejs.org/) (Incluye npm para la gestión de paquetes).
* [Git](https://git-scm.com/) para el control de versiones.

### 2. Clonar el repositorio
Abre tu terminal y clona el proyecto ejecutando:
```bash
git clone https://github.com/elmer2210/unachstudyclub.git
```

### 3. Instalar dependencias
Navega hasta la carpeta del proyecto e instala los paquetes necesarios:
```bash
cd unachstudyclub
npm install
```

### 4. Ejecutar el proyecto
Levanta el servidor de desarrollo local con el siguiente comando:
```bash
npm run dev
```
La aplicación estará disponible generalmente en `http://localhost:5173` o el puerto que te indique la terminal.

## Despliegue en Servidor (Producción)

Dado que la aplicación está en fase de desarrollo, estas son las instrucciones generales para su futuro paso a producción:

1. **Generar el build de producción:**
   Ejecuta el comando para compilar el proyecto y optimizar los archivos estáticos:
   ```bash
   npm run build
   ```
2. **Servidor Web:**
   El comando anterior generará una carpeta (usualmente llamada `dist/` o `build/`). El contenido de esta carpeta debe ser alojado en un servidor web estático. Puedes utilizar servicios como **Vercel, Netlify, GitHub Pages**, o servidores tradicionales configurados con **Nginx** o **Apache**.

---
*Nota: Este archivo se encuentra bajo constante actualización conforme avance el ciclo de vida del desarrollo del software.*
