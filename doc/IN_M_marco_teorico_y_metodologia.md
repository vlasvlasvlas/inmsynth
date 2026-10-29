# IN M · Marco Teórico, Investigación Cultural y Metodología

**Terry Riley (*In C*, 1964) y el Jingle de Marolio (2001) como Dispositivo Sonoro de Memoria Colectiva**

---

## 1. Introducción y Tesis Artística

*IN M* plantea una operación de **apropiación conceptual y desplazamiento funcional**: toma el jingle publicitario de Marolio —una de las piezas más persistentes, reconocibles y reproducidas en la historia de los medios de comunicación argentinos— y lo somete al rigor compositivo y al sistema de partitura abierta de *In C* (Terry Riley, 1964), obra fundacional del minimalismo musical contemporáneo.

La hipótesis artística central descansa sobre una paradoja productiva:

* **La repetición publicitaria** opera bajo una lógica de saturación y fijación mnemotécnica cuyo propósito es inducir el consumo y consolidar una marca en el inconsciente colectivo.
* **La repetición minimalista**, por el contrario, busca despojar al oyente del sentido utilitario del tiempo, abriendo un espacio de contemplación, micropolifonía y trance perceptivo.

Al cruzar ambos universos en un entorno de software generativo en tiempo real, *IN M* resignifica un artefacto del capitalismo de consumo rioplatense, transformándolo en un ritual sonoro meditativo, autónomo e inagotable. La obra no funciona como parodia, pastiche ni nostalgia kitsch: se inscribe explícitamente en un linaje de seis décadas de **adaptaciones autorizadas por la propia naturaleza de partitura abierta** de *In C* (ver §4), y se apoya en los marcos teóricos de la postproducción y la cultura remix (Bourriaud, Lessig, Lethem; ver §5) para legitimar su gesto como práctica artística contemporánea.

---

## 2. Marco Teórico I · Terry Riley y el Sistema *In C* (1964)

### 2.1. Ruptura con la ortodoxia del siglo XX

En 1964, el compositor estadounidense Terry Riley compuso *In C*, quebrando simultáneamente el determinismo estricto del serialismo integral europeo y la indeterminación aleatoria pura postulada por John Cage. *In C* introdujo una tercera vía: la **indeterminación controlada mediante procesos algorítmicos ejecutados por intérpretes humanos**. La monografía de referencia sobre la obra —Carl (2009), *Terry Riley's In C*, Oxford University Press, serie *Studies in Musical Genesis, Structure, and Interpretation*— reconstruye el proceso de gestación entre 1963 y 1964, el estreno en el San Francisco Tape Music Center el 4 de noviembre de 1964 bajo dirección del propio Riley, y el modo en que la obra se consolidó como piedra fundacional del minimalismo norteamericano.

Un dato relevante para el argumento de *IN M*: **el icónico pulso de corcheas constantes en Do agudo (C8) no estaba en la partitura original de Riley**. Lo aportó Steve Reich durante los ensayos de la premiere, como solución práctica para mantener a los músicos sincronizados sin director. Riley lo adoptó e incorporó formalmente a las instrucciones de ejecución (Carl, 2009; Wikipedia, "In C"). Es decir: la obra que hoy se considera canónica es ya el resultado de una **modificación colaborativa** sobre el original. *IN M* no se aparta de esa tradición mutante al proponer un pulso adaptado —en el modo Ensemble, un `MembraneSynth` grave por compás en lugar del C8 por corchea— sino que la continúa.

### 2.2. Principios compositivos de *In C*

La obra se fundamenta en un conjunto de premisas que *IN M* traslada formalmente al código de software:

1. **Partitura abierta y modularidad celular.**
   *In C* consta de 53 patrones melódico-rítmicos breves numerados secuencialmente. Ninguna voz tiene una partitura asignada de principio a fin; todos los intérpretes leen la misma secuencia común de fragmentos y la recorren en orden, pero cada uno decide independientemente cuántas veces repite cada patrón antes de avanzar al siguiente.

2. **Autonomía guiada por escucha mutua (*mutual listening*).**
   Las *performing directions* originales de Riley (reproducidas en múltiples ediciones libres y adoptadas por ensambles como Third Coast Percussion) instruyen literalmente:
   > *"The performers must listen very carefully to one another and this means occasionally even stopping and listening to the others before entering again […] It is very important that performers listen to each other. Each performer should try to stay within 2 or 3 patterns of each other."*

   Esta directiva es el núcleo conceptual de la obra: la pieza no es una secuencia predefinida sino un **sistema de interacciones** cuyo resultado emerge del comportamiento colectivo.

