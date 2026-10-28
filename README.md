# IN M

**Marolio como partitura abierta · Sistema Riley**

IN M toma el jingle de Marolio y lo transforma en una obra interactiva y
generativa inspirada en *In C* (Terry Riley, 1964).

La partitura (24 células + 2 células de silencio, 18 compases, modulación
de Re mayor a Mi mayor) está transcripta nota a nota desde la partitura
original (`doc/partitura.png`). Sobre esa base, tres músicos virtuales la
recorren a su propio ritmo, escuchándose entre sí, y cada ejecución suena
distinta.

- Demo: <https://vlasvlasvlas.github.io/inmsynth/>
- Repo: <https://github.com/vlasvlasvlas/inmsynth>
- **Marco Teórico & Metodología:** [`doc/IN_M_marco_teorico_y_metodologia.md`](./doc/IN_M_marco_teorico_y_metodologia.md) (Terry Riley, *In C* y la historia sociocultural del jingle de Marolio)

---

## Correrlo

Es un `index.html` autocontenido con Tone.js y js-yaml por CDN.
Necesita servidor local para que el navegador haga `fetch` del YAML de timbres.

```bash
cd inmsynth
python3 -m http.server 8000
# http://localhost:8000
```

Si lo abrís con `file://` igual funciona, pero cae al fallback embebido de
8 timbres (sin los 6 clásicos adicionales del YAML).

---

## Modos

### Canción
Toca los 18 compases exactos con melodía + armonía (acordes + bajo sub-pad
continuo) + pulso. Es la referencia: la obra tal cual la escribí en la
transcripción.

### Auto
Tres intérpretes virtuales recorren las 24 células guiados por un algoritmo
de escucha mutua inspirado en *In C*. Cada uno con su propia paciencia,
phasing rítmico, pausas y dinámica adaptativa. Cada ejecución es distinta.

### Humano
Vos dirigís. `1` / `2` / `3` (o los botones **Avanzar** de cada card) le
dicen a cada músico que pase a la siguiente célula.

---

## Controles por músico (modos Auto / Humano)

Cada card tiene:

- **Timbre** (dropdown) — elegís el sonido entre los definidos en
  [`timbres.yaml`](./timbres.yaml). Cambia en vivo sin reiniciar.
- **Auto / Manual** — quién decide los avances. En Auto el algoritmo. En
  Manual sólo vos.
- **Pausar** — pausa el avance: el músico sigue tocando el mismo patrón
  en loop hasta que lo destildes. Útil para generar un ostinato o pedal
  mientras los otros rotan.
- **Respirar** — pausa puntual de 2 compases. Vuelve solo.
- **Avanzar** — manda el salto a la siguiente célula. Cuantizado al próximo
  beat (negra) para que no corte frases a la mitad, pero sin esperar al
  ciclo entero. Prácticamente inmediato.

Espacialización estéreo:

- Músico 1 → izquierda (−55%) · color **rojo**
- Músico 2 → centro · color **verde**
- Músico 3 → derecha (+55%) · color **azul índigo**

Los colores identifican a cada voz en la góndola. Cuando dos músicos
coinciden en la misma célula, los colores se mezclan por **screen blend**
(rojo + verde = amarillo, rojo + azul = magenta, verde + azul = cyan).
Los tres juntos → blanco cálido.

---

## Controles globales (panel inferior)

Agrupados en 3 cards:

**Tiempo & Estado**
- *Tempo* — BPM del transport (70–160).
- *Reps mín.* — repeticiones mínimas que cada músico sostiene una célula
  antes de considerar avanzar. Más alto = la obra evoluciona más lenta.
- Presets rápidos: *Meditativo* (16 reps · ~15 min · ambient) /
  *Clásico* (8 reps · ~6 min · estilo In C) / *Ágil* (4 reps · ~2.5 min).

**Espacio & FX**
- *Reverb* 0–100% — en 0 queda apagado.
- *Delay* 0–100% — en 0 queda apagado.
- División rítmica del delay (dropdown): `½ · ¼· · ¼ · ⅛· · ⅛ · 1/16 · 1/8T`.
  Sincronizada al tempo del transport — si cambiás el BPM, el delay se adapta.

