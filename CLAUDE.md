# Web de MO Estudio — instrucciones de trabajo

## Qué es
Web corporativa de MO Estudio (Marketing · Comunicación · Eventos), marca del Grupo IB10.
Dominio: https://hacemosmo.es (principal) y www.hacemosmo.es.

## Cómo se publica
- Repositorio: `hacemosmo/web` (GitHub, privado), rama `main`.
- Netlify (equipo y proyecto `hacemosmo`) despliega automáticamente cada push a `main`.
  No hay paso de compilación: se publica la raíz del repositorio (ver `netlify.toml`).
- Flujo: editar → commit → push a `main` → comprobar que el deploy queda `ready` en Netlify.
- Para cambios grandes o dudosos, trabajar en una rama y usar la deploy preview antes de fusionar.

## Estructura
- `index.html`: página única (HTML + CSS + JS en el mismo archivo).
- `images/`: fotos ya tratadas (tono marino/marfil). Fuentes y licencias en `images/FUENTES.txt`
  (Pexels/Burst, uso comercial libre). Optimizar antes de subir: JPEG progresivo, calidad ~80, lado mayor ≤1600 px (portada ≤2200 px).
- Formulario de contacto: Netlify Forms, formulario `contacto`.

## Marca
- Colores: azul marino #1B2A41, rojo #7A1F2B, marfil #FBF8F1, blanco. El verde #2F4538 solo de forma puntual.
- Tipografías de marca: Cormorant Garamond (titulares) y Montserrat (texto).
- Tono: sobrio, elegante, clásico, cercano y serio. Nada de textos vulgares ni de "nuestros servicios".

## Reglas
- Contacto público: hola@hacemosmo.es, teléfono 606 26 57 07 (publicado a petición expresa, 17/11/2026) e Instagram @hacemosmo. No añadir WhatsApp salvo que se pida.
- No publicar casos o clientes inventados como si fueran reales.
- Mientras la web esté en construcción se mantiene `<meta name="robots" content="noindex">`; quitarlo solo al lanzar.
- DNS en OVH (no en Netlify): A `@` → 75.2.60.5, CNAME `www` → hacemosmo.netlify.app. No tocar MX, SPF, DKIM, DMARC ni SRV del correo.