3. **El Pulso (*The Pulse*).**
   Un ejecutante —típicamente al piano— mantiene corcheas constantes sobre Do agudo (C8). Este pulso funciona como reloj maestro sobre el cual se desenvuelve el contrapunto. Como se señaló, es un agregado histórico de Reich al diseño original.

4. **Phasing y armonía emergente (*resultant patterns*).**
   Al superponerse células de diferentes métricas y duraciones en bucles asincrónicos, emergen patrones armónicos, batidos acústicos y melodías fantasma que jamás fueron escritas formalmente por el compositor, sino que nacen de la interacción colectiva del sistema. Este fenómeno —central en la poética minimalista y teorizado por Mertens (1983) y Potter (2000)— es el objetivo estético último de *In C* y lo que distingue a cada ejecución como irrepetible.

---

## 3. Marco Teórico II · La Canción de Marolio como Mito Cultural Popular

### 3.1. Contexto de producción y génesis (2001)

Lejos de ser un producto corporativo estandarizado, el jingle de Marolio nació a mediados de 2001 —en vísperas del colapso socioeconómico argentino— como un spot radial encargado por la cadena de supermercados mayoristas Maxiconsumo.

De acuerdo con investigaciones periodísticas y testimonios de sus protagonistas (Azcárate, 2021; El Destape, 2025; El Cronista, 2021):

* **La concepción publicitaria (Ignacio Tisser).**
  El publicista Ignacio Tisser planteó una estrategia radical para la época: frente a la publicidad convencional que apelaba a metáforas aspiracionales y ficciones de estatus, el spot de Marolio consistiría en una **enumeración literal, directa y despojada de su catálogo de productos**. Una lista de almacén convertida en métrica.

* **La producción (The Sound Studio / Osvaldo Botaya).**
  La producción se encomendó a *The Sound Studio*, productora publicitaria dirigida por Osvaldo Botaya (fallecido en 2012), responsable de imprimirle al spot una estética familiar, cálida y directa.

* **La composición musical (Gustavo y Alejandro Ridilenir).**
  La música fue compuesta por los hermanos Gustavo y Alejandro Ridilenir, músicos de profundo arraigo en el rock nacional y la música experimental argentina:
  * **Gustavo Ridilenir.** Saxofonista y flautista, integrante histórico de *Illya Kuryaki and the Valderramas* (desde el álbum *Chaco*, 1995, hasta la disolución de la banda), colaborador de *Babasónicos* (*Miami*) y miembro de *Dancing Mood*.
  * **Alejandro Ridilenir.** Guitarrista, arreglador y productor vinculado al tango de vanguardia y la música contemporánea (trabajos con Roxana Amed y Carlos Libedinsky / *Narcotango*).

* **La voz de culto (Andrea Báez).**
  La locución y el canto quedaron a cargo de Andrea Báez, figura institucional del jingle publicitario en Argentina (cortinas de *Almorzando con Mirtha Legrand*, *Bricolage*, entre otras) y corista histórica de figuras del rock argentino como *Ciro y Los Persas*, *Turf* e *Isabel Pantoja*. Grabada en una única sesión en cinta analógica, la toma original permanece inalterada en las transmisiones radiales tras más de dos décadas.

### 3.2. Arquitectura musical del jingle original

A pesar de su aparente ingenuidad popular, la pieza contiene una notable sofisticación estructural:

* **Duración atípica.** 38 segundos (18 compases), prácticamente el doble de la duración estándar de un spot radial comercial (15–20 segundos).
* **Prosodia y enumeración rítmica.** Una sucesión de 24 ítems cotidianos que van desde el desayuno hasta la cena (*"mate, café, harina y palmitos…"*). La prosodia respeta las sinalefas naturales del castellano rioplatense (por ejemplo, la conjunción *"y"* se liga a la sílaba inicial de la palabra siguiente en el compás 13: *"-clo yLen-te-jas"*, no *"-clo y Len-te-jas"*), rasgo que *IN M* preserva en la asignación silábica de sus células.
* **Modulación armónica ascendente.** La pieza comienza en **Re mayor** (D) para la primera sección de productos y modula a **Mi mayor** (E) en el compás 10 (anacrusa a *"Paté"*). Esta elevación tonal de un tono entero reactiva la atención del oyente y otorga a la frase final un clímax de brillo resolutivo.

