# 〰️ LA RAYA

![Version](https://img.shields.io/badge/version-2.24-blueviolet?style=flat-square)
![Tech](https://img.shields.io/badge/HTML5-JS-orange?style=flat-square)
![Style](https://img.shields.io/badge/Tailwind-CSS-38bdf8?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![AI](https://img.shields.io/badge/AI_Assistance-Google_Gemini-8E75B2?style=flat-square)

> Aplicación web de estimación y precisión para multijugador local basada en escalas subjetivas.

---

## Descripción del Proyecto

**LA RAYA** es una *Single Page Application* (SPA) ligera diseñada para gestionar partidas locales de 2 a 10 jugadores organizados en equipos. La aplicación digitaliza la mecánica de juegos de mesa basados en diales o escalas continuas, permitiendo una precisión decimal (0.0 a 10.0) y ofreciendo herramientas de gestión de partida automatizadas.

El proyecto está contenido en un único archivo HTML, facilitando su portabilidad y ejecución sin necesidad de despliegue en servidor (backend-less).

### Mecánica de Juego

El núcleo del juego se basa en la discrepancia de percepción entre dos jugadores de un mismo equipo:

1.  **Definición de Escala:** Se establece un espectro semántico (ej. 0 = "Feo" / 10 = "Guapo").
2.  **Input del Objetivo:** El sistema o el jugador activo ("Guía") determina un valor objetivo (ej. 6.5) o lo genera al azar (botón random) y ofrece una pista verbal asociada a dicho valor.
3.  **Estimación:** El compañero ("Adivino") debe posicionar el cursor en la escala basándose únicamente en la pista recibida.
4.  **Cálculo de Error:** El sistema calcula la diferencia absoluta entre el *Target* y el *Guess*, asignando una puntuación porcentual basada en la proximidad.

---

## Funcionalidades Técnicas

* **Gestión de Estado Local:** Control de turnos, rotación de equipos y puntuaciones almacenadas en variables de sesión. Soporte para hasta 5 equipos simultáneos.
* **Renderizado en Canvas:** La barra de juego y los indicadores visuales se renderizan dinámicamente utilizando la API Canvas de HTML5 para un movimiento fluido a 60fps.
* **Visualización de Datos (SVG):** Generación de gráficas vectoriales en tiempo real para mostrar el rendimiento acumulado y por ronda de cada equipo.
* **Diseño Adaptativo (Glassmorphism):** Interfaz construida con TailwindCSS, utilizando transparencias y *backdrop-filter*. Incluye detección automática de preferencias de color del sistema (Dark/Light Mode) con *toggle* manual.
* **Feedback Háptico:** Implementación de la API `navigator.vibrate` para respuesta física en dispositivos móviles al interactuar con la interfaz.

---

## Stack Tecnológico

El proyecto busca la simplicidad y el rendimiento, evitando frameworks pesados de JavaScript.

* **Estructura:** HTML5 Semántico.
* **Lógica:** Vanilla JavaScript (ES6+).
* **Estilos:** [TailwindCSS](https://tailwindcss.com/) (vía CDN).
* **Fuentes:** Inter (Google Fonts).

---

## Despliegue y Uso

Al ser un archivo estático, no requiere instalación de dependencias npm ni procesos de compilación. Puedes ejecutarlo de dos formas:

### Opción A: Online (Recomendado)
Accede directamente a la última versión desplegada sin descargar nada:
**https://rrojjo.github.io/LaRaya/**

### Opción B: Local (Offline)
1.  Clonar el repositorio o descargar el archivo `index.html`.
2.  Ejecutar en cualquier navegador web moderno (Chromium, Gecko, WebKit).

> **Nota:** Se requiere conexión a internet la primera vez (en ambas opciones) para cargar la librería de estilos (Tailwind) y las tipografías.

---

## Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Consulte el archivo `LICENSE` para más detalles.
