# Mis 3 valores esenciales · SSK002

Web estática para GitHub Pages con conexión a Google Sheets y correo automático mediante Apps Script.

## Configuración (una sola vez)

1. Abre la hoja nueva: https://docs.google.com/spreadsheets/d/1RjPpefWlu5Yu9GB-kKFlqEhxOdi1Z2sc8OE8QlxHzlw/edit?usp=drivesdk
2. En esa hoja, abre **Extensiones → Apps Script**. Sustituye el contenido de `Code.gs` por el archivo `Code.gs` de este paquete y guarda.
3. En **Implementar → Nueva implementación → Tipo: Aplicación web**, selecciona **Ejecutar como: Yo** y **Acceso: Cualquier usuario**. Concede a Apps Script los permisos para editar Sheets y enviar correo. Copia el URL que termina en `/exec`. Si tu organización impide acceso público, pide autorización institucional o usa una implementación con acceso restringido.
4. Abre `index.html` y reemplaza `PEGA_AQUI_LA_URL_DE_APPS_SCRIPT` por ese URL `/exec` (entre las comillas existentes).
5. En GitHub crea un repositorio (por ejemplo `ssk002-valores`). Sube `index.html` y `README.md` a la raíz. `Code.gs` se puede mantener **fuera del repositorio público**; no contiene credenciales, pero publicar el script no es necesario.
6. En GitHub: **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save**.
7. Abre la URL de GitHub Pages y completa una prueba con tu propio correo y una matrícula de prueba. Comprueba: nueva fila en pestaña `Resultados`, columna `Estado del correo` igual a `ENVIADO`, mensaje de éxito en la web y correo recibido.

## Notas importantes

- El enlace de Apps Script estará visible en el código público; **no es un secreto**. Puede recibir peticiones externas. Para uso en grupo cerrado, considera acceso restringido, políticas institucionales y monitoreo de cuotas de MailApp.
- La matrícula se utiliza para bloquear un segundo envío; si necesitan corregir uno, el profesor puede borrar o modificar el registro manualmente.
- Las descripciones del perfil son **orientativas, no diagnósticas**; las reglas de interpretación están en el navegador y se envían a la hoja. Si buscas integridad reforzada, traslada la construcción del perfil al script del servidor.
- Los datos de identificación y valores se guardan en la cuenta propietaria del Google Sheets y se envían por correo a los participantes. Configura los permisos de la hoja para que solo el profesor tenga acceso. No incluyas matrículas ni correos en la web pública.
- La entrega se basa en la matriz de 15 cuadros del archivo `Valores.pdf`, preservando su orden por filas y columnas.
- Apps Script tiene cuotas de envío de correo. Antes de aplicar a todo el grupo comprueba que queden suficientes envíos diarios.
