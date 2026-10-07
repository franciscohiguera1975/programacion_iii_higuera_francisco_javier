# Programación III

## Autor

**Ing. Francisco Higuera**

---

## Descripción

Este repositorio contiene el material, ejemplos, ejercicios y proyectos desarrollados durante la asignatura **Programación III**.

La materia está orientada al desarrollo de aplicaciones web modernas, abordando progresivamente las tecnologías fundamentales del **Frontend** y **Backend**, desde la estructura de una página web hasta la construcción de aplicaciones utilizando arquitecturas y frameworks modernos.

Durante el curso trabajaremos con:

* HTML
* CSS
* JavaScript
* TypeScript
* NestJS
* ReactJS

---

# Contenidos

## 1. HTML

**HTML (HyperText Markup Language)** es el lenguaje utilizado para definir la **estructura y el contenido** de una página web.

Permite representar elementos como:

* Títulos
* Párrafos
* Enlaces
* Imágenes
* Formularios
* Tablas
* Listas
* Botones
* Secciones

### Ejemplo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi primera página</title>
</head>
<body>

    <h1>Programación III</h1>
    <p>Bienvenidos al curso.</p>

</body>
</html>
```

**Concepto clave:**

> HTML define **qué elementos existen y cómo está estructurado el contenido**.

---

# 2. CSS

**CSS (Cascading Style Sheets)** permite definir la **apariencia y presentación visual** de una página web.

Con CSS podemos controlar:

* Colores
* Tipografías
* Tamaños
* Espaciados
* Bordes
* Posicionamiento
* Diseño responsivo
* Animaciones
* Layouts mediante Flexbox y Grid

### Ejemplo

```css
h1 {
    color: blue;
    font-size: 32px;
}

p {
    color: #333;
}
```

**Concepto clave:**

> CSS define **cómo se ve y cómo se presenta el contenido**.

---

# 3. JavaScript

**JavaScript** es un lenguaje de programación utilizado principalmente para agregar **comportamiento e interactividad** a las aplicaciones web.

Permite trabajar con:

* Variables
* Condicionales
* Ciclos
* Funciones
* Arrays
* Objetos
* Eventos
* Manipulación del DOM
* Programación asíncrona
* Consumo de APIs

### Ejemplo

```javascript
const nombre = "Francisco";

function saludar(nombre) {
    return `Hola ${nombre}`;
}

console.log(saludar(nombre));
```

**Concepto clave:**

> JavaScript permite **programar el comportamiento y la lógica de una aplicación web**.

---

# 4. TypeScript

**TypeScript** es un lenguaje basado en JavaScript que incorpora principalmente **tipado estático** y otras características que facilitan el desarrollo de aplicaciones grandes.

Permite trabajar con:

* Tipos
* Interfaces
* Clases
* Genéricos
* Enumeraciones
* Tipos personalizados
* Programación orientada a objetos
* Mejor soporte para herramientas de desarrollo

### Ejemplo

```typescript
interface Estudiante {
    nombre: string;
    edad: number;
}

const estudiante: Estudiante = {
    nombre: "Juan",
    edad: 20
};
```

**Concepto clave:**

> TypeScript agrega **tipos y herramientas adicionales sobre JavaScript para desarrollar aplicaciones más estructuradas y mantenibles**.

---

# 5. NestJS

**NestJS** es un framework para desarrollar aplicaciones **Backend con Node.js**, utilizando principalmente TypeScript.

Está orientado a la construcción de aplicaciones escalables y utiliza conceptos como:

* Módulos
* Controladores
* Servicios
* Inyección de dependencias
* DTO
* Validaciones
* Middleware
* Guards
* Pipes
* Interceptors
* APIs REST
* Integración con bases de datos

### Ejemplo

```typescript
import { Controller, Get } from '@nestjs/common';

@Controller('estudiantes')
export class EstudiantesController {