### 3.3. Transmutación en folklore urbano y fenómeno social

Con el paso de los años, el jingle trascendió su función comercial para convertirse en un fenómeno sociocultural singular en Argentina:

* **Coreado masivo en estadios.** En diciembre de 2017, durante un concierto de *Ciro y Los Persas* en el estadio Luna Park colmado por 9.000 personas, Andrea Báez fue invitada al micrófono a entonar el jingle *a capela*: el estadio completo lo coreó unísonamente de memoria de principio a fin, legitimándolo como himno colectivo.
* **El pogo metalero.** La banda de heavy metal bizarro *Asspera* realizó una versión distorsionada de la canción, transformándola en un clásico de sus presentaciones en vivo y desatando pogos masivos en festivales y salas de conciertos.
* **Meme cultural y memoria intergeneracional.** El jingle colonizó plataformas contemporáneas (Twitter/X, TikTok, YouTube), sirviendo como código de identificación generacional, recurso pedagógico en aulas escolares y temática recurrente de festejos populares.

---

## 4. Linaje de Adaptaciones de *In C* (1964–2024)

La naturaleza misma de *In C* como partitura abierta ha generado, a lo largo de seis décadas, una tradición consolidada de versiones, adaptaciones transculturales y reinterpretaciones mediáticas. *IN M* se inscribe conscientemente en esa genealogía.

### 4.1. Grabaciones canónicas

* **Terry Riley et al., *In C* (CBS Masterworks, 1968).** Primera grabación comercial, bajo supervisión del propio Riley. Define el "sonido" característico (Buchla + instrumentos acústicos) y establece la duración típica de 40 a 70 minutos.
* **Bang on a Can, *Terry Riley: In C* (Cantaloupe Music CA-21004, 2000).** Grabada en vivo en el World Financial Center de Nueva York en 1998. Considerada por la crítica una de las interpretaciones de referencia por su balance entre fidelidad y espontaneidad.

### 4.2. Adaptaciones transculturales

* **Shanghai Film Orchestra, *In C* (Celestial Harmonies 13026, 1989).** Primera gran reinterpretación transcultural: 108 ejecutantes con instrumentos tradicionales chinos (*pipa*, *guzheng*, *sheng*) co-producida con la participación de Brian Eno y Jon Hassell. Legitima el principio de que la partitura puede ejecutarse con cualquier combinación instrumental.

* **Africa Express Presents… Terry Riley's *In C Mali* (Transgressive Records, 2015).** Grabado en octubre de 2013 en la Maison des Jeunes de Bamako, con dirección de André de Ridder y co-producción de Andi Toma (*Mouse on Mars*). Participan Damon Albarn (melódica), Brian Eno (voz), Nick Zinner (*Yeah Yeah Yeahs*), Jeff Wootton y 17 músicos malienses con *n'goni*, *kora*, *balafón* y *djembe*. Realizado para el 50º aniversario oficial de la obra, con estreno en vivo en Tate Modern (Londres). Rolling Stone lo incluyó entre los 20 mejores discos avant-garde de 2014. Es el **antecedente paradigmático** del tipo de operación que ensaya *IN M*: una tradición musical local-popular leída desde el dispositivo *In C*.

* **Adrian Utley's Guitar Orchestra, *In C* (Invada Records, 2013).** Versión para 20 guitarras eléctricas liderada por el guitarrista de *Portishead*.

### 4.3. Remix y curaduría académica

* **Grand Valley State University New Music Ensemble, *In C Remixed* (Innova 758, 2009).** Dirigido por Bill Ryan. **Doble álbum** que combina una ejecución íntegra con **18 remixes** encargados a artistas de disciplinas diversas: Mason Bates, Glenn Kotche (*Wilco*), Zoë Keating, Jad Abumrad (*Radiolab*), Nico Muhly, DJ Spooky, David Lang, Jack Dangers (*Meat Beat Manifesto*), entre otros. Reseñado positivamente por el *Washington Post*, que lo incluyó en su listado de los diez mejores discos clásicos de 2009. **Es la referencia más fuerte para legitimar académicamente proyectos como *IN M***: una universidad convirtiendo *In C* en plataforma oficial de reescritura y remix.