**Capas Sonoras** (toggles)
- *Variación* — swells de dinámica, octavas ocasionales, lead-in suave y
  dropouts raros sobre las células.
- *Respiración* — habilita las pausas automáticas de 2–4 compases.
- *Armonía* — acompañamiento de acordes + bajo en modo Canción.
- *Pulso* — pulso base en corcheas.

En el navbar: botón **play/stop** (ícono), botón **Beat** (pulso de
negras tipo *In C*, golpe agudo y delicado — se puede encender/apagar
independientemente del player), slider de **Vol master** (al mínimo mutea
totalmente), botón **?** que abre el modal con la documentación.

---

## Teclado (tocar sobre la obra)

Al final del panel hay una card con un teclado de una octava en Re mayor
(D4 · E4 · F♯4 · G4 · A4 · B4 · C♯5 · D5) para improvisar sobre la obra
mientras suena:

- **Dropdown de timbre** · misma lista que los músicos.
- **Slider de volumen propio** · independiente del master.
- Click o tocá con las teclas `A S D F G H J K` del teclado físico.

---

## Atajos de teclado

| Tecla | Acción |
|---|---|
| `Espacio` | Iniciar / Parar |
| `Esc` | Parar |
| `1` / `2` / `3` | Avanzar músico 1 / 2 / 3 |
| `A S D F G H J K` | Teclado musical (D4 → D5 en Re mayor) |
| Click en una célula | Preescucha |

---

## Cómo funciona el algoritmo In C

El modo Auto usa un reloj maestro de corcheas (`8n`) y por cada tick procesa
las tres voces en paralelo. Decisiones clave:

### Phasing rítmico permanente
Cada músico tiene un offset fijo (0, 1, 2 corcheas). Al tocar la misma
célula, las notas quedan desplazadas entre voces → *shimmer* polirrítmico
característico de *In C*.

### Dispersión máxima
Hasta **4 células** de diferencia entre el más adelantado y el más
atrasado. Si uno se excede, espera.

### Decisión de avance (por voz, en cada cierre de ciclo)
Mira sus propias reps (mínimas), la dispersión del grupo y el promedio de
posición. Si está rezagado, acelera. Si está en sincronía, avanza con
probabilidad que crece con las reps.

### Pausas con sentido (vs. aleatorias)
Pausas de 2–4 compases gatilladas por 3 reglas:

1. **Unísono prolongado** — si 2+ voces están en la misma célula hace rato,
   la que acumuló más reps sale a abrir espacio.
2. **Fatiga** — si una voz lleva >10 compases tocando sin descanso.
3. **Respiración de grupo** — cada ~10 compases, una voz al azar descansa.

Mínimo 6 compases entre pausas por voz.

### Factores "humanos"

Sobre el esqueleto algorítmico se montan 3 comportamientos que buscan dar
vida al ensamble:

1. **Dinámica adaptativa por densidad** — cuando están los 3 tocando, cada
   uno baja a 0.80× su velocity; con 2 → 0.95×; cuando queda uno solo
   (los otros respiran/paran), sube a 1.12× para llenar el espacio. El
   ensamble "respira" como grupo.
2. **Lead-in suave al cambiar de célula** — las primeras 2 reps de una
   célula nueva entran con fade-in (0.55 → 0.77 → full). La nueva voz
   emerge gradualmente en vez de cortar y empezar.
3. **Líder emergente / contagio** — cuando una voz avanza, se registra el
   momento y la posición. Las otras suben su probabilidad de avanzar
   hasta +0.35 si hay un salto reciente adelante (decae linealmente en
   6 compases). Simula el "yo voy, yo voy" humano. El status muestra
   "Siguiendo el impulso" cuando están reaccionando al contagio.

### Variación por repetición
Mientras repite una célula, cada voz aplica (si *Variación* está activa):

- *Swell de velocity* a lo largo de la permanencia (fade in – pico – fade out).
- *Saltos de octava por frase completa:*
  - Una octava abajo (`8vb`, ~25%): aporta contrapunto, calidez y cuerpo de bajo durante 1–2 repeticiones.
  - Una octava arriba (`8va`, ~9%): reservada para patrones de registro medio/grave (octava ≤ 4) y con velocity atenuada para dar brillo y campana sin estridencia ni saturar el oído.
  - Las cards de los músicos muestran el indicador `8vb` o `8va` en tiempo real mientras suena.
