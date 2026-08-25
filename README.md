# Cotizador de Créditos

App offline (PWA) para cotizar préstamos personales a 1, 3, 6, 9, 12 y 18 cuotas.

## Publicar en GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo `cotizador-creditos`).
2. Subí estos 5 elementos a la raíz del repo: `index.html`, `manifest.json`, `service-worker.js` y la carpeta `icons/` completa (con `icon-192.png` e `icon-512.png`).
3. En el repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, elegí la rama `main` y la carpeta `/root`. Guardá.
4. Esperá 1-2 minutos y va a quedar publicada en algo como:
   `https://TU-USUARIO.github.io/cotizador-creditos/`

## Instalar en el iPhone

1. Abrí esa URL en **Safari** (tiene que ser Safari, no Chrome).
2. Tocá el ícono de compartir (el cuadrado con la flecha hacia arriba).
3. Elegí **"Agregar a la pantalla de inicio"**.
4. Confirmá el nombre y tocá **"Agregar"**.

Va a quedar como un ícono más, y al abrirla funciona a pantalla completa, sin la barra de Safari. Una vez que la abriste conectado por lo menos una vez, el Service Worker deja todo guardado en el teléfono y funciona sin internet.

## Cómo funciona

- Cargás Capital, TEM (tasa efectiva mensual) y fecha de otorgamiento.
- La TEM queda guardada como valor por defecto para la próxima vez (editable siempre).
- Elegís qué planes cotizar (1, 3, 6, 9, 12, 18 cuotas).
- El plan de **1 cuota** vence 1 mes después del otorgamiento y el total a devolver es `Capital × (1 + TEM)`.
- Los demás planes usan el sistema francés (cuota fija).
- Podés destildar cualquier plan del resultado para que no aparezca en el mensaje de WhatsApp.
- El botón "Enviar por WhatsApp" abre WhatsApp con el texto ya cargado, listo para elegir el contacto.

Todo el cálculo es local: no hay servidor, no hay conexión a internet necesaria una vez instalada.
