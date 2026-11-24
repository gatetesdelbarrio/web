# Web de Gatetes del Barrio

Web estática en español: un solo archivo `index.html` (CSS, logo y un poco de JavaScript incluidos). Sin backend, sin analítica, sin cookies propias, sin coste.

Estado: la rama `preview` tiene la web lista para revisar. `main` (producción) está vacía a propósito hasta que los dueños den el ok.

## Quién es dueño de qué
| Cosa | Cuenta / dónde |
|---|---|
| Código | GitHub, usuario `gatetesdelbarrio`, repo https://github.com/gatetesdelbarrio/web |
| Alojamiento | Cloudflare Pages, proyecto `gatetesdelbarrio` (plan gratuito), conectado al repo por Git |
| Gmail, Drive, formulario | Google, cuenta `gatetesdelbarrio@gmail.com` |
| Gráficos originales | Drive compartido "Gatetes" (solo lectura, no tocar), carpeta Graficos |
| Copia de trabajo de la web | Drive de Gatetes, carpeta "Web" (propia) |

Las contraseñas están en el gestor de contraseñas del dueño. No hay credenciales en el repo.

## Direcciones
- Producción (`main`): https://gatetesdelbarrio.pages.dev
- Vista previa (`preview`): https://preview.gatetesdelbarrio.pages.dev (cada commit también tiene su propia URL en Cloudflare)

## Contenido de la web
Portada, Quiénes somos, Cómo ayudar, Adopta (formulario de Google), En directo (Twitch), Contacto y redes. Los textos salen del Instagram público (@gatetesdelbarrio). Lo que no se sabe está marcado con "[Pendiente: ...]" en una línea propia.

## Cómo hacer cambios
Siempre en la rama `preview`, nunca directo en `main`.
1. Editar texto: en GitHub abrir `index.html` en `preview`, lápiz de editar, cambiar el texto, "Commit changes" con "Commit directly to the preview branch". Cloudflare publica la vista previa en 1 o 2 minutos.
2. Quitar un marcador pendiente: borrar la línea `<p class="todo">[Pendiente: ...]</p>` y poner el texto real.
3. Añadir fotos: solo si la asociación confirma que son suyas. Redimensionar a unos 1200 px de ancho y menos de 200 kB, subirlas a la carpeta `img/` del repo y usar `<img src="img/nombre.jpg" alt="descripción" loading="lazy">`. Aviso: la subida por navegador de GitHub puede añadir un número delante del nombre; con git no pasa. Para un carrusel, un `<div>` con `display:flex; overflow-x:auto; scroll-snap-type:x mandatory` y varias imágenes basta, sin librerías.
4. Cambiar el formulario de adopción: en `index.html`, en la sección `#adopta`, cambiar la dirección en `data-src` (debe acabar en `/viewform?embedded=true`) y el enlace de "abrirlo en una pestaña nueva". Para sacarla en Google Forms: Enviar, pestaña `<>`, copiar el `src`.
5. Cambiar el canal de Twitch: en la sección `#directo`, cambiar el valor de `data-twitch`. No hace falta tocar `parent`, el código usa el dominio actual (vale para pages.dev y para un dominio propio).
6. Añadir una red social: añadir un `<li><a href="URL" rel="noopener">Nombre</a></li>` en la lista de `#contacto`.

## Publicar de preview a main (solo con el ok de los dueños)
1. En GitHub, repo `web`, pestaña Pull requests, New pull request, base `main`, compare `preview`.
2. Revisar la vista previa una última vez en escritorio y móvil.
3. Merge. Cloudflare publica en producción en 1 o 2 minutos en https://gatetesdelbarrio.pages.dev.
4. Para deshacer: en Cloudflare, proyecto, Deployments, un despliegue anterior, "Rollback"; o revertir el commit en GitHub.

## Embeds y servicios de terceros
- Formulario de adopción: Google Forms (enlace corto https://forms.gle/nP84wdVC7PU2gWB48). Las respuestas las recibe la asociación en Google. La web no guarda nada.
- Twitch: canal `gatetesdelbarrio`.
- Los dos embeds solo se cargan cuando la persona pulsa el botón. Al pulsar se cargan cookies y contenido de Google o de Twitch. Hasta entonces la web no carga nada de terceros.
- Enlaces (sin embed): Instagram, Threads, Twitch, PayPal (paypal.me/gatetesdelbarrio).
- No hay X ni TikTok porque no se han encontrado cuentas públicas de la asociación.

## Decisiones pendientes, con propuesta por defecto
| Decisión | Propuesta por defecto |
|---|---|
| Publicar en producción | Sí, cuando se hayan rellenado o aceptado los marcadores |
| Dominio propio | No de momento. Seguir con pages.dev (gratis). Si se quiere, un .org o .es cuesta unos 10 a 15 euros al año; decide quien pague |
| Correo público de contacto | No publicar ninguno todavía. Contacto por mensaje directo de Instagram |
| Historia, año de inicio y equipo | Dejar el marcador hasta que la asociación pase un texto. No inventar |
| Voluntariado (tareas, horarios, zonas) | Crear un Google Form propio en el Drive de Gatetes y enlazarlo en "Cómo ayudar" |
| Fotos de gatos | Solo las de la asociación, sin personas reconocibles. Hasta entonces, solo el logo |
| Aviso de cookies | No hace falta con los embeds a un clic. Si se carga algo de terceros sin clic, hay que añadirlo |
| X y TikTok | No añadir hasta que existan cuentas |

## Restricciones acordadas
- Sin datos personales de voluntarios en la web ni backend propio.
- No tocar la carpeta compartida "Gatetes" del Drive (solo leer o copiar).
- Sin gastos ni plan de pago sin aprobación de los dueños.
