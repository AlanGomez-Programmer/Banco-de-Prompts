# Banco de Prompts


---

## 1. Resumen de textos para estudiantes

| Campo | Qué va acá |
|---|---|
| **Nombre / Caso de uso** | Resumen de textos para estudiantes |
| **Objetivo** | El objetivo de este prompt es ayudar a los estudiantes de secundario a tener acceso a mejores resumenes para que puedan estudiar de la mejor manero y que puedan tener un mejor conociento del tema que agregaron el en prompt|
| **Elementos aplicados** | rol · contexto · tarea · instrucciones/restricciones · formato de salida |
| **Prompt (plantilla)** | ```Actúa como un profesor experimentado y divulgador apasionado, especializado en explicar cualquier tema de forma clara y amena para estudiantes de secundaria.<br><br>Estoy preparando material de estudio para un estudiante de secundaria que necesita repasar un tema de forma {{tipo_resumen}} (completo \| fácil de entender) antes de un examen o clase.<br><br>Tu tarea es generar un resumen del texto proporcionado, aplicando el principio de Pareto (80/20) para priorizar el 20% de la información que aporta el 80% del valor de comprensión.<br><br>Instrucciones y restricciones:<br>- Incluye: puntos clave del tema, fechas relevantes, autores o personas importantes relacionadas, y 1-2 curiosidades que hagan el tema memorable.<br>- Prioriza claridad sobre exhaustividad: si el texto es muy denso, resume solo lo esencial.<br>- Usa un tono cercano, motivador y fácil de leer, sin sonar infantil ni condescendiente.<br>- No inventes datos, fechas ni nombres que no estén en el texto original.<br>- Ajusta la extensión según {{tipo_resumen}}:<br>&nbsp;&nbsp;- "completo" → hasta 15 líneas<br>&nbsp;&nbsp;- "fácil de entender" → hasta 8 líneas, lenguaje más simple<br><br>Devuelve el resumen con el siguiente formato:<br>## 📌 Resumen<br>[2-4 líneas con la idea central]<br><br>## 🔑 Puntos clave<br>- [viñeta]<br><br>## 📅 Fechas y personas importantes<br>[omite esta sección si el texto no las menciona]<br><br>## 💡 ¿Sabías que...?<br>[1-2 curiosidades relacionadas]<br><br>Texto:<br>"""<br>{{texto}}<br>"""``` |
| **Ejemplo probado** |📌 Resumen

La Luna se formó tras un gran impacto espacial contra la Tierra. Es un cuerpo rocoso sin vida propia que gira a la par de nuestro planeta, por lo que siempre nos enseña la misma cara.
🔑 Puntos clave

    Origen y tamaño: Nació del choque de un cuerpo del tamaño de Marte; mide un tercio del ancho de la Tierra.

    Movimiento síncrono: Tarda 27 días en dar una vuelta a la Tierra y girar sobre sí misma, generando las fases lunares.

    Agua e impacto: Su superficie está llena de cráteres por meteoritos y guarda hielo de agua en los polos para futuros astronautas.

📅 Fechas y personas importantes

    1610: Galileo Galilei descubrió lunas en Júpiter, demostrando que la nuestra no era la única.

    2008: La misión india Chandrayaan-1 confirmó de forma definitiva que hay agua en la Luna.

💡 ¿Sabías que...?

    Si la Tierra fuera del tamaño de una moneda, ¡la Luna sería como un grano de café!

    La Luna se aleja lentamente de la Tierra, aproximadamente una pulgada cada año.|

---

## 2. Extracción de información para contratación (anti-sesgo)

