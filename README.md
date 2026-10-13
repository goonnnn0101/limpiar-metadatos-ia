# Limpiar Metadatos IA

Herramienta web **100 % local** para eliminar metadatos y rastros de IA de tus archivos.

No sube nada a ningún servidor: todo se procesa en tu navegador.

## Formatos soportados

| Formato | Qué limpia |
|--------|------------|
| **Word** (`.docx`) | Autor, software, fechas, título, keywords. El texto no se modifica. |
| **Excel** (`.xlsx`) | Igual. El contenido de las celdas no se toca. |
| **PowerPoint** (`.pptx`) | Igual. Las diapositivas no se tocan. |
| **PDF** | Título, autor, creador, productor, keywords y fechas. |
| **Imágenes** | EXIF, GPS, C2PA, prompts y metadatos embebidos (re-codificación). |
| **Texto** (`.txt`, `.md`…) | Caracteres invisibles y muletillas típicas de estilo IA. |

## Cómo usar

1. Abre [`index.html`](index.html) en tu navegador (o clona el repo y ábrelo localmente).
2. Arrastra uno o varios archivos.
3. En cada archivo puedes elegir:
   - Nombre de salida
   - Fecha de creación
   - Fecha de modificación
4. (Opcional) Usa la barra superior para aplicar las mismas fechas a todos o añadir el prefijo `limpio_`.
5. Pulsa **Limpiar y descargar**.

## Características

- Controles **por archivo** (nombre y fechas independientes)
- Aplicar fechas globales a todos los archivos de la lista
- Prefijo automático `limpio_`
- Diseño moderno y responsive
- Sin dependencias de servidor

## Limitaciones

- La **marca estadística** de modelos como Claude o Gemini (sesgo en la elección de palabras) no se elimina con metadatos: solo se diluye reescribiendo el texto.
- En documentos Office solo se limpian metadatos; el contenido se conserva intacto a propósito.

## Privacidad

Todo el procesamiento ocurre en el navegador. Ningún archivo se envía a ningún servidor.

## Licencia

Uso libre. Si mejoras la herramienta, las contribuciones son bienvenidas.
