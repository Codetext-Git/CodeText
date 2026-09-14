<p align="center">
  <img src="logo.png" alt="CodeText Software" width="320">
</p>

<h1 align="center">RenamePdfs_isbn</h1>

<p align="center">
  Rename your PDF and EPUB e-books by ISBN — title, publisher, subject, metadata, OCR and online cover, all in one click.<br>
  <em>Renombra tus PDFs y EPUBs automáticamente por ISBN — título, editor, tema, metadatos, OCR y portada online, en un solo clic.</em>
</p>

<p align="center">
  <img src="RenamePdfs_isbn_principal_Eng.png" alt="RenamePdfs_isbn main window (English)" width="850">
</p>

---

## English. About CodeText Software

**CodeText** is based in Barcelona (Spain) and develops software using the latest desktop and web technologies. Our work focuses on computational semantics, creating intelligent systems to search, extract, edit, organize, and encode information in various languages. Our product  **Books Explorer** is an intelligent semantic search engine available for desktop and web that can connect to various locations hosting book repositories. We are seeking companies and institutions interested in implementing these products.

---

## Spanish. Sobre CodeText Software

**CodeText** tiene su sede en Barcelona (España) y desarrolla software utilizando las últimas tecnologías de escritorio y web. Nuestra labor se centra en la semántica computacional, creando sistemas inteligentes para buscar, extraer, editar, organizar y codificar información en diversos idiomas. Nuestro producto **Books Explorer** es un motor de búsqueda semántica inteligente disponible para escritorio y web, capaz de conectarse a diferentes ubicaciones donde se alojan repositorios de libros. Buscamos empresas e instituciones interesadas en implementar estos productos.

