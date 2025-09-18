# BHOP / KZ Records (GitHub Pages)

Este repo publica una página estática con `index.html` que lee `records.json` y muestra los records.
Funciona como URL para MOTD en CS 1.6.

## Pasos (de cero)

1. Crea un repositorio en GitHub. Nombre sugerido: `bhop-records`.
2. Sube **estos tres archivos** al root del repo:
   - `index.html`
   - `records.json`
   - `README.md` (opcional)
3. Ve a **Settings → Pages**:
   - Source: **Deploy from a branch**
   - Branch: **main** (o `master`) y carpeta **/** (root).
   - Guarda.
4. Espera a que GitHub compile. Tu sitio quedará en:
   - `https://TU-USUARIO.github.io/bhop-records/`

> Reemplaza `TU-USUARIO` por tu usuario real de GitHub.

## Actualizar los records
Edita `records.json` desde la web de GitHub (botón **Edit**) o sube un nuevo archivo. La web hará `fetch()` a ese JSON y mostrará los datos.

## Usar en MOTD (AMXX / Pawn)
```pawn
show_motd( id, "https://TU-USUARIO.github.io/bhop-records/", "Top / Records" );
```

Si el navegador del juego tiene problemas con HTTPS, puedes usar un acortador o un proxy HTTP; sin embargo, GitHub Pages sirve solo HTTPS.
