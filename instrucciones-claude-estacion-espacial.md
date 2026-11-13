# Instrucciones para generar la página de la estación espacial

Eres un editor técnico y un diseñador de interfaces. Tu único entregable es un archivo HTML. Léelas todas antes de escribir una sola línea.

## Entregable

- Crea un solo archivo: `estacion-espacial.html`, en la misma carpeta que este documento.
- HTML, CSS y JavaScript van embebidos en ese archivo (`<style>` en el `<head>`, `<script>` al final del `<body>`).
- No uses frameworks, CDN, fuentes remotas, imágenes remotas ni hojas de estilo externas. La página debe abrirse bien haciendo doble clic, sin servidor y sin red.
- Los iconos y el diagrama de la cadena logística son SVG inline.
- Idioma de toda la interfaz y de todo el texto visible: español, con tildes y puntuación correcta.
- No generes otros archivos. No dejes comentarios que repitan estas instrucciones.

## Qué debe lograr la página

Explicar, de forma teórica y honesta, un plan por fases para:

1. Una estación alrededor de la Tierra, lo bastante grande para gravedad artificial, autosustentable en régimen maduro y usable como puerto de carga.
2. Dos puertos capaces de recibir dos naves a la vez.
3. Usar esa estación como primer escalón para una base lunar sustentable y como almacén de alimentos, combustible, materiales de construcción y equipos.
4. Desde esa cadena, una base intermedia entre la Luna y Marte, de apoyo logístico.
5. Una instalación en Marte autosustentable, abastecida con ayuda de la base intermedia.

Además, la página presenta **tres propuestas distintas** de toda la cadena (Tierra → Luna → intermedia → Marte). No son tres adornos de la misma idea: cambian órbita, forma del hábitat, nivel de gravedad, energía, sitio lunar, ubicación de la base intermedia y sitio marciano.

El tono es de divulgación técnica. Un lector curioso debe entender el orden de las decisiones. Un lector exigente debe ver qué es física conocida, qué es criterio de ingeniería y qué es escenario especulativo.

## Precisión: reglas que no puedes saltarte

Separa siempre tres capas, con una etiqueta visible junto a la afirmación:

- **Física.** Relaciones comprobadas. La gravedad artificial de este plan es centrípeta, por rotación: `ω = 2π · rpm / 60`, `a = ω² · R`, `g_rel = a / 9,80665`, con `R` en metros y `ω` en radianes por segundo. El puerto de visita va en un nodo desacoplado del giro (hub despun), porque una nave no puede atracar en un anillo que gira.
- **Criterio de ingeniería.** Pautas de estudios de hábitat, no leyes. Úsalas así: para estancias largas se suele buscar unos 2 rpm o menos, porque el Coriolis se nota al mover la cabeza y al caminar; por encima de unos 4 rpm el efecto es fuerte para la mayoría de las personas. El cierre total de aire, agua, comida y repuestos es un estado tardío, no el del primer año.
- **Escenario.** Arquitectura elegida para comparar. Órbitas, sitios, masas y décadas son hipótesis de trabajo.

Números:

- Si das un nivel de gravedad, un radio o unas rpm, tienen que cumplir la fórmula. Recalcula; no copies un resultado a ojo. Puedes redondear el radio al metro y las rpm a un decimal, y mostrar el `g_rel` resultante con dos decimales.
- Referencias solo para comprobar tu aritmética (vuelve a calcularlas): a 2,0 rpm y 224 m sale aproximadamente 1 g; a 1,0 rpm y 895 m, aproximadamente 1 g; a 2,0 rpm y 85 m, aproximadamente 0,38 g; a 1,0 rpm y 340 m, aproximadamente 0,38 g.
- Los delta-v, si aparecen, son órdenes de magnitud de literatura pública y llevan la etiqueta «orden de magnitud». No inventes un plan de vuelo ni una masa al kilogramo. Si no puedes defender una cifra, escribe el rango o no pongas el dígito.
- Rangos orientativos que sí puedes usar, siempre como orden de magnitud: superficie a LEO unos 9,4 km/s con pérdidas; LEO a transferencia lunar unos 3,1–3,2 km/s; órbita lunar baja a superficie unos 1,7–2 km/s; LEO a transferencia de Hohmann hacia Marte unos 3,6–4 km/s. La captura y el descenso en Marte dependen mucho del aerofrenado: dilo, no lo conviertas en un solo número falso.
- La autosuficiencia se describe por capas y por fase: energía, agua, aire, comida, repuestos y propergol. En las fases tempranas la Tierra sigue reponiendo. «Autosustentable» en esta página significa que, en régimen maduro, el hábitat cubre la mayor parte de aire, agua y calorías, fabrica o recicla una parte de los repuestos, y el propergol de salida hacia la Luna o Marte sale sobre todo de recursos locales (ISRU), no de un flujo permanente desde la Tierra.
- No afirmes que una agencia ha aprobado este plan. No cites informes con título, año o número que no estés seguro de que existan. Puedes nombrar conceptos públicos: rueda de von Braun, toro de Stanford, cilindro de O'Neill, ciclador de Aldrin, ISRU, ECLSS, Sabatier, puntos de Lagrange, NRHO.
- No des procedimientos de lanzamiento, de fabricación de propergol a escala industrial ni de ensamblaje orbital paso de taller. El contenido es arquitectura y secuencia de decisiones.

