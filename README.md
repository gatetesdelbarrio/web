# Web de Gatetes del Barrio

Web estática en español (un solo archivo `index.html`, CSS y logo incluidos). Sin backend, sin analítica, sin cookies propias.

## Estructura
- `index.html`: portada, quiénes somos, cómo ayudar, adopción (formulario de Google), directo en Twitch, contacto y redes.
- Logo: incrustado en el HTML (versión del Drive, carpeta Gatetes/Graficos, `gatetes_(3)-transformed.png`).

## Despliegue
- Repo: https://github.com/gatetesdelbarrio/web
- Cloudflare Pages, proyecto `gatetesdelbarrio`, conectado a este repo por Git (plan gratuito).
- Rama `main` = producción (https://gatetesdelbarrio.pages.dev). Rama `preview` = vista previa (Cloudflare crea una URL por commit).
- Flujo: editar en `preview`, revisar, y solo con el visto bueno de los dueños pasar a `main`.
- Las cuentas (GitHub, Cloudflare, Google) están en el gestor de contraseñas del dueño. No hay credenciales en el repo.

## Embeds y servicios externos
- Formulario de adopción: Google Forms (https://forms.gle/nP84wdVC7PU2gWB48). Los datos los recibe la asociación en Google, no esta web.
- Twitch: canal gatetesdelbarrio. El reproductor usa el dominio actual como `parent`, así que funciona en pages.dev y en un dominio propio sin cambios.
- Los dos embeds solo se cargan cuando la persona pulsa el botón (así no hay cookies de Google ni Twitch al entrar).
- Enlaces: Instagram, Threads, Twitch, PayPal (paypal.me/gatetesdelbarrio).

## Pendiente (marcadores en la web)
- Historia, año de inicio y equipo (texto de "Quiénes somos").
- Tareas, horarios y zonas del voluntariado.
- Fotos reales de los gatos (solo si la asociación confirma derechos).
- Enlaces a X y TikTok: no se han encontrado cuentas públicas, no se han añadido.

## Decisiones para los dueños
- Publicar en producción (`main`).
- Dominio propio (hoy solo pages.dev, sin coste).
- Canal de contacto para voluntarios (hoy: mensaje por Instagram).
- Si quieren un formulario de voluntariado (sería otro Google Form).
