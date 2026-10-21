# Dinámica de valores · SSK002 — versión sin interpretación

## Qué cambia
- En la pantalla final solo aparecen **los tres valores y sus definiciones**.
- El correo reproduce esos mismos valores y definiciones, sin perfil ni juicios.
- Cada una de las tres columnas tiene un título visual en la primera ronda, y en la segunda se muestra «Elige 1 de 5».
- Se conservan **15 valores iniciales**, tres finales, nombre, matrícula, correo y estado del envío.
- Se conservan las 16 columnas técnicas del Google Sheet existente para evitar desplazar información histórica. Las cuatro columnas anteriores de interpretación quedan vacías para nuevas respuestas.

## Actualizar GitHub
1. Sustituye `index.html` en el repositorio (mantén la URL real de Apps Script en `SCRIPT_URL` — la plantilla descargada trae un marcador).
2. Confirma los cambios en `main` y verifica la página de GitHub Pages.

## Actualizar Google Apps Script
1. En la hoja de resultados, Extensiones > Apps Script, sustituye el contenido de `Code.gs` por este archivo.
2. Implementar > Administrar implementaciones > lápiz (editar) > Versión: Nueva versión > Implementar.
3. Prueba con un correo y una matrícula que no se hayan utilizado en pruebas anteriores.

**Importante:** actualizar únicamente GitHub no cambia el correo: hay que actualizar también Google Apps Script y crear una nueva versión de implementación.

## Actualización: sentido práctico de los valores

El resultado en pantalla y el correo incluyen siete aplicaciones pedagógicas comunes a todos los alumnos y una pregunta de reflexión. No se infieren rasgos, fortalezas, retos ni perfiles individuales.

Para actualizar: reemplaza `index.html` en GitHub y conserva tu URL `/exec` real en `SCRIPT_URL`. Sustituye `Code.gs` en el Apps Script vinculado al Sheet, guarda y ve a **Implementar > Administrar implementaciones > Editar > Nueva versión > Implementar**. Los encabezados existentes de Google Sheets no cambian.