## Las tres propuestas

Desarrolla las tres con el mismo esquema, para que se puedan comparar. Cada una incluye estación terrestre, dos puertos, almacén, base lunar, base intermedia y base marciana.

### Propuesta A — Puerto cercano

Pensada para construir y reabastecer pronto, aceptando arrastre atmosférico y muchas lanzaderas.

- Estación: toro rígido en LEO, cerca de 450 km. Gravedad de diseño cerca de 1 g, con radio y rpm coherentes con la fórmula y con el criterio de ≤2 rpm (pista: radio de unos 220–250 m y cerca de 2 rpm; fija tú la pareja exacta y muestra el resultado).
- Dos puertos en el hub central, que no gira. Uno puede estar ocupado por un carguero y el otro por una nave tripulada, o los dos por carga. Esclusa de tripulación y esclusa de carga separadas.
- Energía: solar en el hub y en paneles que no tienen que girar con el anillo, más almacenamiento para la sombra orbital. Di que en LEO hay eclipses frecuentes.
- Vida: invernaderos en el anillo, reciclaje de agua y aire. Comida parcial al principio.
- Almacén: alimentos, propergol criogénico, kits de construcción y equipos, en módulos de depósito junto al hub, no en la zona que gira, para mover contenedores sin luchar contra el giro.
- Luna: base en el polo sur, alrededor de cráteres donde se ha detectado hielo (Shackleton como escenario). El hielo da agua, oxígeno y, con carbono traído o capturado, metano.
- Intermedia: depósito y refugio pequeño en el punto Tierra-Luna L2, del lado lejano de la Luna. Sirve como puerta de salida hacia Marte y como almacén de propergol producido en la Luna. No es una segunda ciudad.
- Marte: asentamiento en una llanura del hemisferio norte con acceso a hielo (usa Arcadia Planitia como escenario) y producción de metano y oxígeno a partir de CO₂ atmosférico y agua local.
- Tensión honesta: cada reboost cuesta propergol; la basura orbital importa; la ventana a Marte no mejora solo por estar en LEO. La ventaja es el acceso desde la Tierra.

### Propuesta B — Ciudad estable y ciclador

Pensada para agricultura de verdad y para un transporte Tierra-Marte que se repite, a cambio de una obra mucho mayor.

- Estación: cilindro de O'Neill corto en el punto Tierra-Luna L5, donde la órbita es dinámicamente más tranquila que en LEO baja. Gravedad cerca de 1 g a cerca de 1 rpm, así que el radio queda en la escala de cientos de metros a cerca de 1 km. Calcula la pareja y muéstrala. El interior del cilindro es suelo, invernadero y barrio; las tapas son industria y muelles.
- Dos puertos en los ejes de las tapas, en la zona de microgravedad. Los dos pueden recibir naves a la vez. El giro del cilindro no llega al mecanismo de atraque.
- Energía: grandes campos solares fuera del cilindro. En L5 no hay el ciclo de eclipse de 90 minutos de LEO; dilo como ventaja, sin prometer luz eterna (la orientación y el mantenimiento siguen existiendo).
- Almacén: la propia ciudad guarda cosechas, agua, equipos y propergol traído de la Luna. La comida de las misiones largas sale de aquí, no de un contenedor lanzado el mes anterior.
- Luna: base industrial en un tubo de lava (escenario: colinas Marius). El tubo da protección contra radiación y extremos térmicos. Exporta oxígeno, metales y áridos a L5.
- Intermedia: un ciclador de Aldrin, hábitat que viaja en una trayectoria repetida entre el sistema Tierra-Luna y Marte, más taxis que suben y bajan en cada encuentro. El encuentro dura poco: la página debe decir que quien pierde la ventana del taxi espera a la siguiente vuelta, del orden de un par de años, no de una semana.
- Marte: base en el sistema de Valles Marineris (escenario), con invernaderos presurizados, energía nuclear de fisión como respaldo del sol —el polvo global existe— y propergol local.
- Tensión honesta: la masa a ensamblar es enorme; el ciclador no se «aparca» junto a Marte; hace falta una industria lunar ya en marcha antes de que el ciclador merezca la pena.

