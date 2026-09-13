<p align="center">
  <img src="logo.png" alt="CodeText Software" width="320">
</p>

<h1 align="center">RenamePdfs_isbn</h1>

<p align="center">
  Automatically rename your PDF and EPUB e-books by ISBN — title, publisher, subject, metadata, OCR and online cover, all in one click.<br>
  <em>Renombra tus PDFs y EPUBs automáticamente por ISBN — título, editor, tema, metadatos, OCR y portada online, en un solo clic.</em>
</p>

<p align="center">
  <img src="RenamePdfs_isbn_principal_Eng.png" alt="RenamePdfs_isbn main window (English)" width="850">
</p>

---

## English

**RenamePdfs_isbn** is a free Windows tool that scans a folder of PDF and EPUB files, finds the ISBN of each book (from its text, its metadata, or — if the file has no embedded text — via OCR), looks up the real title, publisher, edition and subject online, and renames the file accordingly. It can also write that information back into the PDF metadata and add an online cover as the first page.

### Features

- **ISBN detection** from embedded text, PDF/EPUB metadata, or OCR (via Tesseract) when the file has no extractable text.
- **Online lookup** of title, publisher/year and subject (Google Books, Open Library, CrossRef/DOI, and more).
- **Smart fallbacks**: local title from PDF/EPUB metadata, content-based heuristics, or a plain filename-based search — only when nothing reliable is found does it skip renaming, rather than risking a wrong title.
- **Configurable naming format**: append the year, the publisher, both, or neither.
- **Cover insertion**: fetches a cover image online and inserts it as page 1 when the file doesn't already have one.
- **Metadata writing**: title, ISBN, edition and subject can be written back into the PDF's own metadata.
- **Three run modes**: *simulate* (preview only), *rename*, or *run without renaming* (apply metadata/cover but keep the filename).
- **OCR support** for scanned/image-only PDFs (requires Tesseract OCR, see [Requirements](#requirements)).
- **Bilingual interface** (English / Español), switchable at any time from the header — every label, message and log line follows the selected language.
- **Adjustable process priority** (Real Time / High / Normal / Low), verified against what Windows actually applies — not just what was requested.
- **Fully themeable**: window colors, button colors, grid and log colors are all configurable from `config.xml`.
- **Detailed process log**, exportable to a `.txt` file, plus an optional `.csv` report of every processed file.
- **Portable & self-contained**: single `.exe`, no installation beyond Tesseract for OCR; the CodeText logo is embedded in the executable itself.

### Requirements

- Windows 10/11.
- [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki) installed system-wide (or placed in a `.\tesseract\` subfolder next to the executable) — only needed for scanned PDFs without embedded text.
- An internet connection for online lookups (title, publisher, cover).

### Installation

1. Download the latest `RenamePdfs_isbn_vX_X_Windows.zip` from the [Releases](../../releases) page (or via the update icon 🔄 inside the app).
2. Unzip it anywhere.
3. Install Tesseract OCR (see [Requirements](#requirements)) if you plan to process scanned PDFs.
4. Run `RenamePdfs_isbn.exe`.

### Usage

1. Pick the folder (or individual files) to process with the 📁 button.
2. Choose a run mode (*simulate*, *rename*, *run without renaming*), the naming format (year/publisher), and the desired options (OCR, metadata, subject, cover, log).
3. Click **Run**. You can **Pause** or **Cancel** at any point.
4. Review the results in the grid: ISBN found, new name, status and comments. A `.csv` report and/or `.txt` log can be saved automatically.

### Configuration (`config.xml`)

`config.xml` is created automatically next to the executable on first run, and stores:

- Window size, column widths and log panel height.
- Last used folder and file filter.
- Interface language (`<idioma valor="en"/>` or `"es"`, English by default).
- Preferred process priority (`<prioridad valor="tiempo_real"/>`, etc.).
- All interface colors (`<colores .../>`): panel background, field background, selection color, grid scrollbars, button colors, general text color, and the "Process detail" panel's background/text/selection colors.

You can edit these values by hand (with the app closed); they're applied the next time it starts.

### Building from source

Requirements: Python 3.10+, `pip install pyinstaller pymupdf`.

Run `RenamePdfs_isbn.bat` — it builds a single portable `.exe` with PyInstaller (`--onefile --windowed`). Note: a `--onefile` build shows up as **two** processes in Task Manager while running (the self-extracting bootloader plus the actual app); this is normal PyInstaller behavior. See the comments in the `.bat` file if you'd rather build with `--onedir` instead.

---

## Español

**RenamePdfs_isbn** es una herramienta gratuita para Windows que analiza una carpeta de archivos PDF y EPUB, detecta el ISBN de cada libro (por su texto, sus metadatos, o mediante OCR si el archivo no tiene texto extraíble), busca online el título real, editor, edición y tema, y renombra el archivo en consecuencia. También puede escribir esa información en los metadatos del PDF y añadir una portada online como primera página.

<p align="center">
  <img src="RenamePdfs_isbn_principal.png" alt="Ventana principal de RenamePdfs_isbn" width="850">
</p>

### Características

- **Detección de ISBN** por texto embebido, metadatos del PDF/EPUB, o mediante OCR (con Tesseract) cuando el archivo no tiene texto extraíble.
- **Búsqueda online** de título, editor/año y tema (Google Books, Open Library, CrossRef/DOI, entre otros).
- **Alternativas inteligentes**: título local desde metadatos del PDF/EPUB, heurística de contenido, o búsqueda por nombre de archivo — solo se omite el renombrado cuando no hay nada fiable, en vez de arriesgar un título erróneo.
- **Formato de nombre configurable**: añadir el año, el editor, ambos o ninguno.
- **Inserción de portada**: obtiene una imagen de portada online y la inserta como página 1 cuando el archivo no tiene ya una.
- **Escritura de metadatos**: título, ISBN, edición y tema pueden escribirse en los metadatos propios del PDF.
- **Tres modos de ejecución**: *simular* (solo previsualiza), *renombrar*, o *ejecutar sin renombrar* (aplica metadatos/portada pero conserva el nombre).
- **Soporte OCR** para PDFs escaneados/solo imagen (requiere Tesseract OCR, ver [Requisitos](#requisitos)).
- **Interfaz bilingüe** (Español / English), cambiable en cualquier momento desde la cabecera — todos los textos, mensajes y el log siguen el idioma elegido.
- **Prioridad de proceso ajustable** (Tiempo Real / Alta / Normal / Baja), comprobada contra lo que Windows aplica realmente, no solo lo pedido.
- **Totalmente personalizable**: colores de ventana, botones, grid y log configurables desde `config.xml`.
- **Detalle del proceso** exportable a `.txt`, además de un reporte `.csv` opcional de cada archivo procesado.
- **Portátil y autocontenido**: un solo `.exe`, sin más instalación que Tesseract para el OCR; el logo de CodeText va incrustado en el propio ejecutable.

### Requisitos

- Windows 10/11.
- [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki) instalado en el sistema (o colocado en una subcarpeta `.\tesseract\` junto al ejecutable) — solo necesario para PDFs escaneados sin texto embebido.
- Conexión a internet para las búsquedas online (título, editor, portada).

### Instalación

1. Descarga el último `RenamePdfs_isbn_vX_X_Windows.zip` desde la página de [Releases](../../releases) (o con el icono de actualizar 🔄 dentro de la app).
2. Descomprímelo donde quieras.
3. Instala Tesseract OCR (ver [Requisitos](#requisitos)) si vas a procesar PDFs escaneados.
4. Ejecuta `RenamePdfs_isbn.exe`.

### Uso

1. Elige la carpeta (o archivos concretos) a procesar con el botón 📁.
2. Elige el modo de ejecución (*simular*, *renombrar*, *ejecutar sin renombrar*), el formato de nombre (año/editor) y las opciones deseadas (OCR, metadatos, tema, portada, log).
3. Pulsa **Ejecutar**. Puedes **Pausar** o **Cancelar** en cualquier momento.
4. Revisa los resultados en la tabla: ISBN encontrado, nuevo nombre, estado y comentarios. Se puede guardar automáticamente un reporte `.csv` y/o un log `.txt`.

### Configuración (`config.xml`)

`config.xml` se crea automáticamente junto al ejecutable en el primer arranque, y guarda:

- Tamaño de ventana, ancho de columnas y alto del panel de log.
- Última carpeta y filtro de archivos usados.
- Idioma de la interfaz (`<idioma valor="en"/>` o `"es"`, inglés por defecto).
- Prioridad de proceso preferida (`<prioridad valor="tiempo_real"/>`, etc.).
- Todos los colores de la interfaz (`<colores .../>`): fondo del panel, fondo de campos, color de selección, barras del grid, colores de botones, color de texto general, y fondo/texto/selección del panel "Detalle del proceso".

Estos valores se pueden editar a mano (con la app cerrada); se aplican en el siguiente arranque.

### Compilar desde el código fuente

Requisitos: Python 3.10+, `pip install pyinstaller pymupdf`.

Ejecuta `RenamePdfs_isbn.bat` — genera un único `.exe` portátil con PyInstaller (`--onefile --windowed`). Nota: una compilación `--onefile` aparece como **dos** procesos en el Administrador de tareas mientras se ejecuta (el bootloader autoextraíble más la aplicación real); es un comportamiento normal de PyInstaller. Consulta los comentarios del `.bat` si prefieres compilar con `--onedir`.

---

<p align="center">
  © 2026 <a href="https://www.codetext.org">CodeText Software</a>. All rights reserved. / Todos los derechos reservados.
</p>
