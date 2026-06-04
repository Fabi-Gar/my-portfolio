# Portafolio — Fabian García

Portafolio personal de Fabian García. HTML/CSS/JS puro, sin build step.

Incluye un sub-sitio (`send-a-miracle.html`) embebido vía iframe desde `index.html`.

## Ver localmente

Opción rápida: abrí `index.html` directamente en el navegador.

Opción recomendada (para que el iframe cargue sin restricciones de `file://`):

```bash
python3 -m http.server 8000
```

Y luego entrá a http://localhost:8000.

## Deploy

Deployado en [Cloudflare Pages](https://pages.cloudflare.com/) desde la rama `main` de este repositorio.