- *Dropout* muy raro (~5%) — una nota se omite para dar aire.

### Dinámica por arco de obra
Velocity base distinta según en qué sección está la voz:

- Intro (primeros 20% de células) → arrancan suaves y crecen (0.55 → 0.70).
- Productos (sección media) → tutti (0.75).
- Cierre (últimos 20%) → bajan y sostienen (0.70 → 0.60).

---

## Agregar o editar timbres

Los timbres están en [`timbres.yaml`](./timbres.yaml). Al cargar la página,
IN M lo lee y arma los dropdowns de cada canal.

### Formato

```yaml
timbres:
  - key: miPresetNuevo            # id único
    label: Mi preset nuevo        # nombre visible en el dropdown
    type: Synth                   # Synth | FMSynth | AMSynth
    volume: -8                    # nivel en dB (negativo baja)
    oscillator:
      type: triangle              # sine, triangle, square, sawtooth, pulse,
                                  # fatsine, fattriangle, fatsawtooth
      # spread: 20                # (sólo fat*): detuning entre osciladores
      # count: 3                  # (sólo fat*): cantidad de osciladores
      # width: 0.3                # (sólo pulse): ancho de pulso 0–1
    envelope:
      attack:  0.01
      decay:   0.2
      sustain: 0.5
      release: 0.4
    # Sólo FMSynth / AMSynth:
    # harmonicity: 3.0
    # modulationIndex: 2.0
    # modulation:
    #   type: sine
    # modulationEnvelope:
    #   attack: 0.001
    #   decay:  0.3
    #   sustain: 0.0
    #   release: 0.4
```

### Agregar un sonido

1. Pegá un bloque nuevo al final de `timbres.yaml` respetando la
   indentación con dos espacios.
2. Elegí un `key` único (sin espacios).
3. Guardá y recargá el navegador. Los dropdowns de cada músico se arman
   solos desde el YAML.

### Ejemplo — Prophet poly saw

```yaml
  - key: prophet
    label: Prophet Poly
    type: Synth
    volume: -12
    oscillator:
      type: fatsawtooth
      spread: 18
      count: 2
    envelope:
      attack:  0.08
      decay:   0.3
      sustain: 0.7
      release: 1.0
```

### Timbres incluidos de fábrica (14)

| key | Label | Carácter |
|---|---|---|
| `pluck` | Pluck | Triangle decay rápido, estilo kalimba suave |
| `pad` | Pad | FatSine warm, pad respirado |
| `bell` | Campana | FM clean, metálico resonante |
| `clarinet` | Clarinete | Triangle con attack lento, airoso |
| `flute` | Flauta | Sine con attack lento, limpio |
| `pulse` | Pulse | Pulse square 30%, estilo 80s |
| `saw` | Saw suave | Fatsawtooth con release corto |
| `marimba` | Marimba | FM percusivo, decay corto |
| `rhodes` | Rhodes EP | FM Yamaha-ish, cálido |
| `dx7` | DX7 EPiano | FM clásico Yamaha |
| `moog` | Moog Lead | AMSynth saw + mod square — imita filter sweep Moog |
| `juno` | Juno Pad | Fattriangle 4-voice detuned — calor chorus Juno |
| `tb303` | TB-303 Acid | AMSynth saw, harmonicity 0.5 — sub-armónica de bajo acid |
| `arp` | ARP Strings | FMSynth triangle — cuerdas ensemble con swell lento |

**Defaults por músico:** Rhodes (M1), DX7 (M2), Marimba (M3).

### Fallback

Si `timbres.yaml` no se puede cargar (abriste `index.html` con `file://`),
IN M usa un fallback embebido con los 14 timbres completos (los 8 originales
+ los 6 clásicos). La consola del navegador avisa.

---

## Arquitectura de audio

```
voz synth → panner estéreo ─┐
leadSynth (modo canción)   ─┤
chordSynth (acordes)       ─┼→ masterDelay → masterReverb → masterVolume → limiter → out
pulseSynth                 ─┘    (FeedbackDelay sync      (Reverb wet       (dB o
                                   al Transport)          controlable)       −∞)
bassSynth (sub-pad)        ─────────────────────────────→ masterVolume (sin FX)
```