### 4.4. Precursores web y software generativo

El linaje directo de *IN M* en términos técnicos y conceptuales se encuentra en dos implementaciones web preexistentes:

* **Tero Parviainen ("teropa"), *In C* interactivo (2016–2017).** Disponible en `teropa.info/in-c/` y documentado en el ensayo "A Musical Possibility Space" (`teropa.info/blog/2017/01/23/terry-rileys-in-c.html`). Implementa un ensamble de **cinco bots autónomos que el usuario puede empujar o detener** mediante controles gráficos: es exactamente el modelo de interacción Humano+Auto que *IN M* adopta y extiende con la lógica de "contagio de impulso" y la paleta de timbres editable. Técnicamente usa Angular + Web Audio API crudo (no Tone.js). Código abierto en GitHub.

* **Jake Albaugh, *In C* en CodePen (2016).** Implementación compacta con Tone.js (`codepen.io/jakealbaugh/pen/NAjdLY`). Es el precursor directo del stack técnico de *IN M* y demuestra la viabilidad de la Web Audio API como entorno de ejecución para *In C*.

* **Brian Eno y Peter Chilvers (Opal Limited).** La serie de *generative music apps* para iOS —*Bloom* (2008), *Trope* (2009), *Scape* (2012), *Reflection* (2017)— constituye el marco conceptual más próximo al de *IN M* en lo relativo a **obras-sistema**: piezas donde el compositor diseña reglas de interacción y el oyente/usuario completa la ejecución. *Scape* es particularmente afín al pensar los elementos como "entidades que reaccionan entre sí".

---

## 5. Marco Teórico III · Apropiación Conceptual y Cultura del Remix

El gesto de *IN M* —tomar un objeto cultural preexistente (el jingle) y someterlo a un dispositivo compositivo ajeno (el sistema *In C*)— se enmarca en una tradición teórica bien establecida de reflexiones sobre la apropiación como práctica artística legítima.

* **Bourriaud, Nicolas (2002 / 2005).** *Postproduction: Culture as Screenplay — How Art Reprograms the World.* Lukas & Sternberg, Nueva York. ISBN 0971119309 (2ª ed. 2005, ISBN 9780974568898). Edición original francesa: *Postproduction — La culture comme scénario* (Les presses du réel, 2004). Bourriaud sostiene que el artista contemporáneo opera "a partir de obras preexistentes […] respondiendo al caos proliferante de la cultura global", y propone pensar cada obra como un **departamento alquilado** que el nuevo autor habita, redecora y utiliza (apoyándose en Michel de Certeau). *IN M* ejecuta literalmente ese programa: el jingle de Marolio es el departamento, el sistema de Riley es la forma de habitarlo.

* **Lessig, Lawrence (2008).** *Remix: Making Art and Commerce Thrive in the Hybrid Economy.* The Penguin Press, Nueva York. ISBN 978-1-59420-172-1. Libro publicado bajo licencia Creative Commons BY-NC —coherente con la licencia **CC BY-SA 4.0** adoptada por *IN M*—. Lessig teoriza la *read-write culture* como el régimen semiótico contemporáneo, en el que la circulación de los objetos culturales incluye necesariamente su reinscripción, cita, remezcla y transformación. El código de *IN M* es software libre precisamente para habilitar el próximo eslabón de esa cadena.

* **Lethem, Jonathan (2007).** *"The Ecstasy of Influence: A Plagiarism".* *Harper's Magazine*, febrero 2007, pp. 59–71 (posteriormente ampliado como libro homónimo, Doubleday, 2011). Ensayo construido en su totalidad como un tejido de citas no marcadas de otros autores, revelado al final del texto. Operación formal que ilumina el estatuto siempre citacional de la escritura (y, por extensión, de toda producción cultural). *IN M* opera en ese mismo espíritu: cada célula es cita exacta de la partitura original, pero el ensamblaje algorítmico es nuevo.

---

## 6. Metodología de Implementación · De la Partitura al Algoritmo

Para construir *IN M*, el material original fue descompuesto, analizado y reconstruido como un sistema computacional generativo y autónomo.