### Propuesta C — Corredor de depósitos

Pensada para mover carga con poca masa estructural y para dejar caches entre la Tierra y Marte, a cambio de viajes más lentos y de una gravedad menor en el primer hábitat.

- Estación: dos hábitats unidos por un cable (tether) en órbita terrestre alta, por encima de la basura densa de LEO y con menos arrastre. Giran alrededor del centro de masa. Gravedad de diseño 0,38 g, parecida a la de Marte, para que la tripulación y los invernaderos vivan ya en el régimen del destino. Radio y rpm coherentes con ≤2 rpm (pista: cerca de 1 rpm el radio ronda unos pocos cientos de metros; calcula y muestra). Un hub en el centro de masa, sin giro útil para la tripulación, con los dos puertos.
- Por qué 0,38 g y no 1 g: menos longitud de cable y menos masa para la misma rpm, y aclimatación al cuerpo y a los cultivos que luego irán a Marte. La página debe decir que 0,38 g no sustituye la evidencia médica que aún no existe sobre años enteros en esa gravedad: es una hipótesis de diseño.
- Energía: solar en el hub y, para las naves de carga del corredor, propulsión eléctrica solar de bajo empuje.
- Almacén: el hub es un puerto de contenedores. Los cuatro tipos de recurso (alimentos, combustible, materiales, equipos) viajan en contenedores estándar del escenario, intercambiables entre estación, Luna, depósito intermedio y Marte.
- Luna: polo sur, igual que en A en cuanto al hielo, pero aquí la Luna es sobre todo mina y fábrica: oxígeno como propergol y como masa de reacción, metales y piezas sinterizadas. La estación terrestre ensambla poco; la Luna fabrica.
- Intermedia: un depósito en órbita heliocéntrica entre las órbitas de la Tierra y Marte, cerca de 1,3 UA (escenario). No orbita la Luna ni Marte. Lo reponen cargueros eléctricos lentos. Acorta la cadena: una misión tripulada no tiene que llevar desde la Tierra todo el propergol del tramo final.
- Marte: asentamiento cercano al casquete norte, donde el hielo es el recurso dominante (escenario), con reactores y huertos. Fobos puede mencionarse solo como puerto natural opcional de bajada, no como la base intermedia: la intermedia de esta propuesta es el depósito a 1,3 UA.
- Tensión honesta: el cable tiene modos de vibración y riesgo de corte; la propulsión eléctrica alarga los viajes de carga a meses; 0,38 g es una apuesta fisiológica.

Las tres deben verse, en la tabla comparativa, distintas en al menos estas filas: órbita de la estación, tipo de hábitat, gravedad y par radio/rpm, energía, sitio lunar, base intermedia, sitio marciano, plazo (en décadas, como rango), riesgo que domina y motivo para elegirla.

## Paso a paso

Además de las tres propuestas, hay un método común de once fases. Cada propuesta reutiliza esas fases y dice en qué cambia. No dupliques once textos casi iguales tres veces: el método se explica una vez; en cada propuesta, un bloque «cómo se aplica aquí» recorre las fases en menos líneas, solo con lo que cambia.

Fases, en este orden:

