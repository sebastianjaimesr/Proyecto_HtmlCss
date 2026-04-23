# Proyecto_HtmlCss
# 🚀 UberX × SpaceX — Space Rides

> Prototipo de app móvil para reserva de viajes espaciales. HTML5 + CSS3 puro, sin dependencias ni JavaScript externo (salvo interacciones mínimas con JS inline).

---

## 📋 Descripción

**UberX × SpaceX** es un concepto de interfaz futurista de transporte espacial ambientado en el año 2053. Simula el flujo completo de una app de ride-hailing llevada al espacio: desde la pantalla de bienvenida hasta el recibo de pago, pasando por la selección de nave, reserva y método de pago.

El proyecto está orientado a demostrar técnicas avanzadas de maquetación CSS3: animaciones CSS-only, glassmorphism, bottom sheets expandibles, cartas de pago con BEM, y componentes de UI inmersivos sin frameworks.

---

## 🗂️ Estructura del proyecto

```
UberX-SpaceX/
├── index.html                  # Splash / pantalla de entrada
├── css/
│   └── app.css                 # Hoja de estilos global (tokens, componentes, animaciones)
└── screens/
    ├── splash.html             # Pantalla de carga animada
    ├── home.html               # Dashboard principal
    ├── travel.html             # Mapa espacial + selector de nave
    ├── booking.html            # Resumen de reserva y add-ons
    ├── payment-methods.html    # Gestión de métodos de pago
    └── receipt.html            # Recibo de transacción
```

---

## 🔀 Flujo de navegación

```
index.html
    └── home.html
            ├── travel.html
            │       └── booking.html
            │               └── payment-methods.html
            │                           └── receipt.html
            └── booking.html (acceso directo)
```

---

## 🖥️ Pantallas

| Pantalla | Archivo | Descripción |
|---|---|---|
| **Splash** | `index.html` | Animación orbital CSS-only, planetas SVG decorativos, barra de carga |
| **Loading** | `splash.html` | Pantalla de inicialización con redirect automático |
| **Home** | `home.html` | Avatar, buscador, accesos rápidos y lista de destinos |
| **Travel** | `travel.html` | Mapa espacial con planetas reales, selector de nave con radio CSS, bottom sheet expandible, swipe-to-confirm |
| **Booking** | `booking.html` | Resumen del viaje, datos del pasajero y selección de add-ons |
| **Payments** | `payment-methods.html` | Lista de tarjetas con buscador, badge Default, acciones CRUD |
| **Receipt** | `receipt.html` | Glassmorphism, desglose de vuelo, footer de acciones |

---

## ✨ Técnicas destacadas

- **Animaciones CSS-only** — Orbital SVG animado (`stroke-dashoffset`), float, fadeIn, shimmer de carga
- **Bottom sheet expandible** — Implementado solo con `<input type="checkbox">` y selectores CSS `:checked`
- **Selector de nave tipo radio** — `<input type="radio">` + etiquetas CSS, sin JS
- **Swipe to confirm** — `<input type="range">` con JS inline mínimo para feedback visual y navegación
- **Glassmorphism** — Fondos con `backdrop-filter: blur()` y bordes semitransparentes
- **Metodología BEM** — Nomenclatura consistente en todos los componentes (`.payment-card__info`, `.ship-label__price`, etc.)
- **Design tokens** — Variables CSS centralizadas en `:root` para colores, tipografía, espaciado y radios
- **SVG inline** — Planetas (Saturno, planeta azul), órbita animada, íconos de UI todos embebidos

---

## 🎨 Sistema de diseño

### Tipografías
| Rol | Familia |
|---|---|
| Display / Logo | `Orbitron` (Google Fonts) |
| Body / UI | `Syne` (Google Fonts) |
| Código / Monoespaciado | `Space Mono` (Google Fonts) |

### Paleta principal
| Token | Valor | Uso |
|---|---|---|
| `--bg-void` | `#04040a` | Fondo más profundo |
| `--bg-card` | `#0e0e1a` | Tarjetas y paneles |
| `--accent` | `#7c6dfa` | Color de marca / primario |
| `--accent-bright` | `#a89bff` | Énfasis y hovers |
| `--gold` | `#f0b429` | Badge Default, detalles premium |
| `--danger` | `#f05252` | Acciones destructivas |
| `--text-0` | `#f4f4ff` | Texto principal |
| `--text-2` | `#52526a` | Texto terciario / placeholders |

### Moneda ficticia
El sistema usa **◈** (Space Credits) como unidad monetaria para todos los precios de viaje.

---

## 🚀 Cómo usar

No se requiere servidor ni build tools. Simplemente abre `index.html` en cualquier navegador moderno:

```bash
# Opción 1 — Abrir directo
open index.html

# Opción 2 — Servidor local (recomendado para evitar CORS en imágenes)
npx serve .
# o
python3 -m http.server 8080
```

> **Nota:** Las imágenes de planetas en `travel.html` se cargan desde URLs externas. Se recomienda un servidor local para una experiencia óptima.

---

## 🌐 Compatibilidad

| Navegador | Soporte |
|---|---|
| Chrome / Edge 90+ | ✅ Completo |
| Firefox 88+ | ✅ Completo |
| Safari 14+ | ✅ Completo |
| Mobile (iOS/Android) | ✅ Diseñado mobile-first |

---

## 📐 Convenciones de código

- **Git:** [Conventional Commits](https://www.conventionalcommits.org/)
- **CSS:** BEM para componentes, tokens globales en `:root`
- **HTML:** Semántico con atributos ARIA (`aria-label`, `aria-hidden`, `role`)
- **Sin frameworks:** Vanilla HTML5 + CSS3, JS inline mínimo solo donde necesario

### Ejemplos de commits
```
feat(splash): animación orbital CSS-only
feat(travel): bottom sheet expandible CSS-only
feat(payment): payment cards con BEM
feat(receipt): glassmorphism fondo claro
fix(home): contraste de texto en modo oscuro
```

---

## 👤 Autor

**Sebastian Jaimes**  
Prototipo de concepto — UberX × SpaceX Space Rides  
Año ficticio: 2053

---

## 📄 Licencia

Proyecto de demostración / portafolio. No afiliado con Uber ni SpaceX.