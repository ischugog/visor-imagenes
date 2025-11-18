En este archivo HTML5, cada línea cumple una función específica: 
- <!DOCTYPE html> declara el documento como HTML5, activando reglas modernas del navegador. 
- <html lang=es> abre la raíz, especificando español para accesibilidad y motores de búsqueda.
- <meta charset=UTF-8> garantiza que caracteres especiales se muestren correctamente. 
- <meta name=viewport content=width=device-width, initial-scale=1.0> adapta la vista móvil.
- - <title>Visor de Imágenes</title> fija el título en la pestaña. 
- <style>…</style> define estilos internos: fuente Arial, centrado, bordes en la imagen, fondo claro 
–todo CSS puro. - <h2>Selecciona una imagen</h2> muestra un encabezado descriptivo. 
- <input type=file id=myImage accept=image/ > crea un selector de archivos, limitado a imágenes; id lo identifica para JavaScript.
- - <img id=myFile alt=… src= style=display:none;> reserva espacio para la imagen; se oculta al inicio.
  - - <script> inicia JavaScript: – const inputFile = document.getElementById(myImage); obtiene el input. 
    – const myFile = document.getElementById(myFile); obtiene la etiqueta de imagen.
    – inputFile.addEventListener(change, function() { … }) detecta cuando se elige archivo.
    – const file = this.files[0]; captura la imagen seleccionada.
    – new FileReader() convierte la imagen a cadena base64 (data URL).
    – reader.onload = … myFile.src = e.target.result; asigna esa cadena como fuente de la imagen.
    – myFile.style.display = block; la hace visible.
    - </body> y </html> cierran el documento. HTML5 da la estructura fija; CSS hace que 
    El flujo completo es: usuario selecciona imagen → JavaScript detecta el cambio
    → convierte el archivo a cadena legible → la asigna a la etiqueta [image]
    → la imagen se muestra. Resumen técnico: HTML5 proporciona la estructura semántica y el input seguro;
    CSS controla la apariencia y layout; JavaScript maneja el evento, la conversión binaria a texto y el renderizado dinámico.
    Todo corre en el cliente, sin servidor, sin latencia. Fin.