1. **Marco.** Qué se quiere decidir, qué queda fuera (no es un programa nacional ni un presupuesto), criterios de éxito del escenario.
2. **Órbita y forma.** Dónde vive la estación y cómo genera gravedad. Por qué el puerto no gira con el hábitat.
3. **Energía y calor.** De dónde sale la electricidad y cómo se rechaza el calor. Sin energía sobrada no hay invernadero ni depósito criogénico.
4. **Estructura que gira.** Orden conceptual: hub y puertos primero (en microgravedad ya se puede recibir carga), luego el radio habitable. Un puerto de carga que espera a la ciudad terminada no cumple el encargo.
5. **Aire, agua y comida.** ECLSS en capas. Meta de calorías por fase, sin prometer el 100 % el primer año. Residuos como recurso.
6. **Dos puertos y carga.** Operación simultánea de dos naves: atraque, esclusas separadas, grúa o carril de contenedores en el hub, zona de propergol alejada de la esclusa de tripulación. Qué pasa si un puerto queda fuera de servicio: el otro mantiene el puerto vivo.
7. **Almacén.** Cuatro familias —alimentos, combustible, materiales de construcción, equipos— con una función distinta para cada una: la comida alimenta estación, Luna y tránsitos; el combustible abre las salidas; los materiales construyen la base lunar y después la marciana; los equipos son el repuesto que no se puede improvisar. Incluye la idea de stock de seguridad para una ventana de lanzamiento perdida.
8. **Salto a la Luna.** La estación como astillero y depósito: se acumula, se prueba el hábitat lunar en el puerto y se manda en una ventana. La base lunar no nace autosuficiente; hereda el almacén terrestre.
9. **Base lunar sustentable.** Energía local, hielo, oxígeno, un invernadero, protección (regolito o tubo) y una línea de vuelta de productos hacia la estación. Sustentable aquí quiere decir que la base puede pasar una noche lunar o un fallo de reabastecimiento sin evacuarse, y que exporta más masa útil de la que importa en régimen maduro. El texto debe reconocer que ese régimen llega después de una etapa dependiente.
10. **Base intermedia.** Su trabajo no es ser otra ciudad: guarda propergol y repuestos, ofrece refugio y mantiene la cadena cuando la geometría Tierra-Marte es mala. Ubicación según la propuesta.
11. **Marte autosustentable.** Energía que sobreviva a las tormentas de polvo, agua local, aire y comida de invernadero, propergol de retorno o de hoppers, y un almacén que la intermedia rellena en cada ventana. Cierre maduro: la base marciana produce lo esencial para permanecer aunque falle una ventana de suministro. El texto no debe decir que el primer descenso ya es independiente.

En cada fase del método común incluye, en este orden y con estos rótulos visibles: Objetivo, Decisiones, Trabajos, Dependencia (qué fase tiene que existir antes), Criterio de listo, Riesgo principal. El riesgo no puede ser una frase vacía del tipo «puede haber fallos».

## Estructura de la página

Un solo documento, con desplazamiento vertical y navegación fija. Orden:

1. **Portada.** Título, una frase que diga que es un escenario teórico, y tres datos de alcance: gravedad por rotación, dos naves a la vez, cadena Tierra–Luna–intermedia–Marte. Un botón a las propuestas y otro al paso a paso.
2. **Cadena.** Diagrama SVG de cinco nodos: Tierra, estación, Luna, intermedia, Marte. Cada nodo se puede activar y lleva a su sección. Una línea de tiempo breve debajo: acumular en órbita, aprender en la Luna, cachear en el camino, permanecer en Marte.
3. **Método.** Las once fases. En pantallas anchas, un raíl numerado; en estrechas, lista. Se puede abrir y cerrar cada fase. La primera fase aparece abierta.
4. **Tres propuestas.** Selector persistente (A, B y C). Al elegir una, cambia el detalle, la URL con hash (`#propuesta-a`, `#propuesta-b`, `#propuesta-c`) y el estado del diagrama si hace falta. Al cargar la página con un hash, esa propuesta queda seleccionada. Incluye en cada una: resumen en un párrafo, ficha técnica (órbita, hábitat, radio, rpm, g calculado, puertos, energía, almacén, Luna, intermedia, Marte), «cómo se aplica el método», tensión honesta y motivo para elegirla.
5. **Comparación.** Tabla con las filas obligatorias. En móvil la tabla no se sale de la pantalla: cada propuesta es un bloque apilado, o la tabla tiene desplazamiento horizontal con la primera columna fija. Cabecera de tabla con alcance claro.
6. **Explorador de gravedad.** Juguete didáctico, no un simulador certificado. Dos campos numéricos: radio en metros y rpm. Salida: aceleración en m/s², gravedad en g, y una nota de Coriolis según rpm (≤2, entre 2 y 4, >4), usando el criterio de arriba y diciendo que es una pauta. Botones para cargar los tres diseños (rellenan radio y rpm de A, B y C). Valores fuera de rango (radio ≤0, rpm ≤0, o cifras absurdas como más de 20 rpm o más de 5000 m) muestran un mensaje claro y no un NaN. La fórmula visible, en texto, junto a la herramienta.
7. **Almacén.** Los cuatro recursos, cada uno con qué problema resuelve en la estación, en la Luna, en la intermedia y en Marte.
8. **Límites.** Qué no demuestra esta página: medicina de años en gravedad parcial, presupuesto, tratado político, diseño estructural detallado, protección planetaria más allá de una mención (no se contamina Marte ni se trae material marciano sin un protocolo; en este escenario eso queda como condición abierta, no como trámite resuelto).
9. **Cierre.** Tres frases: el orden es estación que ya recibe carga, Luna que aprende a vivir, camino con un almacén a mitad, Marte que puede quedarse. Recordatorio de que las tres propuestas compiten; no hace falta fingir que una ganó.