```
       Partitura Original (Marolio, 2001)
                     │
                     ▼
       Deconstrucción en 24 Células + 2 Silencios
                     │
                     ▼
       Motor Generativo de Escucha Mutua (In C)
       ├── Phasing rítmico fijo por voz (0, 1, 2 corcheas)
       ├── Restricción de dispersión (máx. 4 células)
       ├── Dinámica adaptativa por densidad
       ├── Variación de registro por octavación
       └── Algoritmo de contagio e impulso
                     │
                     ▼
       Síntesis Procedural en Tiempo Real (Tone.js)
       ├── Voces estéreo (L / C / R)
       ├── Catálogo de 18 timbres YAML (FM / AM / Sustractiva + Cuerdas)
       └── Visualización: Mezcla de color aditiva en góndola
```

### 6.1. Deconstrucción y modularización celular

Se realizó una transcripción nota a nota del jingle (`doc/IN_M_transcripcion_partitura.md`), segmentando la melodía en **24 células rítmico-melódicas** y **2 células de silencio** ($\Sigma_1, \Sigma_2$), distribuidas en tres regiones formales:

1. **Intro (células 1 a 4 · Re mayor).** El enunciado melódico preliminar ("*Marolio le da sabor a tu vida…*").
2. **Productos D (células 5 a 12 · Re mayor).** La primera mitad de la enumeración ("*Mate, Café, Harina y Palmitos…*").
3. **Productos E (células 13 a 20 · Mi mayor).** La modulación tonal ("*Paté, Caballa, Arroz y Arvejas, Sardinas y Atún, Choclo y Lentejas*").
4. **Outro (células 21 a 24 · Mi mayor).** Cierre y resolución ("*Marolio le da sabor a tu vida…*").

Cada célula preserva la prosodia silábica original —incluidas sinalefas como *"yLen-"* en la frontera entre células 19 y 20— pero funciona como un bucle cerrado capaz de autosostenerse infinitamente.

### 6.2. Ensamble de intérpretes virtuales y algoritmo de escucha mutua

La pieza prescinde de un secuenciador lineal. En su lugar, tres intérpretes sintéticos recorren la partitura de manera concurrente:

* **Músico 1** · izquierda (pan −55%) · color **rojo**.
* **Músico 2** · centro (pan 0%) · color **verde**.
* **Músico 3** · derecha (pan +55%) · color **azul**.

Cada intérprete evalúa, en cada final de ciclo, las siguientes reglas algorítmicas de escucha mutua —todas derivadas directamente de las *performing directions* de Riley o inferidas de la práctica histórica de la obra—:

1. **Phasing rítmico estructural.** Cada voz ingresa con un offset fijo de corcheas (0, 1 y 2 corcheas de desfase), generando el característico *shimmer* polirrítmico rileyano cuando dos o tres voces tocan la misma célula.
2. **Límite de dispersión.** Ninguna voz puede alejarse a más de 4 células de distancia del integrante más retrasado. Si una voz corre el riesgo de quebrar el ensamble, se fuerza a esperar en loop. Riley especifica "2 or 3 patterns"; *IN M* amplía ligeramente el margen a 4 para habilitar mayor libertad individual sin perder cohesión.
3. **Decisión probabilística y paciencia.** Cada músico posee un umbral de repeticiones mínimas antes de calcular su probabilidad de avance. A mayor permanencia en una célula, mayor la propensión al cambio.
4. **Contagio de liderazgo.** Cuando una voz da el salto a una célula avanzada, emite un pulso de influencia que eleva temporalmente (+0.35) la probabilidad de avance de sus compañeras durante los 6 compases subsiguientes, emulando la dinámica orgánica de los ensambles humanos ("arrastre de sección").
5. **Respiración y fatiga grupal.** Si un músico toca ininterrumpidamente durante más de 10 compases, o si varias voces coinciden en unísono prolongado, el algoritmo gatilla pausas deliberadas de 2 a 4 compases para oxigenar la masa contrapuntística. Esta regla implementa literalmente la directiva de Riley: *"occasionally even stopping and listening to the others before entering again"*.
6. **Dinámica adaptativa por densidad.**
   * 3 voces activas simultáneas: factor de ganancia $0.80\times$ (textura calma).
   * 2 voces activas: $0.95\times$.
   * 1 voz solista (las otras descansan): $1.12\times$ para sostener el espacio sonoro.