**Contact:** [CodeText@yahoo.com](mailto:CodeText@yahoo.com)  
**Website (English):** [https://www.codetext.org?Idioma=_Eng](https://www.codetext.org?Idioma=_Eng)  
**Website (Español):** [https://www.codetext.org](https://www.codetext.org)<br>
**Facebook:**          [https://www.facebook.com/CodeTextSoftware](https://www.facebook.com/CodeTextSoftware)  

---

## English RenamePdfs_isbn Information.

**RenamePdfs_isbn** is a free Windows tool that automatically renames your PDFs and EPUBs according to their ISBN: it detects the ISBN (via text, metadata, or OCR if the file has no text), searches online for the real information, and renames the file. It also saves the information in the file’s metadata and tries to add a cover as the first page if it doesn’t have one.

<p align="center">
  <img src="RenamePdfs_isbn_principal_Eng.png" alt="RenamePdfs_isbn main window (English)" width="850">
</p>

### Features

- **PDF and ePub support**: Allows selecting all the files in a folder or the files selected by the user.
- **OCR support** for text or image-only PDFs with Tesseract OCR (64-bit).
- **ISBN10 to 13 detection** in the text, in the metadata, or via OCR when the file has no extractable text.
- **Online lookup** of title, edition, year, publisher and subject using various systems such as: Google Books, Open Library, CrossRef/DOI...
- **Smart alternatives**: title recovered from PDF/EPUB metadata, content heuristics, or search by file name — renaming is only skipped when there is no reliable text, so as not to risk getting an incorrect title.
- **Configurable name format**: allows adding the book’s year, edition, and publisher in parentheses.
- **Cover insertion**: when the file has no cover, it tries to obtain an image online and inserts it as the first page.
- **Metadata writing**: they are retrieved online and saved in the file.
- **Three execution modes**: *Simulate* (performs the entire process, but does not apply the changes), *Rename* or *Execute without Renaming* (applies the metadata and inserts the cover, but does not rename the file).
- **Adjustable process priority**.
- **Customizable design** using a multitude of themes and manually, by editing `config.xml`.
- **Optional Log file** with processing details in .txt format and also in .csv format (comma-separated fields) where one file appears on each line.

### More Advantages

- **64-bit installer with Tesseract OCR included**, so there is no need to install it separately. Keep in mind that, when installing it, it offers you the option to select additional languages, besides English, in the “Additional language data” option.

### Technical Details

- **Operating System**: Windows 10/11 64bits.
- **Requires** an internet connection for online lookups.
- **Supported Languages**: English and Spanish.

### Installation

1. Download [`RenamePdfs_isbn.zip`](download/RenamePdfs_isbn.zip) (or use the update icon "↻" inside the app, which points to the same file).
2. Unzip it anywhere and run the installer — it includes Tesseract OCR (64-bit), so there's nothing else to install.
3. Run `RenamePdfs_isbn.exe`.

### Usage

1. Pick the folder (or individual files) to process with the 📁 button.
2. Choose a run mode (*simulate*, *rename*, *run without renaming*), the naming format (year/publisher), and the desired options (OCR, metadata, subject, cover, log).
3. Click **Run**. You can **Pause** or **Cancel** at any point.
4. Review the results in the grid: ISBN found, new name, status and comments. A `.csv` report and/or `.txt` log can be saved automatically.

---

## Español RenamePdfs_isbn Información.

**RenamePdfs_isbn** es una herramienta gratuita para Windows que renombra automáticamente tus PDFs y EPUBs según su ISBN: detecta el ISBN (por texto, metadatos u OCR si el archivo no tiene texto), busca online la información real y renombra el archivo. También guarda la información en los metadatos del archivo e intenta añadir una portada como primera página si no la tiene.

<p align="center">
  <img src="RenamePdfs_isbn_principal.png" alt="Ventana principal de RenamePdfs_isbn" width="850">
</p>

### Características

- **Admite archivos Pdf y ePub**: Permite seleccionar todos los archivos de una carpeta o los archivos que el usuario seleccione.
- **Soporte OCR** para Pdfs de texto o solo imagen con Tesseract OCR (64 bits).
- **Detección de ISBN10 a 13** en el texto, en los metadatos o mediante OCR cuando el archivo no tiene texto extraíble.
- **Búsqueda online** de título, edición, año, editor y tema empleando diversos sistemas como: Google Books, Open Library, CrossRef/DOI...
- **Alternativas inteligentes**: título recuperado desde metadatos del PDF/EPUB, heurística de contenido, o búsqueda por nombre de archivo —solo se omite el renombrado cuando no hay un texto fiable, para no arriesgarse a obtener un título erróneo.
- **Formato de nombre configurable**: permite añadir entre paréntesis el año del libro, la edición y el editor.
- **Inserción de portada**: cuando el archivo no tiene portada, intenta obtener una imagen online y la inserta como primera página.
- **Escritura de metadatos**: se recuperan online y se guardan en el archivo.
- **Tres modos de ejecución**: *Simular* (realiza el proceso completo, pero no aplica los cambios), *Renombrar* o *Ejecutar sin Renombrar* (aplica los metadatos e inserta la portada, pero no renombra el archivo).
- **Prioridad de proceso ajustable**.
- **Diseño personalizable** empleando multitud de temas y de forma manual, editando `config.xml`.
- **Archivo de Log opcional** con los detalles del procesamiento en formato .txt y, además, en formato .csv (campos separados por comas) donde aparece un archivo en cada línea.

### Más Ventajas

- **Instalador de 64 bits con Tesseract OCR incluido**, por lo que no hace falta instalarlo aparte. Tenga en cuenta que, al instalarlo, le ofrece la opción de seleccionar lenguajes adicionales, además del inglés, en la opción "Additional language data".

### Detalles Técnicos

- **Sistema Operativo**: Windows 10/11 64bits.
- **Requiere** conexión a internet para las búsquedas online.
- **Idiomas Soportados**: Español e Inglés.

---

<p align="center">
  © 2026 <a href="https://www.codetext.org">CodeText Software</a>. All rights reserved. / Todos los derechos reservados.
</p>
