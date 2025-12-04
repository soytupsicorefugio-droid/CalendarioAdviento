# 🎄 Calendario de Adviento Interactivo (Plantilla)

Una plantilla de calendario de Adviento digital, elegante y totalmente personalizable. Esta versión incluye mensajes genéricos de ejemplo pensados para mostrar usos posibles (música, imágenes, descargas, pistas y pequeños regalos digitales), además de persistencia local del progreso.

## ✨ Características principales

- 🎁 Interacción: 24 cajas clicables con animaciones de apertura.
- 🔒 Bloqueo de días futuros (configurable).
- 💾 Persistencia local: los días abiertos se guardan en `localStorage` para que el progreso no se pierda al recargar.
- 🧩 Mensajes en JSON: `messages.json` contiene 24 entradas editables que el comprador puede personalizar.
- 🎨 Efectos visuales: brillo, sparkles, confeti y modal con fondo animado.
- 📱 Responsive: optimizado para escritorio y dispositivos táctiles.

## 📁 Estructura del proyecto

```
Calendario Adviento/
├── index.html          # Archivo principal con HTML, CSS y JS
├── messages.json       # Mensajes de ejemplo (24 entradas) — edítalo para personalizar
└── resources/          # Carpeta para imágenes y assets (ej. sorpresa, iconos)
```

## 💬 Contenido de ejemplo en `messages.json`

Los mensajes incluidos en la plantilla son demostrativos y están pensados para mostrar qué se puede incluir:
- Texto corto (saludos, reflexiones).
- Enlaces a multimedia (Spotify, YouTube) que el sistema convierte en botones o enlaces.
- Enlaces a descargas o recursos (`https://...`).
- Indicaciones para usar imágenes en `resources/` (por ejemplo `resources/sorpresa.png`).
- Pistas para regalar contenido escondido o actividades interactivas.

Ejemplo de estructura:

```json
{
  "1": "Un pequeño saludo para comenzar: abre este día y respira — algo bonito te espera.",
  "2": "Hoy hay una melodía para la tarde; imagina una canción que calme los vientos.",
  ...
  "24": "Cierre cálido: gracias por acompañar este calendario — añade aquí tu despedida y contacto."
}
```

Consejos para compradores:
- Mantén los enlaces completos `https://...` para que la función de linkify los transforme correctamente.
- Usa rutas relativas a `resources/` para imágenes internas (por ejemplo `resources/fondo.png`).
- Evita HTML complejo dentro de los mensajes; el sistema escapará HTML para seguridad.

## 🛠️ Cómo editar y probar

1. Edita `messages.json` con tus 24 mensajes.
2. Coloca cualquier imagen o archivo en `resources/`.
3. Prueba localmente con un servidor simple (recomendado):

```powershell
cd "C:\ruta\a\tu\repositorio"
python -m http.server 8000
```

Abre `http://localhost:8000/` en tu navegador.

## 📌 Publicar en GitHub Pages

1. Asegúrate de que `index.html`, `messages.json` y `resources/` estén en la rama `main` (o en la rama que hayas configurado para Pages).
2. Haz commit y push:

```powershell
git add .
git commit -m "Plantilla: mensajes genéricos y assets"
git push origin main
```

3. En GitHub, ve a `Settings > Pages` y confirma la rama `main` como fuente de publicación. Espera unos minutos a que la página se construya.

La URL será `https://<usuario>.github.io/<repositorio>/` (o tu dominio personalizado si lo configuras).

## 🔧 Personalización rápida

- Cambiar el día actual bloqueado: en `index.html` ajusta la variable `currentDay` (si está hardcodeada) o modifica la función `getCurrentDay()` para que use la fecha del sistema.
- Colores y tipografías: modifica las variables y reglas CSS dentro de `index.html`.
- Duración de animaciones: busca keyframes `lidFade`, `softGlow`, `sparkleFall`, `confettiFall`.

## ✅ Seguridad y buenas prácticas

- Los mensajes se sanitizan antes de mostrarse para reducir riesgo de XSS.
- Cuando añadas enlaces, usa `https://` para evitar advertencias de contenido mixto.

## 🚀 Ideas para vender la plantilla

- Incluye un `README` claro (ya actualizado) que explique cómo editar `messages.json`.
- Proporciona un archivo `assets.zip` con imágenes de muestra en `resources/`.
- Ofrece varias versiones de ejemplo (idiomas, estilos de copy) como extras descargables.

## 📝 Licencia

Plantilla distribuida bajo licencia MIT. Nota al comprador: revisa y adapta cualquier contenido con derechos (música, imágenes) antes de uso comercial.

## 🤝 Créditos

Desarrollado como plantilla interactiva de Adviento.