7. **Variación de registro por octavación de frase.** En consonancia con las directivas originales de *In C* (donde Riley prescribe que los patrones pueden ejecutarse una octava arriba o abajo para dar cuerpo y variedad polifónica), el ensamble alterna de registro orgánicamente:
   * **Octava baja (`8vb`, ~25%).** Actúa como bajo o contracanto cálido durante 1 o 2 ciclos completos del patrón.
   * **Octava alta (`8va`, ~9%).** Limitada exclusivamente a células de registro medio/grave (octava $\le 4$) y con ganancia atenuada para aportar brillo y aire sin estridencia ni saturación auditiva.

### 6.3. Interacción humana: tres regímenes de ejecución

*IN M* ofrece tres regímenes complementarios de ejecución, que corresponden a lecturas distintas del dispositivo:

* **Canción.** Reproducción lineal de los 18 compases con acompañamiento armónico (acordes + bajo sub-pad) y pulso. Es la **referencia fija**: la obra tal como fue escrita.
* **Auto.** El algoritmo decide por los tres intérpretes. Cada ejecución es irrepetible. Es la lectura **más fiel al espíritu de Riley**: música-sistema que se despliega sin dirección central.
* **Humano.** El usuario funciona como director/co-ejecutante: con las teclas `1 / 2 / 3` empuja a cada músico a avanzar a la próxima célula. Esta modalidad traduce al teclado de computadora el gesto físico del intérprete de *In C* que decide, mirando y escuchando a los otros, cuándo avanzar. Convive con las decisiones autónomas de las voces en modo mixto: se puede empujar a una voz mientras las otras siguen deliberando algorítmicamente.

### 6.4. Motor de audio y síntesis procedural pura

A diferencia de los enfoques comerciales basados en inteligencia artificial de caja negra (*text-to-audio*) o en el disparo de *samples* pregrabados de audio digital, *IN M* utiliza **síntesis procedural pura calculada en tiempo real** mediante la Web Audio API y la librería Tone.js:

* Osciladores modelados matemáticamente: ondas senoidales, triangulares, cuadradas, pulsadas y formas de onda ricas multi-oscilador (`fatsawtooth`, `fattriangle`, `fatsine`).
* Síntesis por Modulación de Frecuencia (FM) y Modulación de Amplitud (AM) para emular timbres clásicos: Marimba, DX7, Rhodes, Campanas, Moog Lead, ARP Strings, TB-303 Acid, Juno Pad.
* **Paleta orquestal expandida (noviembre 2025).** Cuatro nuevos timbres de cuerda —*Cuerdas ensemble*, *Cello*, *Violín pad*, *Cuerdas cristal*— con attacks de 0.9 a 1.8 s y releases de 2.2 a 4.0 s, ampliando el rango expresivo del ensamble hacia texturas de masa orquestal sostenida. El motor eleva en consecuencia `maxPolyphony` por voz a 16 para absorber el solapamiento de releases largos.
* Matriz de modulación editable en vivo desde [`timbres.yaml`](../timbres.yaml) (18 timbres totales).
* Procesamiento estéreo integral: bus de retardo de realimentación sincrónico al tempo maestro (`FeedbackDelay` con subdivisión seleccionable), reverberación algorítmica (`Reverb`) y etapa final de limitación de señal (`Limiter`).

### 6.5. Interfaz como partitura gráfica y síntesis cromática

La interfaz visual no es una mera consola de control: es una **partitura gráfica viva** dispuesta como una góndola de almacén. Cuando dos o más músicos se encuentran en la misma célula melódica, los colores asignados a sus canales se combinan dinámicamente mediante mezcla aditiva (*screen blend*):

$$\text{Rojo} + \text{Verde} = \text{Amarillo}$$
$$\text{Rojo} + \text{Azul} = \text{Magenta}$$
$$\text{Verde} + \text{Azul} = \text{Cian}$$
$$\text{Rojo} + \text{Verde} + \text{Azul} = \text{Blanco cálido}$$

La interfaz traduce visualmente el principio musical de *In C*: la superposición de voces no produce confusión, sino síntesis luminosa y resonancia armónica. Las variaciones de registro (`8va` / `8vb`) se señalizan en tiempo real en la tarjeta de cada músico, permitiendo al oyente seguir las decisiones del algoritmo tanto por el oído como por la vista.

