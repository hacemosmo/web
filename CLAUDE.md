# Web de MO Estudio — instrucciones de trabajo

## Qué es
Web corporativa de MO Estudio (Marketing · Comunicación · Eventos), marca del Grupo IB10.
Dominio: https://hacemosmo.es (principal) y www.hacemosmo.es.

## Cómo se publica
- Repositorio: `hacemosmo/web` (GitHub, público), rama `main`.
- GitHub Pages publica automáticamente cada push a `main` (Settings → Pages → Deploy from a branch → `main` / root).
  Sin compilación propia. El archivo `CNAME` fija el dominio `hacemosmo.es`: no borrarlo.
  `_config.yml` excluye de la web los archivos internos (CLAUDE.md, README.md).
- Flujo: editar → commit → push a `main` → comprobar que el despliegue de Pages termina bien (pestaña Actions del repositorio).
- El repositorio es público: no subir nunca contraseñas, datos personales de clientes ni documentos internos.
- Netlify se usó al principio (noviembre 2026) y se abandonó por la insignia "Powered by Netlify" del plan gratuito.

## Estructura
- `index.html`: página principal (HTML + CSS + JS en el mismo archivo).
- `aviso-legal.html`, `privacidad.html`, `cookies.html`: páginas legales (noindex). La web no usa cookies; si se añade analítica, hay que poner banner de consentimiento y actualizar `cookies.html`.
- `favicon.svg` e `images/compartir.jpg` (imagen para redes, 1200×630).
- `images/`: fotos ya tratadas (tono marino/marfil). Fuentes y licencias en `images/FUENTES.txt`
  (Pexels/Burst, uso comercial libre). Optimizar antes de subir: JPEG progresivo, calidad ~80, lado mayor ≤1600 px (portada ≤2200 px).
- Formulario de contacto: Web3Forms (plan gratuito, 250 envíos/mes) envía cada mensaje por correo a hola@hacemosmo.es. Clave pública en `W3F_KEY` dentro de `index.html`; formulario "Contacto web MO" en la cuenta de Web3Forms de hacemosmo@gmail.com. Antispam: campo oculto `botcheck`.

## Marca
- Colores: azul marino #1B2A41, rojo #7A1F2B, marfil #FBF8F1, blanco. El verde #2F4538 solo de forma puntual.
- Tipografías de marca: Cormorant Garamond (titulares) y Montserrat (texto).
- Tono: sobrio, elegante, clásico, cercano y serio. Nada de textos vulgares ni de "nuestros servicios".

## Reglas
- Contacto público: hola@hacemosmo.es, teléfono 606 26 57 07 (publicado a petición expresa, 17/11/2026) e Instagram @hacemosmo. No añadir WhatsApp salvo que se pida.
- No publicar casos o clientes inventados como si fueran reales.
- Web lanzada el 19/11/2026 (sin noindex en la portada).
- El titular es un autónomo que no quiere publicar nombre, NIF ni domicilio: el aviso legal identifica la web por el nombre comercial MO Estudio y el contacto. No añadir esos datos salvo que el titular lo pida.
- DNS en OVH: A `@` → 185.199.108.153 / .109.153 / .110.153 / .111.153 (GitHub Pages), CNAME `www` → hacemosmo.github.io., TXT `_github-pages-challenge-hacemosmo` (verificación del dominio en GitHub: no borrar). No tocar MX, SPF, DKIM, DMARC ni SRV del correo.