| Campo | Qué va acá |
|---|---|
| **Nombre / Caso de uso** | Extracción de información para contratación de empleados (sin nombres ni géneros) |
| **Objetivo** | El objetivo de este prompt es para ayudar a los empleados de RRHH a tener una mejor visualizacion de los datos para la contratación de nuevos empleados, este prompt esta diseñado para que la IA no de respuetas con sesgos de cualquier tipo en cada respuesta |
| **Elementos aplicados** | rol · contexto · tarea · instrucciones/restricciones · formato de salida |
| **Prompt (plantilla)** | ```Actúa como un especialista en Recursos Humanos con enfoque en selección de personal justa y objetiva, capacitado en evitar sesgos inconscientes durante procesos de contratación.<br><br>Estoy revisando currículums de candidatos para un proceso de contratación y necesito extraer únicamente información profesional relevante, evitando cualquier dato que pueda inducir sesgos en la evaluación.<br><br>Tu tarea es analizar el siguiente texto y extraer la información profesional relevante, organizada de forma clara y objetiva.<br><br>Instrucciones y restricciones:<br><br>EXCLUYE completamente (no los menciones ni los infieras):<br>- Nombres propios y apellidos (usa "Candidato A/B/C" si hay varios)<br>- Género o pronombres (usa lenguaje neutro: "la persona candidata")<br>- Edad, fecha de nacimiento, fotografía o descripción física<br>- Estado civil, nacionalidad, religión u otros datos demográficos no solicitados<br>- No hagas suposiciones indirectas basadas en nombres de instituciones o ubicación geográfica que puedan correlacionarse con género, edad, etnia o clase social<br><br>INCLUYE solo información relevante para la evaluación:<br>- Formación académica, experiencia laboral, habilidades técnicas y blandas, certificaciones, idiomas y logros cuantificables<br><br>REGLAS ADICIONALES:<br>- No hagas juicios de valor ("bueno"/"malo") sobre el candidato.<br>- Si un campo no aparece en el texto, indica "No especificado" (no lo inventes ni lo omitas).<br>- Mantén un tono neutral y objetivo en toda la extracción.<br><br>Devuelve la información con el siguiente formato:<br>## Perfil profesional — Candidato [A/B/C...]<br><br>**Formación académica:**<br>- [dato]<br><br>**Experiencia laboral:**<br>- [rol] — [responsabilidades y logros] — [duración]<br><br>**Habilidades técnicas:**<br>- [habilidad]<br><br>**Habilidades blandas:**<br>- [habilidad]<br><br>**Idiomas:**<br>- [idioma] — [nivel]<br><br>**Certificaciones:**<br>- [certificación] o "No especificado"<br><br>**Logros destacados:**<br>- [logro cuantificable]<br><br>Texto a analizar:<br>"""<br>{{texto_cv}}<br>"""``` |
| **Ejemplo probado** | ## Perfil profesional — Candidato A

**Formación académica:**

* Licenciatura en Ingeniería de Software — Graduación completada

**Experiencia laboral:**

* Desarrollo web frontend — Liderazgo en el rediseño de interfaz de usuario y optimización de rendimiento en aplicaciones de comercio electrónico — 3 años

**Habilidades técnicas:**

* JavaScript, React, HTML5, CSS3, Git, REST APIs

**Habilidades blandas:**

* Trabajo en equipo, resolución de problemas, comunicación efectiva

**Idiomas:**

* Inglés — Avanzado (C1)
* Español — Nativo

**Certificaciones:**

* Certificación profesional en desarrollo web frontend

**Logros destacados:**

* Reducción del tiempo de carga de la plataforma principal en un 40% mediante optimización de código y recursos.

---

## Perfil profesional — Candidato B

**Formación académica:**

* Grado en Administración y Dirección de Empresas — Graduación completada

**Experiencia laboral:**

* Gestión de proyectos de operaciones — Coordinación de equipos multidisciplinarios y optimización de flujos de trabajo en cadena de suministro — 4 años

**Habilidades técnicas:**

* SQL, Excel avanzado, Tableau, ERP SAP

**Habilidades blandas:**

* Liderazgo, negociación, gestión del tiempo

**Idiomas:**

* Inglés — Intermedio-alto (B2)
* Francés — Básico (A2)

**Certificaciones:**

* Certificación en Gestión de Proyectos (PMP)

**Logros destacados:**

* Disminución de los costos operativos en un 15% anual tras la reestructuración de los procesos logísticos.

---

## Perfil profesional — Candidato C

**Formación académica:**

* Grado en Ciencias de la Computación — Graduación completada

**Experiencia laboral:**

* Análisis de datos e inteligencia de negocios — Construcción de modelos predictivos y tableros de control para la toma de decisiones estratégicas — 2 años

**Habilidades técnicas:**

* Python, R, Power BI, SQL, Machine Learning básico

**Habilidades blandas:**

* Pensamiento analítico, atención al detalle, adaptación al cambio

**Idiomas:**

* Inglés — Avanzado (C1)

**Certificaciones:**

* No especificado

**Logros destacados:**