---

## 7. Síntesis Crítica · *IN M* dentro del Linaje

A la luz del linaje reconstruido en §4, *IN M* puede leerse como la convergencia de **tres tradiciones**:

1. **La tradición de las adaptaciones transculturales de *In C*** (Shanghai 1989, Mali 2015, Portishead 2013), que establece que la partitura puede acoger cualquier material tímbrico, instrumental o cultural sin perder su identidad formal.
2. **La tradición del remix curado académicamente** (GVSU *In C Remixed* 2009), que legitima el gesto de intervenir la obra con material contemporáneo y de otras procedencias estéticas.
3. **La tradición del software generativo web** (Parviainen 2017, Albaugh 2016, Eno/Chilvers 2008–2017), que traslada el dispositivo al navegador y convierte al oyente en co-ejecutante.

*IN M* aporta a esta genealogía dos novedades específicas:

* **Material fuente de origen publicitario popular rioplatense.** Hasta donde la investigación bibliográfica permite afirmar, no existen adaptaciones previas de *In C* que tomen como material celular una obra del *advertising folklore* latinoamericano. Esta elección tensa productivamente la escala tímbrica aceptada por el linaje (música tradicional china, música maliense, rock, electrónica experimental) con un registro culturalmente estigmatizado como "menor" (el jingle comercial), demostrando que la operación formal del dispositivo *In C* opera con independencia del prestigio del material.
* **Factores "humanos" explícitamente modelados.** Los algoritmos de contagio, lead-in dinámico, dinámica adaptativa por densidad y variación por arco de obra incorporan al sistema reglas que, en las ejecuciones humanas de *In C*, dependen de la intuición del ensamble. *IN M* los explicita y los hace parametrizables, aportando a la discusión sobre **qué cosas del "estar juntos" musical son automatizables y cuáles no**.

---

## 8. Conclusión · La Obra como Dispositivo Crítico

*IN M* no opera como parodia ni como nostalgia *kitsch*, sino como un **ejercicio de arqueología de los medios y desvío deconstructivo**. Al desacelerar, expandir y abrir el jingle publicitario de Marolio bajo los mecanismos de Terry Riley, el proyecto desplaza a la melodía de su función mercantil original. Despojada de la urgencia de vender, la pieza deja al descubierto su lógica constructiva: una letanía de productos cotidianos convertida en pura materia rítmico-melódica, articulada a través de un sistema algorítmico que dialoga con la memoria sonora compartida.

Si Riley —ayudado por Reich en el pulso— demostró en 1964 que una partitura abierta podía dar lugar a una tradición de seis décadas de reinterpretaciones vivientes, y si Africa Express demostró en 2015 que esa partitura podía recibir el aire de Bamako sin dejar de ser *In C*, *IN M* propone que también puede recibir —con el mismo rigor y la misma apertura— el aire del almacén argentino.

---

## 9. Referencias y Fuentes Consultadas

### 9.1. Sobre *In C* y minimalismo

