# 🎮 Gamer Fest ESPE 2027 - Landing Page

Este proyecto consiste en una página de aterrizaje (*landing page*) diseñada para promocionar y gestionar las inscripciones del torneo universitario de videojuegos **Gamer Fest ESPE 2027**, a realizarse en el Campus Belisario Quevedo de la Universidad de las Fuerzas Armadas ESPE (Latacunga, Ecuador).

El sitio cuenta con una interfaz moderna en modo oscuro (*dark mode*), estructura semántica en HTML5 y diseño adaptable (*responsive*) mediante Bootstrap 5.3.

---

## 📋 Características y Secciones

El sitio web está estructurado en una sola página con navegación fluida a través de las siguientes secciones:

1. **Header / Navegación (`sticky-top`):**
   * Logotipo e identidad del evento.
   * Menú horizontal para pantallas grandes (`lg` en adelante).
   * Menú desplegable para dispositivos móviles implementado de forma nativa con las etiquetas `<details>` y `<summary>` (sin depender de JavaScript).
   * Botón de llamado a la acción (CTA) directo hacia el formulario de inscripción.

2. **Hero (`#inicio`):**
   * Presentación principal del evento con información clave:
     * **Fecha:** Sábado 15 de enero de 2027.
     * **Horario:** 08:00 – 14:00.
     * **Lugar:** Campus Belisario Quevedo, ESPE.
   * Imagen destacada y botón de inscripción.

3. **Categorías de Torneos (`#categorias`):**
   * Presentación en tarjetas (*cards*) de los 4 videojuegos oficiales del torneo:
     * **Fortnite:** Individual o en equipos (Battle Royale).
     * **Clash Royale:** Individual (Estrategia en tiempo real).
     * **FIFA 22:** Individual 1 vs 1 (Simulador de fútbol).
     * **Mortal Kombat:** Individual 1 vs 1 (Peleas).

4. **Premios (`#premios`):**
   * Detalle de incentivos y condiciones para el podio:
     * 🥇 **Primer lugar:** Trofeo, medallas y kit gamer (audífonos + mouse).
     * 🥈 **Segundo lugar:** Medallas y teclado gamer.
     * 🥉 **Tercer lugar:** Medallas y certificado de participación destacada.

5. **Auspiciantes (`#auspiciantes`):**
   * Espacio dedicado a las marcas patrocinadoras del evento (Ruffles, Cubata, Coca-Cola).

6. **Ubicación (`#ubicacion`):**
   * Mapa interactivo de Google Maps integrado mediante `<iframe>` con carga diferida (`loading="lazy"`) mostrando el Campus Belisario Quevedo.
   * Enlace externo de respaldo para abrir la ubicación directamente en Google Maps.

7. **Formulario de Inscripción (`#inscripcion`):**
   * Captura de datos del participante con validaciones nativas de HTML5:
     * Nombres y apellidos (Obligatorio).
     * Correo institucional (`usuario@espe.edu.ec`).
     * Teléfono celular (Numérico, máx. 10 dígitos).
     * Nickname de jugador.
     * Selección de categoría (Obligatorio).
     * Casilla de aceptación de bases del torneo.

8. **Footer:**
   * Identidad del evento y enlaces a redes sociales (Instagram, Facebook, TikTok).

---

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Uso de etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<details>`).
* **Bootstrap 5.3:** Sistema de grillas (*Grid System*), componentes de interfaz (Cards, Buttons, Forms, Navbar) y utilidades de diseño con soporte nativo para tema oscuro (`data-bs-theme="dark"`).
* **CSS3:** Archivo externo (`css/estilos.css`) para personalizaciones adicionales.
* **Accesibilidad (a11y):** Uso de atributos `aria-label`, textos alternativos detallados (`alt`) en imágenes y asociación correcta de etiquetas `<label>` en formularios.

---

## 📂 Estructura de Archivos Requerida

Para que la página visualice correctamente todos sus estilos e imágenes, el proyecto debe mantener la siguiente jerarquía de directorios:

```text
proyecto-gamer-fest/
│
├── index.html              # Código fuente principal
│
├── css/
│   ├── bootstrap.min.css   # Hoja de estilos de Bootstrap 5.3
│   └── estilos.css         # Estilos personalizados del proyecto
│
└── img/
    ├── logo.jpg            # Logotipo del evento (150x100)
    ├── hero.jpg            # Imagen principal del torneo
    ├── juego1.jpg          # Imagen para Fortnite
    ├── juego2.jpg          # Imagen para Clash Royale
    ├── juego3.jpg          # Imagen para FIFA 22
    ├── juego4.jpg          # Imagen para Mortal Kombat
    ├── ausp-1.png          # Logo auspiciante 1 (Ruffles)
    ├── ausp-2.jpg          # Logo auspiciante 2 (Cubata)
    └── ausp-3.png          # Logo auspiciante 3 (Coca-Cola)
```

---

## 🚀 Instalación y Uso

1. Descarga o clona este repositorio en tu máquina local.
2. Asegúrate de incluir el archivo `bootstrap.min.css` dentro de la carpeta `css/` y las imágenes correspondientes dentro de `img/`.
3. Abre el archivo `index.html` directamente en cualquier navegador web moderno (Chrome, Firefox, Edge, Safari) o utiliza una extensión como *Live Server* en VS Code.

---

## 📌 Notas de Desarrollo y Mejoras Futuras

* **Alineación de Categorías en Formulario:** En la sección `#categorias` se muestran los juegos *Fortnite, Clash Royale, FIFA 22 y Mortal Kombat*, mientras que el `<select>` del formulario mantiene nombres genéricos (*Arena Estratégica, Tiro Táctico, Fútbol Virtual, Duelo de Combate*). Se recomienda actualizar las opciones del `<select>` si se desea mostrar el nombre comercial de cada juego.
* ** Textos Alternativos (`alt`) en Auspiciantes:** Las etiquetas `<img>` de los auspiciantes conservan textos alternativos de plantilla (*PixelByte Hardware, Nova Energy Drink, CloudLink Internet*) que pueden actualizarse para coincidir con *Ruffles, Cubata y Coca-Cola*.
* **Procesamiento del Formulario:** El formulario es actualmente demostrativo del lado del cliente. Para almacenar las inscripciones reales, se debe integrar un script en JavaScript o un backend.