## Interacción

JavaScript propio, sin dependencias:

- Menú fijo con anclas a Portada, Cadena, Método, Propuestas, Comparación, Gravedad, Almacén y Límites. En pantallas estrechas, el menú se abre y se cierra con un botón que indica el estado (`aria-expanded`).
- Fases del método: botones de verdad, `aria-expanded`, un panel asociado con `aria-controls`. Cerrar una no borra el texto.
- Selector de propuestas: pestañas con `role="tablist"`, `role="tab"`, `role="tabpanel"`, flechas izquierda y derecha para cambiar, y el hash sincronizado sin recargar.
- Explorador de gravedad: calcula al escribir y al pulsar los tres botones de diseño. Usa los mismos números que la ficha de cada propuesta.
- Diagrama: cada nodo es un enlace o un botón con nombre accesible.
- Respeta `prefers-reduced-motion`: sin desplazamientos suaves ni animaciones largas si el usuario lo pide. Con movimiento permitido, un desplazamiento suave al usar el menú es suficiente. No hagas animaciones decorativas infinitas.
- Todo control se usa con teclado y muestra foco visible.

## Diseño

Tiene que parecer un informe de misión editado, no una plantilla de startup. Dirección visual obligatoria:

- Fondo tinta `#10140f`. Texto principal `#f3efe4`. Texto secundario `#c8c2b4`.
- Acento de la estación y de la energía: ámbar `#e0a45c`.
- Acento lunar: `#d7e2dc`. Acento de Marte: `#c4643a`. Acento de la intermedia: `#8aa88b`.
- Una sola familia para títulos: `Palatino Linotype`, Palatino, `Iowan Old Style`, Georgia, serif. Cuerpo: `Segoe UI`, system-ui, sans-serif. No uses Inter, Roboto, ni una fuente cargada por red.
- Títulos grandes, con tracking ligeramente cerrado. Números de fase en serif, del tamaño de un índice de libro.
- Maquetación: ancho de lectura cerca de 70 caracteres en los párrafos largos; las fichas y la tabla pueden usar todo el ancho hasta unos 1120 px. Portada con el título alineado a la izquierda, no centrado en una tarjeta flotante.
- Sin gradientes púrpura, sin glassmorphism, sin sombras blandas en cada caja, sin emojis, sin iconos de stock. Las separaciones se hacen con regla de 1 px en `#2a3128` y con espacio, no con tarjetas idénticas repetidas.
- Las tres propuestas se distinguen por una franja de 4 px: ámbar para A, verde salvia para B, óxido para C.
- Contraste suficiente para texto secundario sobre el fondo. Enlace y botón no se diferencian solo por el color: el enlace va subrayado; el botón tiene borde.
- `meta viewport`, `lang="es"`, título de documento y descripción. Encabezados en orden, sin saltar de `h1` a `h3`.
- Tipografía fluida con `clamp` para el título principal. El cuerpo no baja de 17 px.
- Una hoja mínima de impresión: fondo claro, texto oscuro, menú oculto, fases abiertas.

## Criterios de aceptación

Antes de dar el archivo por terminado, comprueba:

- Un solo HTML, se abre en local, consola sin errores al cargar, al cambiar de propuesta, al abrir fases y al usar el explorador con 0, con negativo y con los tres diseños.
- Los tres pares radio/rpm producen el g que la ficha declara, con la misma fórmula que el explorador.
- Están los dos puertos, los cuatro tipos de almacén, la base lunar, la base intermedia y Marte autosustentable, en las tres propuestas.
- A, B y C no comparten la misma órbita ni el mismo tipo de hábitat ni la misma intermedia.
- Hay once fases con los seis rótulos.
- No hay lorem ipsum, no hay cifras sin capa (física, criterio o escenario) cuando el número podría leerse como medición, y no hay promesa de autosuficiencia en el año uno.
- El hash `#propuesta-b` y `#propuesta-c` selecciona la propuesta correcta al cargar.
- En un ancho de 380 px no hay desplazamiento horizontal de la página entera. La tabla puede desplazarse dentro de su región.

## Prohibido

- No añadas una cuarta propuesta ni un «ganador» secreto.
- No conviertas el texto en una novela ni en una lista de consignas.
- No uses jerga sin una frase llana al lado la primera vez que aparezca (ECLSS, ISRU, delta-v, hub despun, ciclador, tether).
- No copies estas instrucciones dentro de la página.