1. **Carl, Robert (2009).** *Terry Riley's In C.* Oxford University Press, serie *Studies in Musical Genesis, Structure, and Interpretation*. 160 pp. ISBN 978-0-19-532528-7. [Google Books](https://books.google.com/books/about/Terry_Riley_s_In_C.html?id=xXaFqd5W9X4C) · Entrevista con el autor en [New Music USA](https://newmusicusa.org/nmbx/a-conversation-with-robert-carl-author-of-terry-rileys-in-c/).
2. **Potter, Keith (2011).** Reseña de Carl (2009) en *Music & Letters* 92(1): 171–174. DOI: `10.1093/ml/gcq097`. [Oxford Academic](https://academic.oup.com/ml/article-abstract/92/1/171/1244516).
3. **Mertens, Wim (1983).** *American Minimal Music: La Monte Young, Terry Riley, Steve Reich, Philip Glass.* Kahn & Averill, Londres.
4. **Potter, Keith (2000).** *Four Musical Minimalists: La Monte Young, Terry Riley, Steve Reich, Philip Glass.* Cambridge University Press.
5. **Riley, Terry (1964).** *In C.* Partitura y *performing directions* para ensamble abierto. Ediciones libres disponibles vía [Third Coast Percussion (PDF)](https://thirdcoastpercussion.com/downloads/2015/04/Terry-Riley-In-C-concert2.pdf) y [Music Institute (PDF)](https://www.musicinst.org/sites/default/files/attachments/In%20C%20Instructions%20for%20Beginners.pdf).

### 9.2. Grabaciones y adaptaciones de *In C*

6. **Riley, Terry et al. (1968).** *In C.* CBS Masterworks MS-7178.
7. **Shanghai Film Orchestra (1989).** *In C.* Celestial Harmonies 13026.
8. **Bang on a Can (2000).** *Terry Riley: In C.* Cantaloupe Music CA-21004.
9. **Grand Valley State University New Music Ensemble (2009).** *In C Remixed.* Innova 758. Dirección: Bill Ryan. Reseña en [All About Jazz](https://www.allaboutjazz.com/grand-valley-state-university-new-music-ensemble-in-c-remixed-by-john-kelman/).
10. **Adrian Utley's Guitar Orchestra (2013).** *In C.* Invada Records.
11. **Africa Express (2015).** *Africa Express Presents… Terry Riley's In C Mali.* Transgressive Records TRANS198. Dirección: André de Ridder. Grabado en Maison des Jeunes, Bamako, octubre de 2013. [Wikipedia](https://en.wikipedia.org/wiki/Africa_Express_Presents..._Terry_Riley%27s_In_C_Mali).

### 9.3. Software y precursores web generativos

12. **Parviainen, Tero (2017).** *"A Musical Possibility Space"* y aplicación web interactiva. [teropa.info/in-c](https://teropa.info/in-c/) · [blog](https://teropa.info/blog/2017/01/23/terry-rileys-in-c.html) · [GitHub](https://github.com/teropa/in-c).
13. **Albaugh, Jake (2016).** *In C* en CodePen. [codepen.io/jakealbaugh/pen/NAjdLY](https://codepen.io/jakealbaugh/pen/NAjdLY).
14. **Chilvers, Peter & Eno, Brian.** *Bloom* (2008), *Trope* (2009), *Scape* (2012), *Reflection* (2017). Opal Limited / Warp Records. Entrevista con Chilvers en [Tape Op](https://tapeop.com/interviews/137/peter-chilvers).

### 9.4. Apropiación conceptual y cultura del remix

15. **Bourriaud, Nicolas (2002, 2005).** *Postproduction: Culture as Screenplay — How Art Reprograms the World.* Lukas & Sternberg, Nueva York. 2ª ed. 2005, ISBN 9780974568898. Edición francesa: Les presses du réel, 2004.
16. **Lessig, Lawrence (2008).** *Remix: Making Art and Commerce Thrive in the Hybrid Economy.* The Penguin Press, Nueva York. ISBN 978-1-59420-172-1. Publicado bajo CC BY-NC.
17. **Lethem, Jonathan (2007).** *"The Ecstasy of Influence: A Plagiarism".* *Harper's Magazine*, febrero de 2007, pp. 59–71. [Harper's archivo](https://harpers.org/archive/2007/02/the-ecstasy-of-influence/). Versión ampliada en libro homónimo, Doubleday, 2011.

### 9.5. Sobre el jingle de Marolio

18. **Azcárate, Paz (31 de mayo de 2021).** *"A 20 años del lanzamiento: la historia del jingle de Marolio, contada por sus protagonistas"*. *La Nación*, Sección Espectáculos.
19. **El Destape (8 de enero de 2025).** *"Están detrás de un jingle icónico y 24 años después develan todos sus secretos: la historia de Marolio"*.
20. **El Cronista (18 de junio de 2021).** *"La historia del jingle de Marolio: la idea de un amigo que se viralizó en todos lados"*.

### 9.6. Documentación interna del proyecto

21. [`doc/IN_M_transcripcion_partitura.md`](./IN_M_transcripcion_partitura.md). Transcripción formal y rítmica compás a compás.
22. [`doc/IN_M_analisis_v1.md`](./IN_M_analisis_v1.md). Análisis morfológico preliminar.
23. [`doc/IN_M_analisis_v2.md`](./IN_M_analisis_v2.md). Deliberación del comité de expertos en HCI, composición y estudios culturales.
24. [`timbres.yaml`](../timbres.yaml). Catálogo editable de los 18 timbres sintetizados.
