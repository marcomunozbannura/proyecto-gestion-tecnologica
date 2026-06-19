# One Page — Proyecto de Gestión Tecnológica

Dos piezas para captar dueños de pyme hacia el botón de WhatsApp y el **piloto gratis**.

## Las dos entregas

1. **El link (la landing)** → `index.html`
   Página de una sola página, responsive (se ve bien en celular y computador), autocontenida
   (HTML + CSS + JS en un archivo). Es lo que compartes como **enlace**.

2. **La imagen para WhatsApp** → `compartir.png`
   Pieza vertical 1080×1920 lista para mandar directo por chat o estado. Funciona sola:
   tiene el gancho, el "PILOTO GRATIS" y los dos números de teléfono. Es la que pega fuerte
   para difusión masiva en grupos.

## Archivos
| Archivo | Qué es |
|---|---|
| `index.html` | La landing (el link). |
| `compartir.png` | **Imagen vertical para mandar por WhatsApp.** |
| `og-image.png` | Imagen 1200×630 del preview cuando pegas el *link* en WhatsApp/redes. |
| `compartir.html` / `og-image.html` | Fuentes con que se generaron los PNG (no es necesario subirlas). |
| `_serve.ps1` | Servidor local para previsualizar (solo pruebas, no se sube). |

## Probar en tu computador
- Doble clic en `index.html` abre la landing en el navegador (el preview del link OG solo se
  ve una vez publicado, ver abajo).
- O clic derecho en `_serve.ps1` → "Ejecutar con PowerShell" y abre http://localhost:8123/

## Publicar para tener el link (con preview bonito en WhatsApp)
Lo más rápido y gratis: **GitHub Pages** (ya lo usan) o **Netlify Drop**.

- **Netlify (lo más simple):** entra a app.netlify.com/drop → arrastra la carpeta `one-page`.
  Te da una URL al instante.
- **GitHub Pages:** crea un repo, sube los archivos, Settings → Pages → Deploy from branch.

Sube al menos `index.html` y `og-image.png` (que queden en la misma carpeta).

### ⚠️ Paso obligatorio después de publicar
Abre `index.html` y pon tu URL real en las metaetiquetas `og:url`, `og:image` y `twitter:image`
(están al inicio, marcadas con un comentario). Sin esto el preview del link no muestra la imagen.
Para que WhatsApp/Facebook refresquen el preview: https://developers.facebook.com/tools/debug/

## Editar (sin saber programar)
Abre `index.html` con el Bloc de notas. Busca el bloque **"ZONA EDITABLE"** al inicio:
- **Teléfonos / mensajes WhatsApp** → busca `wa.me`.
- **Correos** → busca `mailto:`.
- **Colores** → variables al inicio del `<style>` (busca `--azul`, `--teal`, `--wa`).
- **Textos** → están en el HTML, separados por secciones con comentarios.

> Si cambias textos de la **imagen** (`compartir.png` / `og-image.png`), edita
> `compartir.html` / `og-image.html` y pide regenerar los PNG (se generan con captura headless).