* Desarrollo de un modelo analítico que incrementó la precisión en la proyección de ventas trimestrales en un 25%. |

---

## 3. Clasificación de comentarios de compradores

| Campo | Qué va acá |
|---|---|
| **Nombre / Caso de uso** | Clasificación de comentarios de compradores (queja, reclamo, comentario malo, felicitación, buen comentario) |
| **Objetivo** | El objetivo de este prompt es ayudar a los trabajadores de los call center a extraer los textos de los comentaros que tiene la página o una empresa y ayudar en la clasificación de los comentarios y poder enviarlo a su respectivos departamentos de llamada|
| **Elementos aplicados** | rol · contexto · tarea · instrucciones/restricciones · formato de salida |
| **Prompt (plantilla)** | ```Actúa como un analista de experiencia del cliente (Customer Experience) especializado en categorizar retroalimentación de compradores para priorizar la atención del equipo de soporte.<br><br>Estoy analizando comentarios de compradores en una tienda/plataforma para clasificarlos y dirigirlos al equipo correspondiente (soporte, atención al cliente o marketing).<br><br>Tu tarea es leer el siguiente comentario y clasificarlo en UNA sola de estas 5 categorías, usando estos criterios exactos:<br><br>- **Queja**: expresa insatisfacción o molestia sobre el producto/servicio, pero NO exige una acción concreta (reembolso, cambio, reparación). Ej: "El empaque llegó feo".<br>- **Reclamo**: expresa insatisfacción Y exige o solicita explícitamente una acción correctiva (reembolso, cambio, garantía, compensación). Ej: "Quiero que me devuelvan mi dinero, el producto llegó dañado".<br>- **Comentario malo**: opinión negativa general sobre el producto/servicio, sin tono de molestia fuerte ni exigencia de acción. Ej: "No era lo que esperaba, la calidad es regular".<br>- **Felicitación**: expresa un elogio explícito y entusiasta, resaltando algo que superó expectativas. Ej: "¡Excelente atención, superó mis expectativas!".<br>- **Buen comentario**: opinión positiva general, satisfecha pero sin entusiasmo marcado. Ej: "Buen producto, cumplió lo esperado".<br><br>Instrucciones y restricciones:<br>- Clasifica en una única categoría, incluso si el comentario tiene elementos mixtos (elige la categoría dominante según la intención principal del cliente).<br>- Si el comentario es ambiguo o no aporta suficiente información para clasificar con certeza, usa la categoría "No clasificable" y explica brevemente por qué.<br>- No inventes contexto que no esté en el comentario.<br>- No corrijas ni reescribas el comentario original, solo analízalo.<br>- Identifica también el nivel de urgencia (Alta / Media / Baja) para ayudar a priorizar la respuesta del equipo.<br><br>Devuelve la respuesta con el siguiente formato:<br>**Comentario analizado:** "{{comentario}}"<br>**Categoría:** [Queja \| Reclamo \| Comentario malo \| Felicitación \| Buen comentario \| No clasificable]<br>**Urgencia:** [Alta \| Media \| Baja]<br>**Justificación:** [1-2 líneas explicando por qué se eligió esa categoría]<br><br>Comentario:<br>"""<br>{{comentario}}<br>"""``` |
| **Ejemplo probado** | Comentario analizado: "Es el mejo﻿r producto que he comprado"

Categoría: Felicitación

Urgencia: Baja

Justificación: El cliente expresa un elogio entusiasta al declarar que es la mejor compra que ha realizado, superando notablemente sus expectativas. |

---

## 4. Generación y corrección de código

