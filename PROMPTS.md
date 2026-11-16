# Prompts

Copia, pega en Claude Code y cambia lo que está entre [corchetes]. Van en orden: cada uno es un paso.
Copy, paste into Claude Code and swap everything in [brackets]. They go in order: one per step.

---

## 1. La idea en una pregunta / The idea as a question

**ES**
```
/simulab Quiero un lab sobre [cómo pescar sin que se rompa el hilo].
Antes de construir nada, conviértelo en una sola pregunta con una pieza que se mueve y un número que la gente pueda comprobar.
Dame 3 opciones, dime cuál es la parte que más confunde a un principiante y recomiéndame una.
```

**EN**
```
/simulab I want a lab about [how to fish without snapping the line].
Before building anything, turn it into one question with one moving part and one number people can check.
Give me 3 options, tell me which part confuses beginners most and recommend one.
```

## 2. Los números con fuente / The numbers with sources

**ES**
```
Investiga los números reales de [un carrete de spinning: el freno (drag) frente a la resistencia del hilo].
Dame una tabla: valor, unidad, fuente con link, y si es dato o supuesto.
Si no encuentras fuente para un número, márcalo como supuesto. No inventes fuentes.
Con esa tabla escribe la nota del modelo para demo.json.
```

**EN**
```
Research the real numbers for [a spinning reel: drag setting versus line strength].
Give me a table: value, unit, source with a link, and whether it is data or an assumption.
If a number has no source, mark it as an assumption. Do not invent sources.
Use the table to write the model note for demo.json.
```

## 3. El modelo y el lab / The model and the lab

**ES**
```
/simulab Construye el lab "[¿Por qué se rompe el hilo cuando el pez jala?]" en labs/[lab01-pesca].
Objetos, hechos con código en cm reales: [una caña, un carrete con su perilla de freno, el hilo y un pez].
Escribe primero model.js como funciones puras de una entrada: [la fuerza del pez en kg].
Revisa una cuenta a mano y enséñamela.
Todo lo que se ve (piezas, paneles, etiquetas y veredicto) lee de ese modelo.
Si falta un objeto en CATALOGO.md, créalo en assets/[pesca].js y agrégalo al catálogo.
```

**EN**
```
/simulab Build the lab "[Why does the line snap when the fish pulls?]" in labs/[lab01-fishing].
Objects, built in code in real cm: [a rod, a reel with its drag knob, the line and a fish].
Write model.js first as pure functions of one input: [the fish's pull in kg].
Check one value by hand and show me.
Everything on screen (parts, panels, labels, verdict) reads from that model.
If an object is missing from CATALOGO.md, create it in assets/[fishing].js and add it to the catalogue.
```

## 4. Capítulos por contraste / Chapters by contrast

**ES**
```
Divide el lab en 3 capítulos: [el freno muy apretado (se rompe el hilo)], [el freno muy suelto (el pez se lleva todo el hilo)] y [el freno justo].
Una idea por capítulo, con una tarjeta de 2 líneas que explique qué pasa.
Si un proceso es largo, adelántalo y dilo en pantalla (×N).
Cierra con una sola frase: [el freno cede antes de que el hilo se rompa].
```

**EN**
```
Split the lab into 3 chapters: [drag too tight (the line snaps)], [drag too loose (the fish strips the spool)] and [drag just right].
One idea per chapter, with a 2-line card that explains what happens.
If a process is long, speed it up and say so on screen (×N).
End with one sentence: [the drag gives before the line breaks].
```

## 5. Déjalo romperse / Let them break it

**ES**
```
Agrega un modo práctica: una perilla para [el freno, de 0 a 10 kg] y una tecla [J] para [que el pez jale].
Cada intento termina con un veredicto y una línea de por qué.
```

**EN**
```
Add a practice mode: a knob for [the drag, 0 to 10 kg] and a key [J] to [make the fish pull].
Every attempt ends with a verdict and one line on why.
```

## 6. Revísalo como crítico / Review it like a critic

**ES**
```
Antes de enseñarme nada, saca una hoja de contacto con tools/stills.mjs (un cuadro por capítulo) y revísala:
piezas encimadas, etiquetas que tapan lo que nombran, números que no cuadran con lo que se ve, textos que no se leen.
Arregla cada problema con un número en el código, nunca moviendo la cámara para esconderlo.
Dime qué revisaste, qué arreglaste y enséñame la hoja.
```

**EN**
```
Before showing me anything, make a contact sheet with tools/stills.mjs (one frame per chapter) and read it:
overlapping parts, labels covering what they name, numbers that disagree with the picture, unreadable text.
Fix each problem with a number in the code, never by moving the camera to hide it.
Tell me what you checked, what you fixed and show me the sheet.
```

## 7. El video / The video

**ES**
```
Saca primero el preview con tools/video.sh --preview y revísalo.
Si está limpio, saca el video final y la portada con tools/cover.mjs.
```

**EN**
```
Render the preview first with tools/video.sh --preview and review it.
If it is clean, render the final video and the cover with tools/cover.mjs.
```

---

## Ideas por nicho / Ideas by niche

Cada una ya tiene su pieza que se mueve y su número. / Each one already has its moving part and its number.

| Nicho / Niche | Pregunta / Question | Pieza y número / Part and number |
|---|---|---|
| Café / Coffee | ¿Por qué el espresso sale agrio o amargo? | La molienda; segundos para 36 g |
| Pesca / Fishing | ¿Por qué se rompe el hilo? | El freno del carrete; kg contra la resistencia del hilo |
| Gym | ¿Por qué el curl pesa más con el codo a 90°? | El brazo como palanca; torque en el codo |
| Finanzas / Finance | ¿Cuánto cambia empezar a ahorrar 5 años antes? | Monedas cayendo en frascos; el total al final |
| Cocina / Cooking | ¿Por qué el pan sube en el horno? | Burbujas de gas en la masa; temperatura |
| Autos / Cars | ¿Cómo gira cada rueda distinto en una curva? | El diferencial; vueltas de cada rueda |
| Música / Music | ¿Cómo suena una guitarra eléctrica? | La cuerda sobre la pastilla; frecuencia en Hz |
| Casa / Home | ¿Cómo sabe el tanque del baño cuándo dejar de llenarse? | El flotador y la válvula; nivel del agua |
| Bici / Bike | ¿Por qué cambiar de velocidad facilita la subida? | Los piñones; vueltas del pedal por vuelta de rueda |
| Ciberseguridad / Security | ¿Qué pasa entre la URL y el candado? | Paquetes en una banda; los 4 pasos DNS, TCP, TLS, HTTP |
| Biología / Biology | ¿Cómo llega el oxígeno a tu músculo? | Glóbulos en un tubo; saturación en % |
| Tu trabajo / Your job | [El proceso que más te cuesta explicar] | [La pieza que se mueve]; [el número que importa] |
