[README.md](https://github.com/user-attachments/files/27805353/README.md)
# Internaco Mobile — Prototipo HTML

Prototipo navegable de la app móvil de Internaco, distribuidor de maquinaria de jardín (Husqvarna / Caravaggi). Construido como un único archivo HTML autocontenido que simula una pantalla de iPhone.

---

## Cómo usar

Abre https://mariacoronil.github.io/internaco/

---

## Pantallas implementadas

| Pantalla | Descripción |
|---|---|
| **Home** | Pedido activo con stepper de seguimiento, quick actions, grid de productos destacados y banners promocionales |
| **Catálogo · Categorías** | Lista de categorías con filtros de marca multi-selección (Husqvarna / Caravaggi) y contadores dinámicos |
| **Catálogo · Subcategoría** | Segundo nivel de navegación; mantiene el estado de los filtros activos |
| **Parrilla de productos** | Grid 2 columnas con sheet de filtros |
| **Ficha de producto (PDP)** | Galería swipeable, especificaciones técnicas reales (husqvarna.com), tabs Descripción / Ficha / Envío |
| **Añadir al carro** | Bottom sheet con selector de cantidad |
| **Detalle de pedido** | Bottom sheet con stepper de estado, líneas de producto e importes |
| **Mi cuenta** | Pantalla principal + 7 sub-pantallas: datos empresa, facturación, datos fiscales, acceso, contraseña, soporte |

---

## Stack

- HTML + CSS + JavaScript vanilla — sin frameworks ni dependencias externas
- Tipografía: SF Pro Text (sistema) + Hind Siliguri (Google Fonts)
- Simulación de iPhone: 375 × 812 px con shell visual
- Diseño de referencia: Figma — archivo *Internaco Mobile*

## Paleta de colores

| Token | Hex |
|---|---|
| Brand dark | `#002A3A` |
| Brand green | `#84BD00` |
| Background | `#EEF0F3` |

---

## Assets incluidos

- **Fotos de producto** — 6 cortacéspedes Husqvarna (2-3 imágenes por modelo)
- **Imágenes de categoría** — cortacéspedes, cortasetos, robots Automower, sopladores, motoazadas
- **Iconos SVG** — búsqueda, filtro, favoritos, entrega, almacén, volver, repetir, Caravaggi (normal + blanco)
- **Iconos de pago** — Visa, Mastercard

---

## Versiones

El proyecto itero desde `internaco_v1.html` hasta `internaco_v17.html`. Puntos de inflexión principales:

- **v15** — PDP con datos reales de Husqvarna + filtros de marca funcionales
- **v16** — Sección Mi cuenta completa (7 sub-pantallas)
- **v17** — Bottom sheet de detalle de pedido + correcciones al stepper de progreso

---

## Prompts que mejor funcionaron durante el desarrollo

Estos patrones de instrucción produjeron consistentemente los mejores resultados:

1. **Describir el comportamiento visible, no la implementación** — *"Solo se debe ver cómo el número de productos por categoría disminuye o aumenta a medida que se marcan"*
2. **Señalar la fuente de verdad** — *"Me posiciono sobre las pantallas de Figma. Si tienes alguna duda, pregúntamela antes de continuar"*
3. **Agrupar correcciones relacionadas en un solo mensaje** — lista de 4 bugs visuales resuelta en una sola pasada
4. **Dejar apertura para pedir recursos** — *"Si tienes algún problema con el dímelo antes de continuar"*
5. **Aportar el asset cuando el CSS no es suficiente** — proporcionar `caravaggi_blanco.svg` en vez de intentar compensar con filtros CSS

---

## Estimación de horas

Estimación basada en el volumen de rondas de trabajo por sesión (prompt → implementación → verificación):

| Bloque | Estimación |
|---|---|
| Home, estructura base, stepper, tab bar, cards de producto (v1–v14) | 4–6 h |
| PDP clickable con datos reales de Husqvarna (v15) | 2–3 h |
| Filtros de marca — multi-select, estado compartido, Caravaggi (v15) | 1–2 h |
| Mi cuenta — pantalla principal + 7 sub-pantallas (v16–v17) | 2–3 h |
| Bottom sheet de detalle de pedido (v17) | 1–1,5 h |
| Correcciones visuales — stepper, imágenes, iconos (v17) | 1–1,5 h |
| Revisión de diseños en Figma + pruebas en navegador | 1–2 h |
| **Total** | **12–19 h** |

El bloque más costoso fue la base (v1–v14), donde se estableció la arquitectura del archivo, el sistema de pantallas y el diseño inicial de cada sección. A partir de v15 cada sesión fue más eficiente al tener el patrón de trabajo ya rodado.

---

*Mayo 2026*