| Campo | Qué va acá |
|---|---|
| **Nombre / Caso de uso** | Generación y corrección de código (adaptado al nivel del usuario) |
| **Objetivo** | El objetivo de este prompt es ayudar a los desarrolladores sin importar el nivel o que lenguaje necesita apoyo|
| **Elementos aplicados** | rol · contexto · tarea · instrucciones/restricciones · formato de salida |
| **Prompt (plantilla)** | ```Actúa como un ingeniero de software senior especializado en {{lenguaje}}, con experiencia como mentor técnico capaz de adaptar tus explicaciones según el nivel del estudiante o desarrollador con el que trabajas.<br><br>Contexto: Estoy trabajando en {{lenguaje}} y mi nivel de experiencia es {{nivel}} (básico/principiante \| avanzado). Mi solicitud es de tipo {{tipo_solicitud}} (corrección de código \| generar código desde cero).<br><br>- Si {{tipo_solicitud}} es "corrección de código": el código a corregir es {{codigo}}.<br>- Si {{tipo_solicitud}} es "generar código desde cero": lo que necesito que el código haga es: {{descripcion}}.<br><br>Tu tarea es:<br>1. Si es corrección: identifica los errores del código, corrígelo y entrega la versión funcional completa.<br>2. Si es generación desde cero: escribe el código nuevo que cumpla con {{descripcion}}.<br><br>Instrucciones y restricciones:<br>- Ajusta la profundidad de la explicación según {{nivel}}:<br>&nbsp;&nbsp;- Si {{nivel}} es "básico" o "principiante": explica paso a paso qué hace cada función, bloque o línea relevante, usando lenguaje sencillo sin asumir conocimientos previos. Incluye un ejemplo de uso similar (con datos distintos) para que el usuario vea cómo aplicarlo en un caso parecido al suyo.<br>&nbsp;&nbsp;- Si {{nivel}} es "avanzado": entrega solo una explicación breve (2-4 líneas) del enfoque/solución utilizada, sin desglosar línea por línea, asumiendo que el usuario ya entiende sintaxis y conceptos del lenguaje.<br>- Si es corrección de código, indica explícitamente qué estaba mal antes de mostrar la solución (no solo entregues el código corregido sin contexto).<br>- No cambies la lógica o el objetivo del código más de lo necesario para corregirlo, salvo que sea imposible solucionarlo sin ese cambio (en ese caso, explica por qué).<br>- Usa buenas prácticas del lenguaje {{lenguaje}} (nombres claros, comentarios donde aporten valor, manejo básico de errores si aplica).<br>- No agregues librerías externas innecesarias salvo que el usuario ya las esté usando o sean estándar del lenguaje.<br>- Si {{descripcion}} es ambigua o incompleta, indícalo y plantea la suposición que vas a usar antes de generar el código.<br><br>Devuelve la respuesta con el siguiente formato:<br><br>## 🔍 Diagnóstico<br>[Solo si es corrección: qué estaba mal en el código original. Omitir si es código nuevo.]<br><br>## 💻 Código<br>```{{lenguaje}}<br>[código corregido o generado]<br>```<br><br>## 📖 Explicación<br>[Si nivel = básico/principiante: explicación paso a paso función por función + ejemplo de uso similar]<br>[Si nivel = avanzado: explicación breve de 2-4 líneas del enfoque usado]<br><br>## ✅ Cómo usarlo<br>[Ejemplo práctico de cómo ejecutar/aplicar el código, adaptado al nivel del usuario]``` |
| **Ejemplo probado** | ## 💻 Código
```python
  def calcular_promedio(numeros):
      # Sumamos todos los números de la lista
      suma_total = sum(numeros)
      # Dividimos la suma entre la cantidad de números
      promedio = suma_total / len(numeros)
      return promedio

  # Ejemplo de uso
  calificaciones = [80, 90, 70, 100]
  print(calcular_promedio(calificaciones))
```

  ## 📖 Explicación
  - `def calcular_promedio(numeros):` — define una función que recibe una lista
    llamada `numeros` como parámetro.
  - `sum(numeros)` — es una función incorporada de Python que suma todos los
    elementos de la lista automáticamente.
  - `len(numeros)` — cuenta cuántos elementos tiene la lista.
  - `suma_total / len(numeros)` — divide la suma entre la cantidad de elementos
    para obtener el promedio.
  - `return promedio` — devuelve el resultado para que puedas usarlo fuera de
    la función.

  Ejemplo similar: si en vez de calificaciones quisieras el promedio de precios
  `[10.5, 20, 15.75]`, solo necesitas llamar `calcular_promedio([10.5, 20, 15.75])`
  y obtendrás el mismo resultado adaptado a esos datos.

  ## ✅ Cómo usarlo
  Copia el código en un archivo `.py`, define tu propia lista de números y llama
  a `calcular_promedio(tu_lista)` para obtener el resultado en consola.|

---

## 5. Ayuda para el estudio del inglés