    @Get()
    obtenerEstudiantes() {
        return [
            {
                id: 1,
                nombre: 'Juan'
            }
        ];
    }
}
```

Una petición:

```text
GET /estudiantes
```

puede ser atendida por el controlador.

**Concepto clave:**

> NestJS permite construir **APIs y aplicaciones Backend estructuradas, escalables y mantenibles utilizando TypeScript**.

---

# 6. ReactJS

**ReactJS** es una biblioteca de JavaScript utilizada para construir **interfaces de usuario** mediante componentes reutilizables.

Trabajaremos conceptos como:

* Componentes
* JSX
* Props
* State
* Hooks
* Eventos
* Formularios
* Renderizado condicional
* Listas
* Consumo de APIs
* Rutas
* Componentes reutilizables

### Ejemplo

```jsx
function Saludo() {
    const nombre = "Estudiante";

    return (
        <div>
            <h1>Hola {nombre}</h1>
            <p>Bienvenido a Programación III.</p>
        </div>
    );
}

export default Saludo;
```

**Concepto clave:**

> React permite construir **interfaces de usuario mediante componentes reutilizables y dinámicos**.

---

# Relación entre las tecnologías

Durante la asignatura veremos cómo estas tecnologías pueden integrarse para construir una aplicación completa:

```text
                    APLICACIÓN WEB
                          │
             ┌────────────┴────────────┐
             │                         │
          FRONTEND                  BACKEND
             │                         │
          ReactJS                   NestJS
             │                         │
        TypeScript                TypeScript
             │                         │
          HTML / CSS              Node.js
             │                         │
             └────────────┬────────────┘
                          │
                       API REST
                          │
                     Base de Datos
```

Una posible arquitectura de trabajo será:

```text
┌───────────────────────────────┐
│           USUARIO             │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│           ReactJS             │
│           Frontend             │
└───────────────┬───────────────┘
                │
                │ HTTP / REST
                ▼
┌───────────────────────────────┐
│           NestJS              │
│           Backend             │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│          Base de Datos        │
└───────────────────────────────┘
```

---

# Objetivo de la asignatura

Al finalizar la asignatura, el estudiante estará en capacidad de comprender y aplicar los fundamentos necesarios para desarrollar una **aplicación web Full Stack**, integrando tecnologías de Frontend y Backend.

El proceso de aprendizaje seguirá una evolución progresiva:

```text
HTML
  ↓
CSS
  ↓
JavaScript
  ↓
TypeScript
  ↓
ReactJS
  ↓
NestJS
  ↓
API REST
  ↓
Aplicación Full Stack
```

---

# Estructura del repositorio

El repositorio podrá organizarse de la siguiente manera:

```text
programacion-iii/
│
├── html/
├── css/
├── javascript/
├── typescript/
├── reactjs/
├── nestjs/
│
├── ejercicios/
├── proyectos/
│
├── .gitignore
└── README.md
```

Los ejercicios y proyectos pueden contener a su vez sus propias carpetas y subproyectos.

---

# Tecnologías

| Tecnología | Propósito                        |
| ---------- | -------------------------------- |
| HTML       | Estructura del contenido         |
| CSS        | Diseño y presentación            |
| JavaScript | Lógica e interactividad          |
| TypeScript | Tipado y desarrollo estructurado |
| ReactJS    | Desarrollo de interfaces         |
| NestJS     | Desarrollo Backend y APIs        |

---

# Metodología

Durante el desarrollo de la asignatura se combinarán:

* Conceptos teóricos.
* Ejemplos prácticos.
* Ejercicios de programación.
* Resolución de problemas.
* Desarrollo de componentes.
* Consumo de APIs.
* Desarrollo de servicios Backend.
* Integración Frontend + Backend.
* Desarrollo de proyectos.

---

## 🚀 Programación III

> **Del HTML a una aplicación Full Stack.**

Este repositorio será el espacio para experimentar, aprender, desarrollar y aplicar los conocimientos adquiridos durante la asignatura.