- El bajo va directo sin FX para preservar la claridad del grave.
- Las voces + lead + chord pasan por el delay y después por el reverb.
- El pulso va al reverb directo (sin delay) para no manchar el click rítmico.

---

## Marco Teórico e Investigación Cultural

Para una profundización exhaustiva sobre la fundamentación estética, la historia de los creadores del jingle y la metodología de traducción algorítmica, consultar:

👉 [**IN M · Marco Teórico, Investigación Cultural y Metodología**](./doc/IN_M_marco_teorico_y_metodologia.md)

Puntos clave desarrollados en el documento:
- **Terry Riley y el sistema *In C* (1964):** Partitura abierta, escucha mutua (*mutual listening*), phasing rítmico, pulso constante y micropolifonía emergente.
- **Historia y fenomenología del jingle de Marolio (2001):** La gestación en The Sound Studio (Osvaldo Botaya), la composición de los hermanos Gustavo y Alejandro Ridilenir (músicos de Illya Kuryaki, Babasónicos y Dancing Mood), la voz de Andrea Báez y la concepción publicitaria de catálogo literal de Ignacio Tisser.
- **De spot comercial a mito popular:** El fenómeno sociocultural que trascendió la publicidad (coreado masivo en el Luna Park ante 9.000 personas junto a Ciro y Los Persas, versión metalera de Asspera, memes y memoria colectiva).
- **Desplazamiento funcional:** La transmutación de la repetición publicitaria (diseñada para el consumo) en repetición minimalista contemplativa.

---

## Estructura del proyecto

```
inmsynth/
├── index.html                           # app completa (HTML + CSS + JS inline)
├── timbres.yaml                         # catálogo de timbres editable
├── README.md                            # este archivo
├── LICENSE                              # CC BY-SA 4.0
└── doc/
    ├── partitura.png                    # partitura original escaneada
    ├── IN_M_marco_teorico_y_metodologia.md # marco teórico, investigación cultural y metodología
    ├── IN_M_transcripcion_partitura.md  # transcripción nota a nota
    ├── IN_M_analisis_v1.md              # análisis musical v1
    └── IN_M_analisis_v2.md              # análisis musical v2
```

Sin build step, sin dependencias que instalar. Dependencias externas por CDN:

- [Tone.js 14.8.49](https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.49/Tone.js) — motor de audio
- [js-yaml 4.1.0](https://cdn.jsdelivr.net/npm/js-yaml@4.1.0/dist/js-yaml.min.js) — parser YAML

---

## Modificar la partitura

Las células están en `const CELLS = [...]` dentro de `index.html`:

```js
{
  id: 5,
  name: 'Mate',
  region: 'D',             // 'D' = Re mayor, 'E' = Mi mayor
  chord: 'D/A',
  group: 'products-d',     // intro | products-d | products-e | outro
  beats: 2,
  notes: [
    { p: 'D5', d: '8n', t: 0.0, s: 'Ma-' },   // pitch, duración, tiempo, sílaba
    { p: 'D5', d: '8n', t: 0.5, s: '-te,' }
  ]
}
```

Para modo Canción está también `const SONG_MELODY = [...]` con la secuencia
lineal exacta de los 18 compases, y `const SONG_CHORDS = [...]` con la
armonía (acordes + bajo).

El `group` determina en qué fila de la góndola se dibuja la célula:
intro (fila 1), products-d/e (fila 2), outro (fila 3).

---

## Licencia

Código, interfaz y algoritmo bajo
[**CC BY-SA 4.0**](https://creativecommons.org/licenses/by-sa/4.0/).
Ver [`LICENSE`](./LICENSE).

La melodía transcripta deriva del jingle original de Marolio (cancionero
popular argentino). Esta aplicación es un homenaje no comercial en línea
con la idea de "partitura abierta" de *In C* de Terry Riley.

---

## Créditos

- *In C* — Terry Riley (1964), de donde tomamos las reglas de escucha mutua.
- Jingle de Marolio — cancionero popular argentino.
- Audio engine: [Tone.js](https://tonejs.github.io/).
- YAML parsing: [js-yaml](https://github.com/nodeca/js-yaml).
