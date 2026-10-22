# Formato de las canciones

Cada canción es un archivo de texto plano `.txt` guardado en esta carpeta,
con los acordes escritos arriba de la letra (igual que se hace a mano),
alineados con espacios.

La página `canciones.html` lee directamente esta carpeta desde GitHub: con
subir el `.txt` acá alcanza, no hace falta editar ningún índice aparte. El
título que se muestra en la lista es la **primera línea** del archivo.

## Cómo migrar una canción desde Google Docs

1. Abrí el Google Doc de la canción.
2. Seleccioná todo el texto y copialo tal cual está (acordes arriba de la
   letra, alineados con espacios).
3. Pegalo en un archivo nuevo dentro de esta carpeta, por ejemplo
   `nombre-de-la-cancion.txt`. La primera línea del archivo tiene que ser
   el título tal como querés que aparezca en la lista (ej: "Un Lugar en el
   Mundo").
4. Revisá que los acordes sigan alineados con la letra (si se desalinean,
   es porque Google Docs usó tabs en vez de espacios: reemplazalos por
   espacios).
5. Guardá, hacé commit y push (o subí los cambios por PR). En cuanto el
   archivo esté en `main`, aparece solo en la lista de `canciones.html`.

## Reglas del formato

- Codificación UTF-8.
- La primera línea del archivo es el título que se muestra en la lista.
- Usar espacios, no tabs, para alinear los acordes con la letra.
- El nombre del archivo no necesita coincidir con el título, pero conviene
  que sea parecido y sin espacios ni tildes (ej: `un-lugar-en-el-mundo.txt`).

## Diagramas de acordes

En el visor, cada acorde (no toda la línea, cada palabra tipo `Em`, `F#m`,
`Am/G`, etc.) es clickeable y muestra un diagrama de cómo tocarlo. Los
diagramas salen de `../acordes.js`, un diccionario chico con solo los
acordes que ya se usan en las canciones subidas.

Si agregás una canción con un acorde nuevo que no está en ese diccionario,
no pasa nada grave: el acorde se sigue resaltando y es clickeable, pero al
tocarlo avisa que todavía no tiene diagrama. Para agregarlo, pedile a
Claude que regenere `acordes.js` incluyendo el acorde nuevo (usa como
fuente `chords-db`, de dominio MIT, así que es gratis y no depende de
ningún servicio externo).