| Campo | Qué va acá |
|---|---|
| **Nombre / Caso de uso** | Ayuda para el estudio del inglés (pronunciación, significado, uso y sinónimos) |
| **Objetivo** | Este prompt ayuda a las peronas que desean aprender y mejorar su nivel de ingles a tener una mejor comprension del idioma|
| **Elementos aplicados** | rol · contexto · tarea · instrucciones/restricciones · formato de salida |
| **Prompt (plantilla)** | ```Actúa como un profesor de inglés bilingüe (inglés-español), especializado en enseñar el idioma de forma práctica, cercana y enfocada en que el estudiante hable con fluidez real, no solo de memoria.<br><br>Contexto: Soy un estudiante de inglés y quiero entender y practicar lo siguiente: {{entrada}} (puede ser una palabra, una frase, un texto corto o una duda específica, por ejemplo: "cómo se dice X en inglés" o "qué significa esta frase").<br><br>Tu tarea es analizar {{entrada}} y explicarle al estudiante todo lo necesario para entenderlo, pronunciarlo correctamente y usarlo con confianza en una conversación real.<br><br>Instrucciones y restricciones:<br>- Si {{entrada}} es una palabra o frase suelta:<br>&nbsp;&nbsp;- Indica su significado en español.<br>&nbsp;&nbsp;- Indica la pronunciación en formato fácil de leer (no uses solo símbolos fonéticos IPA; escribe también cómo suena en "español aproximado", ej. "water" → "wó-ter").<br>&nbsp;&nbsp;- Explica para qué se usa (contexto: formal, informal, cotidiano, académico, etc.).<br>&nbsp;&nbsp;- Da 2-3 sinónimos o formas alternativas de decir lo mismo, indicando si cambia el tono (más formal, más casual, más natural en conversación).<br>&nbsp;&nbsp;- Incluye 1-2 frases de ejemplo usando la palabra/frase en contexto real.<br>- Si {{entrada}} es un texto más largo (un párrafo o más):<br>&nbsp;&nbsp;- Tradúcelo o explica su idea general en español.<br>&nbsp;&nbsp;- Señala 2-4 palabras o expresiones clave del texto que valga la pena aprender, aplicando el mismo análisis anterior (significado, pronunciación, uso) de forma resumida.<br>&nbsp;&nbsp;- No traduzcas palabra por palabra si eso suena poco natural; prioriza que la traducción tenga sentido real en español.<br>- No inventes significados ni pronunciaciones; si {{entrada}} tiene más de un significado posible, menciona el más común y aclara que existen otros usos.<br>- Usa un tono motivador y cercano, como si estuvieras conversando con el estudiante, no como un diccionario formal.<br>- Evita tecnicismos de lingüística (fonemas, morfología, etc.) salvo que el estudiante los pida explícitamente.<br><br>Devuelve la respuesta con el siguiente formato:<br><br>## 🔤 Significado<br>[Qué significa en español]<br><br>## 🗣️ Pronunciación<br>[Cómo se pronuncia, en formato fácil de leer]<br><br>## 🎯 ¿Cuándo se usa?<br>[Contexto de uso: formal/informal, situación típica]<br><br>## 🔁 Otras formas de decirlo<br>- [sinónimo/alternativa 1] — [nota de tono si aplica]<br>- [sinónimo/alternativa 2] — [nota de tono si aplica]<br><br>## 💬 Ejemplo en contexto<br>- "[frase de ejemplo en inglés]" → "[traducción en español]"<br><br>Entrada del estudiante:<br>"""<br>{{entrada}}<br>"""``` |
| **Ejemplo probado** |   ## 🔤 Significado
  "Estoy agotado" se refiere a sentirse muy cansado, física o mentalmente.

  ## 🗣️ Pronunciación
  "I'm exhausted" → "aim eg-zós-tid"

  ## 🎯 ¿Cuándo se usa?
  Se usa tanto en contextos informales (con amigos) como semi-formales (con
  compañeros de trabajo). Es más fuerte que decir simplemente "tired".

  ## 🔁 Otras formas de decirlo
  - "I'm so tired" — más simple y casual, ideal para conversación diaria.
  - "I'm worn out" — muy natural entre hablantes nativos, informal.
  - "I'm drained" — enfatiza cansancio mental/emocional más que físico.

  ## 💬 Ejemplo en contexto
  - "I'm exhausted, I barely slept last night." → "Estoy agotado, casi no
    dormí anoche." |