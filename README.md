# Portafolio — Fabian García

Portafolio personal de **Fabian García**, ingeniero de software full stack.

Live: https://portfolio.pages.dev (o tu dominio custom si configuraste uno)

---

## Stack de este sitio

- **HTML5** + **CSS3** (custom properties, grid, flexbox)
- **JavaScript vanilla** (Intersection Observer para reveal animations, i18n manual con `localStorage` + `navigator.language`)
- **Cero dependencias, cero build step.**

> **¿Por qué HTML puro si mi stack es React / NestJS / Spring Boot?**
> Decisión deliberada. Para una landing estática de 2 páginas, agregar React + Vite + un bundler agrega más complejidad operativa que valor:
> - **Deploy instantáneo** (<2s) en Cloudflare Pages, sin build.
> - **First Contentful Paint** prácticamente inmediato — no hay bundle JS bloqueando el render.
> - **Cero dependencias** = cero `npm audit` warnings, cero supply-chain risk.
> - **El código es leíble en `View Source`** — un reclutador o dev puede auditar todo el sitio en 5 minutos.
>
> El stack pesado está en mis **proyectos reales**, no en la vidriera.

---

## Mis proyectos reales (donde sí está el stack pesado)

- **INAB Wildfire Monitoring** — React Native + Expo + Node/Express + PostGIS + Firebase FCM
  - Frontend: https://github.com/Fabi-Gar/frontend-expo-actualizado
  - Backend:  https://github.com/Fabi-Gar/Backend-app-Incendios
- **Wallet Pass SaaS Multi-Tenant** — NestJS (DDD Hexagonal) + React 19 + PostgreSQL + Tailwind v4 + Docker (repo privado por ahora)
- **Softcontext** — Java Spring Boot + MongoDB + React (sitio: https://softcontext.com/)

---

## Features del portfolio

- **Internacionalización ES/EN** con detección automática de `navigator.language` y toggle persistente en `localStorage`.
- **Reveal animations** on-scroll via `IntersectionObserver` (sin librerías).
- **Sub-sitio embebido**: `send-a-miracle.html` se sirve como página independiente Y se previsualiza desde la card del portafolio.
- **Headers de seguridad** (`_headers`) configurados en Cloudflare: `X-Frame-Options`, `Referrer-Policy`, `X-Content-Type-Options`.
- **Responsive** mobile-first.

---

## Ver localmente

Abrí `index.html` directamente en el navegador, o serví la carpeta para evitar restricciones de `file://`:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy

Conectado a **Cloudflare Pages** desde la rama `main`. Cada `git push` dispara redeploy automático (~10s).

- Build command: *(none)*
- Build output: *(root)*
- Framework preset: *None*

---

## Estructura

```
.
├── index.html              # Portafolio principal
├── send-a-miracle.html     # Sub-sitio (NGO landing redesign)
├── send-a-miracle-preview.png
├── _headers                # Cloudflare Pages security headers
├── .gitignore
└── README.md
```

---

## Contacto

- Email: fabian.garcia.ac@gmail.com
- LinkedIn: https://www.linkedin.com/in/fabian-andre-garcia-mendez-b1639b214/
- GitHub: https://github.com/Fabi-Gar
