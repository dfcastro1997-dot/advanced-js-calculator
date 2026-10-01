# advanced-js-calculator

Calculadora científica avanzada construida con HTML, Tailwind CSS y Math.js.

Este proyecto es una aplicación web de una sola página (SPA) que replica el comportamiento de una calculadora científica moderna. Está diseñada con un enfoque en la limpieza del código, la mantenibilidad (utilizando programación orientada a objetos en JavaScript) y la seguridad en la evaluación de expresiones matemáticas.

## Tabla de Contenidos

- [Demostración](#demostración)
- [Capturas de Pantalla](#capturas-de-pantalla)
- [Características Principales](#características-principales)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Arquitectura y Decisiones Técnicas](#arquitectura-y-decisiones-técnicas)
- [Instalación y Uso Local](#instalación-y-uso-local)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Contribución](#contribución)
- [Licencia](#licencia)
- [Contacto](#contacto)

## Demostración

Puedes probar la calculadora directamente desde el navegador, ya que está desplegada a través de GitHub Pages:

[Enlace a la calculadora en vivo] (Reemplaza este texto con el enlace real de tu GitHub Pages, ej: https://tu-usuario.github.io/advanced-js-calculator)

## Capturas de Pantalla

A continuación, se muestra la interfaz de usuario en sus diferentes configuraciones.

[Para agregar tus imágenes: Toma capturas de tu pantalla, guárdalas en una carpeta llamada "assets" o "images" en tu repositorio, y reemplaza las rutas de abajo]

**Vista de Escritorio (Modo Oscuro):**
![Vista de Escritorio - Modo Oscuro](https://i.ibb.co/S8MrzV4/image.png)

**Vista de Escritorio (Modo Claro):**
![Vista de Escritorio - Modo Claro](https://i.ibb.co/0pjWN5xq/image.png)

## Características Principales

La aplicación va más allá de las operaciones aritméticas básicas, integrando funcionalidades de nivel científico y mejoras en la experiencia de usuario (UX):

*   **Operaciones Aritméticas Básicas:** Suma, resta, multiplicación, división y porcentajes.
*   **Funciones Científicas:** 
    *   Trigonometría (Seno, Coseno, Tangente).
    *   Logaritmos (Logaritmo en base 10 y Logaritmo natural).
    *   Potenciación (x al cuadrado, x a la potencia de y) y Radicación (raíz cuadrada).
    *   Constantes matemáticas (Pi, Euler).
*   **Gestión de Expresiones Complejas:** Soporte para paréntesis anidados y jerarquía de operaciones.
*   **Historial de Pantalla:** Muestra la operación previa en la parte superior de la pantalla, facilitando el seguimiento del cálculo actual.
*   **Interfaz Responsiva:** Diseño fluido (Mobile-First) que se adapta perfectamente a pantallas de teléfonos inteligentes, tabletas y monitores de escritorio.
*   **Temas de Interfaz (Dark/Light Mode):** Botón integrado para alternar entre modo claro y oscuro, mejorando la accesibilidad visual.

## Tecnologías Utilizadas

*   **HTML5:** Estructuración semántica de los elementos de la interfaz.
*   **Tailwind CSS:** Framework CSS de utilidad (utilizado vía CDN) para el diseño responsivo, manejo del DOM, estados (hover/active) y el cambio rápido de temas (Dark Mode).
*   **JavaScript (ES6+):** Lógica del lado del cliente, manipulación del DOM y manejo de eventos.
*   **Math.js:** Librería de matemáticas para JavaScript. Se utiliza como motor de cálculo para interpretar y evaluar de manera segura las cadenas de texto (strings) matemáticas complejas.

## Arquitectura y Decisiones Técnicas

Este proyecto fue estructurado pensando en las mejores prácticas de la industria:

1.  **Seguridad frente a Inyecciones de Código:** 
    Se evitó estrictamente el uso de la función nativa `eval()` de JavaScript, la cual representa un riesgo de seguridad al ejecutar código arbitrario. En su lugar, se implementó la función `math.evaluate()` de la librería **Math.js**, que parsea y calcula expresiones matemáticas de forma segura y precisa.
2.  **Programación Orientada a Objetos (POO):**
    La lógica principal reside dentro de una clase `Calculator`. Esto encapsula los datos (operando anterior, operando actual, operación en curso) y los métodos (limpiar, añadir número, calcular), evitando la contaminación del ámbito global y haciendo el código altamente modular y fácil de escalar.
3.  **Manejo de Errores:**
    Implementación de bloques `try...catch` al evaluar las operaciones matemáticas para capturar errores de sintaxis (por ejemplo, paréntesis sin cerrar o divisiones incorrectas) y notificar al usuario de forma elegante en la pantalla sin romper la aplicación.

## Instalación y Uso Local

Al ser un proyecto del lado del cliente (Frontend) sin dependencias de compilación complejas, su ejecución local es sumamente sencilla.

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/TU_USUARIO/advanced-js-calculator.git](https://github.com/TU_USUARIO/advanced-js-calculator.git)
