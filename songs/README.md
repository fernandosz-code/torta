# Formato de las canciones

Cada canción es un archivo de texto plano `.txt` guardado en esta carpeta,
con los acordes escritos arriba de la letra (igual que se hace a mano),
alineados con espacios.

## Cómo migrar una canción desde Google Docs

1. Abrí el Google Doc de la canción.
2. Seleccioná todo el texto y copialo tal cual está (acordes arriba de la
   letra, alineados con espacios).
3. Pegalo en un archivo nuevo dentro de esta carpeta, por ejemplo
   `nombre-de-la-cancion.txt`. Revisá que los acordes sigan alineados con
   la letra (si se desalinean, es porque Google Docs usó tabs en vez de
   espacios: reemplazalos por espacios).
4. Agregá una entrada en `index.json` con el título que se va a mostrar en
   la lista y el nombre del archivo:

   ```json
   { "title": "Nombre de la Canción", "file": "nombre-de-la-cancion.txt" }
   ```

5. Guardá, hacé commit y push (o subí los cambios por PR).

## Reglas del formato

- Codificación UTF-8.
- Usar espacios, no tabs, para alinear los acordes con la letra.
- El nombre del archivo no necesita coincidir con el título, pero conviene
  que sea parecido y sin espacios ni tildes (ej: `un-lugar-en-el-mundo.txt`).
- Ver `cancion-de-ejemplo.txt` como referencia de formato.
