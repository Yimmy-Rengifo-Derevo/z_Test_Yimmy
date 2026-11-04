yimmy.rengifo@derevo.com.mx
yimmy.rengifo@derevo.com.mx  
yimmy.rengifo@derevo.com.mx  
·  
Yimmy Rengifo  
Technical Project Manager (TPM)  
Project Intelligence  
Derevo  
·  
Yimmy Rengifo · Technical Project Manager (TPM) · Project Intelligence · Derevo  
---
---
---

# Guía amplia de Markdown y funciones del preview de Visual Studio Code

**Objetivo:** reunir ejemplos reutilizables para documentación técnica, notas, manuales, procedimientos, informes y archivos README.

**Alcance:** esta guía conserva la sintaxis básica de Markdown y también incluye, en secciones claramente identificadas, extensiones GFM y funciones específicas del preview de VS Code que incorporaste manualmente: HTML, Mermaid, fórmulas matemáticas con KaTeX, Front Matter YAML y estilos CSS opcionales.

**Compatibilidad:** los ejemplos de Markdown básico funcionan sin configuración adicional. Las tablas, el tachado y las casillas se identifican como extensiones GFM. Mermaid y KaTeX son funciones del preview integrado de VS Code en versiones actuales; Front Matter tiene una representación propia en VS Code. Los ejemplos HTML/CSS de personalización son opcionales y requieren las condiciones explicadas en su sección.

> **Nota importante:** Markdown no define colores de texto, estilos personalizados de tablas, bordes dobles o punteados, diagramas Mermaid, fórmulas LaTeX ni metadatos Front Matter. Se conservan porque forman parte de la combinación manual que preparaste, pero se explican por separado para que no se confundan con la sintaxis Markdown estándar.

---

## Índice

1. [Abrir la vista previa en VS Code](#1-abrir-la-vista-previa-en-vs-code)
2. [Conceptos y reglas básicas](#2-conceptos-y-reglas-basicas)
3. [Títulos y encabezados](#3-titulos-y-encabezados)
4. [Párrafos, saltos de línea y separadores](#4-parrafos-saltos-de-linea-y-separadores)
5. [Formato de texto](#5-formato-de-texto)
6. [Listas](#6-listas)
7. [Citas, notas y bloques informativos](#7-citas-notas-y-bloques-informativos)
8. [Enlaces y referencias](#8-enlaces-y-referencias)
9. [Imágenes](#9-imagenes)
10. [Tablas y alineación — GFM](#10-tablas-y-alineacion--gfm)
11. [Bloques de código](#11-bloques-de-codigo)
12. [Ejemplos de distintos lenguajes](#12-ejemplos-de-distintos-lenguajes)
13. [Árboles de carpetas y jerarquías](#13-arboles-de-carpetas-y-jerarquias)
14. [Símbolos y caracteres especiales](#14-simbolos-y-caracteres-especiales)
15. [Escapar caracteres de Markdown](#15-escapar-caracteres-de-markdown)
16. [HTML dentro de Markdown](#16-html-dentro-de-markdown)
17. [Diagramas Mermaid](#17-diagramas-mermaid)
18. [Fórmulas matemáticas con KaTeX](#18-formulas-matematicas-con-katex)
19. [Contenido plegable](#19-contenido-plegable)
20. [Comentarios y contenido oculto](#20-comentarios-y-contenido-oculto)
21. [Front Matter YAML](#21-front-matter-yaml)
22. [Ejemplo integrado de documento completo](#22-ejemplo-integrado-de-documento-completo)
23. [Plantilla reutilizable de documento completo](#23-plantilla-reutilizable-de-documento-completo)
24. [Personalización opcional mediante HTML y CSS](#24-personalizacion-opcional-mediante-html-y-css)
25. [Limitaciones, diferencias y compatibilidad](#25-limitaciones-diferencias-y-compatibilidad)
26. [Resumen rápido de sintaxis](#26-resumen-rapido-de-sintaxis)
27. [Referencias oficiales](#27-referencias-oficiales)

---
## 1. Abrir la vista previa en VS Code

1. Abre este archivo `.md` en Visual Studio Code.
2. Haz clic derecho en la pestaña del archivo y selecciona **Open Preview to the Side**.
3. También puedes abrir la paleta de comandos con `Ctrl+Shift+P` y ejecutar `Markdown: Open Preview to the Side`.
4. Atajo para abrir la vista previa al lado del editor: `Ctrl+K`, seguido de `V`.
5. Atajo para abrir la vista previa en la pestaña actual: `Ctrl+Shift+V`.

La vista previa integrada de VS Code se actualiza mientras editas el archivo. Puedes mantener el código Markdown a la izquierda y el resultado visual a la derecha.

---

## 2. Conceptos y reglas básicas

Markdown es un lenguaje de marcado ligero. Se escribe como texto plano y se utilizan caracteres sencillos para indicar encabezados, listas, citas, enlaces, imágenes y bloques de código.

### 2.1 Reglas prácticas

- Deja una línea en blanco entre párrafos y, normalmente, antes y después de listas, citas y bloques de código.
- Deja un espacio después de los signos `#` de un encabezado: `## Título`.
- Usa una indentación consistente en las listas anidadas.
- Para bloques de código utiliza tres acentos graves: `` ``` ``.
- Para mostrar literalmente un carácter especial, utiliza una barra invertida `\` delante del carácter.
- El formato Markdown define la estructura del documento; no permite controlar de forma portable los colores, fuentes o bordes del visor.

### 2.2 Tabla de sintaxis básica

| Elemento | Sintaxis | Uso |
|:--|:--|:--|
| Encabezado | `# Título` | Título de nivel 1 |
| Negrita | `**texto**` | Énfasis fuerte |
| Cursiva | `*texto*` | Énfasis |
| Código en línea | `` `código` `` | Comandos o nombres de variables |
| Cita | `> texto` | Nota o cita |
| Lista con viñetas | `- elemento` | Elementos sin orden |
| Lista numerada | `1. elemento` | Pasos secuenciales |
| Enlace | `[texto](https://ejemplo.com)` | Referencia web |
| Imagen | `![descripción](imagen.png)` | Imagen con texto alternativo |
| Bloque de código | ```` ```python ```` | Código con identificador de lenguaje |
| Separador | `---` | Separación temática |

---

## 3. Títulos y encabezados

Markdown define **seis niveles de encabezado**. El nivel 1 suele reservarse para el título principal del documento. No existe un séptimo nivel.

### 3.1 Ejemplos de los seis niveles

# Título de nivel 1 — H1

## Título de nivel 2 — H2

### Título de nivel 3 — H3

#### Título de nivel 4 — H4

##### Título de nivel 5 — H5

###### Título de nivel 6 — H6

### 3.2 Sintaxis de cada nivel

| Nivel | Sintaxis |
|:--:|:--|
| H1 | `# Título` |
| H2 | `## Título` |
| H3 | `### Título` |
| H4 | `#### Título` |
| H5 | `##### Título` |
| H6 | `###### Título` |

### 3.3 Otra forma de escribir H1 y H2

Markdown también permite encabezados de estilo subrayado para los dos primeros niveles:

```markdown
Título de nivel 1
=================

Título de nivel 2
-----------------
```

Resultado:

Título de nivel 1
=================

Título de nivel 2
-----------------

### 3.4 Enlaces internos a encabezados

Puedes enlazar una sección del mismo documento utilizando su identificador generado por el visor:

```markdown
[Ir a la sección de tablas](#10-tablas-extension-gfm)
[Ir al resumen de sintaxis](#26-resumen-rapido-de-sintaxis)
```

[Ir a la sección de tablas](#10-tablas-extension-gfm) · [Ir al resumen de sintaxis](#26-resumen-rapido-de-sintaxis)

La conversión del encabezado a un identificador puede variar ligeramente según el motor Markdown, sobre todo si contiene tildes o signos de puntuación.

---

## 4. Párrafos, saltos de línea y separadores

### 4.1 Párrafos

Este es el primer párrafo. Una línea en blanco indica que comienza un párrafo nuevo.

Este es el segundo párrafo. Si solo pulsas Enter y no dejas una línea en blanco, el motor Markdown puede unir las líneas en el mismo párrafo.

### 4.2 Salto de línea dentro del mismo párrafo

En Markdown puedes terminar una línea con dos espacios y luego pulsar Enter. También puedes utilizar una barra invertida al final de la línea.

Primera línea con dos espacios al final.  
Segunda línea del mismo párrafo.

Primera línea con barra invertida al final.\
Segunda línea del mismo párrafo.

**Consejo:** algunos formateadores eliminan espacios al final de una línea. La barra invertida es una alternativa visible para indicar el salto.

### 4.3 Separadores horizontales

Se pueden utilizar tres o más guiones, asteriscos o guiones bajos en una línea independiente:

```markdown
---

***

___
```

Ejemplos:

---

***

___

Estos separadores crean una línea horizontal sencilla. Markdown no permite elegir mediante su sintaxis si la línea debe ser doble, punteada o de otro color.

---

## 5. Formato de texto

| Efecto | Cómo escribirlo | Resultado |
|:--|:--|:--|
| Negrita | `**Texto en negrita**` | **Texto en negrita** |
| Cursiva | `*Texto en cursiva*` | *Texto en cursiva* |
| Negrita y cursiva | `***Texto***` | ***Texto*** |
| Tachado | `~~Texto tachado~~` | ~~Texto tachado~~ |
| Código en línea | `` `SELECT * FROM dbo.Clientes;` `` | `SELECT * FROM dbo.Clientes;` |
| Cita corta | `> Texto citado` | Bloque de cita |
| HTML: resaltado | `<mark>Texto</mark>` | Ver sección 16: HTML |
| HTML: subíndice | `H<sub>2</sub>O` | Ver sección 16: HTML |
| HTML: superíndice | `x<sup>2</sup>` | Ver sección 16: HTML |
| HTML: tecla | `<kbd>Ctrl</kbd>` | Ver sección 16: HTML |
| HTML: texto pequeño | `<small>Texto</small>` | Ver sección 16: HTML |


### 5.1 Negrita

Sintaxis: `**texto**` o `__texto__`.

**Este texto está en negrita.**

__Este texto también está en negrita.__

### 5.2 Cursiva

Sintaxis: `*texto*` o `_texto_`.

*Este texto está en cursiva.*

_Este texto también está en cursiva._

### 5.3 Negrita y cursiva combinadas

Sintaxis: `***texto***`.

***Este texto está en negrita y cursiva.***

### 5.4 Énfasis dentro de una oración

En un documento técnico puedes combinar texto normal, **conceptos importantes**, *términos destacados* y `nombres_de_variables`.

### 5.5 Tachado — extensión GFM

La sintaxis `~~texto~~` es una extensión muy extendida, pero no forma parte del núcleo CommonMark:

~~Este texto aparece tachado en los visores compatibles.~~

### 5.6 Código en línea

Utiliza un acento grave antes y después del fragmento:

Ejemplo: ejecuta `SELECT * FROM dbo.Customers;` y revisa la variable `customer_id`.

Para mostrar un acento grave dentro del propio código, puedes envolver el fragmento con dos acentos graves:

``Use ` para escribir código en línea``

### 5.7 Énfasis semántico sin colores

Markdown no permite definir colores de texto de forma estándar. Para destacar información utiliza encabezados, **negrita**, *cursiva*, citas y etiquetas escritas en palabras:

> **IMPORTANTE:** valida los datos antes de ejecutar el proceso.

> **ADVERTENCIA:** confirma el impacto antes de modificar información productiva.

> **NOTA:** registra la evidencia y la fecha de la validación.

### 5.8 Combinación de formatos

Puedes combinar negrita, cursiva y código en línea: **texto importante**, *énfasis*, ***énfasis fuerte*** y `variable_name`.

### 5.9 Caracteres reservados y escape

Anteponer una barra invertida permite mostrar caracteres que Markdown normalmente interpreta como formato:

```markdown
\* Esto no será cursiva \*
\# Esto no será un encabezado
\- Esto no será una viñeta
\[Esto no será un enlace\]
```

Resultado: \* Esto no será cursiva \*.

---

## 6. Listas

### 6.1 Lista con guiones

```markdown
- Primer elemento
- Segundo elemento
- Tercer elemento
```

Resultado:

- Primer elemento
- Segundo elemento
- Tercer elemento

### 6.2 Lista con asteriscos

```markdown
* Primer elemento
* Segundo elemento
* Tercer elemento
```

Resultado:

* Primer elemento
* Segundo elemento
* Tercer elemento

### 6.3 Lista con signos más

```markdown
+ Primer elemento
+ Segundo elemento
+ Tercer elemento
```

Resultado:

+ Primer elemento
+ Segundo elemento
+ Tercer elemento

Los marcadores `-`, `*` y `+` crean listas con viñetas. Conviene mantener un único marcador dentro de cada lista.

### 6.4 Lista numerada

```markdown
1. Primer paso
2. Segundo paso
3. Tercer paso
```

Resultado:

1. Primer paso
2. Segundo paso
3. Tercer paso

### 6.5 Numeración automática

También puedes escribir `1.` en todos los elementos. El visor calculará los números consecutivos:

```markdown
1. Primer paso
1. Segundo paso
1. Tercer paso
```

Resultado:

1. Primer paso
1. Segundo paso
1. Tercer paso

### 6.6 Lista que comienza en otro número

```markdown
5. Quinto paso
6. Sexto paso
7. Séptimo paso
```

Resultado:

5. Quinto paso
6. Sexto paso
7. Séptimo paso

### 6.7 Listas anidadas

Para crear subniveles, indenta los elementos secundarios con espacios:

```markdown
- Proyecto
  - Planeación
    - Requisitos
    - Cronograma
  - Ejecución
    - Desarrollo
    - Pruebas
  - Cierre
```

Resultado:

- Proyecto
  - Planeación
    - Requisitos
    - Cronograma
  - Ejecución
    - Desarrollo
    - Pruebas
  - Cierre

### 6.8 Lista numerada con subelementos

1. Análisis
   - Identificar las fuentes.
   - Documentar los requisitos.
2. Diseño
   - Definir la arquitectura.
   - Validar el modelo.
3. Implementación
   - Desarrollar la solución.
   - Ejecutar las pruebas.

### 6.9 Números romanos escritos manualmente

Markdown no incluye una numeración automática romana. Puedes escribir los números romanos como parte del texto de cada viñeta:

- **I. Introducción**
- **II. Alcance**
- **III. Diseño**
- **IV. Implementación**
- **V. Conclusiones**

Para subapartados:

- **I. Introducción**
  - **i.** Contexto
  - **ii.** Objetivo
- **II. Desarrollo**
  - **i.** Análisis
  - **ii.** Resultados

El número romano no se incrementa automáticamente; debes editarlo manualmente.

Markdown estándar no incluye un marcador automático de números romanos. Puedes escribirlos manualmente como en los ejemplos anteriores. Si aceptas HTML (no Markdown puro), algunos renderizadores también muestran listas romanas mediante `<ol type="I">` o `<ol type="i">`:

<ol type="I">
  <li>Introducción</li>
  <li>Alcance</li>
  <li>Diseño</li>
  <li>Implementación</li>
</ol>

<ol type="i">
  <li>Primer detalle</li>
  <li>Segundo detalle</li>
  <li>Tercer detalle</li>
</ol>

También existen los tipos alfabéticos:

<ol type="A">
  <li>Alternativa A</li>
  <li>Alternativa B</li>
</ol>

<ol type="a">
  <li>Opción a</li>
  <li>Opción b</li>
</ol>


### 6.10 Lista de verificación con símbolos

Las casillas de tareas `- [ ]` pertenecen a GFM y su representación depende del visor. Para una lista visual sencilla sin depender de controles especiales, puedes utilizar caracteres Unicode.

Sintaxis habitual de GitHub Flavored Markdown (GFM):

```markdown
- [x] Actividad terminada
- [ ] Actividad pendiente
- [ ] Actividad en proceso
```

Las casillas `- [ ]` y `- [x]` son una extensión GFM y su presentación puede variar entre renderizadores. Si el visor de destino no las representa como casillas, utiliza la alternativa simple con símbolos Unicode:

- ☑ Actividad completada
- ☐ Actividad pendiente
- ◐ Actividad en progreso
- ⚠ Actividad que requiere revisión

### 6.11 Listas con párrafos y varios renglones

- **Primer elemento:** este elemento contiene una explicación más larga que puede continuar en el siguiente renglón del mismo párrafo.

  Este es un segundo párrafo que pertenece al primer elemento de la lista.

- **Segundo elemento:** continúa la lista después del párrafo anterior.

### 6.12 Lista de pasos con explicaciones

1. **Preparar:** identificar los archivos de entrada y validar sus formatos.
2. **Procesar:** ejecutar las transformaciones y registrar los resultados.
3. **Verificar:** comparar los resultados con los criterios de aceptación.
4. **Documentar:** guardar evidencias, observaciones y conclusiones.

---

## 7. Citas, notas y bloques informativos

### 7.1 Cita sencilla

```markdown
> Esta es una cita o una observación tomada de otra fuente.
```

Resultado:

> Esta es una cita o una observación tomada de otra fuente.

### 7.2 Cita con varios párrafos

> Este es el primer párrafo de la cita.
>
> Este es el segundo párrafo de la misma cita.

### 7.3 Citas anidadas

> Nivel de cita principal.
>
> > Nivel de cita secundario.
> >
> > > Nivel de cita terciario.

### 7.4 Notas y advertencias

Markdown no define tipos de recuadros de colores para notas. Una alternativa estándar es utilizar citas y etiquetas de texto:

> **NOTA:** utiliza este espacio para aclaraciones importantes.

> **CONSEJO:** incluye aquí una recomendación práctica.

> **ADVERTENCIA:** documenta riesgos, dependencias o acciones que requieren validación.

> **ERROR:** describe el problema y su impacto.

> **ÉXITO:** registra el resultado alcanzado y su evidencia.

### 7.5 Cita con atribución

> La calidad de los datos debe evaluarse mediante reglas definidas, medibles y verificables.
>
> — **Fuente:** nombre del documento o autor, fecha y enlace.

### 7.6 Bloque de texto de referencia

> **Definición — ETL**  
> ETL significa *Extract, Transform, Load*: extraer, transformar y cargar datos.
>
> **Definición — ELT**  
> ELT significa *Extract, Load, Transform*: extraer, cargar y transformar datos.


### 7.7 Texto de autor y fuente

> “La calidad de los datos depende de controles definidos, medibles y verificables.”
>
> — Ejemplo de cita, **fuente:** nombre del documento o autor, fecha y enlace.


---

## 8. Enlaces y referencias

### 8.1 Enlace directo

Sintaxis:

```markdown
[Documentación de Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown)
```

Resultado: [Documentación de Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown).

### 8.2 URL visible como texto

Escribe la dirección completa como enlace entre signos angulares:

```markdown
<https://code.visualstudio.com/>
```

Resultado: <https://code.visualstudio.com/>

### 8.3 Enlace de correo electrónico

```markdown
<mailto:equipo@example.com>
```

Resultado: <mailto:equipo@example.com>

### 8.4 Enlace con referencia

Puedes definir el destino una sola vez y reutilizarlo en el documento:

```markdown
Consulta la [documentación oficial][vscode].
También puedes revisar la [especificación CommonMark][commonmark].

[vscode]: https://code.visualstudio.com/docs/languages/markdown
[commonmark]: https://commonmark.org/
```

Resultado: consulta la [documentación oficial][vscode] y la [especificación CommonMark][commonmark].

[vscode]: https://code.visualstudio.com/docs/languages/markdown
[commonmark]: https://commonmark.org/

### 8.5 Referencia abreviada

```markdown
Consulta la [documentación oficial][] para obtener más información.

[documentación oficial]: https://code.visualstudio.com/docs/languages/markdown
```

### 8.6 Enlace interno a otra sección

```markdown
[Consultar la sección de listas](#6-listas)
```

[Consultar la sección de listas](#6-listas)

### 8.7 Enlace a otro archivo Markdown

Las rutas relativas permiten conectar documentos del mismo repositorio:

```markdown
[Arquitectura](./Arquitectura.md)
[Guía de instalación](./docs/Instalacion.md)
[Sección de componentes](./Arquitectura.md#componentes-principales)
```

### 8.8 Referencias bibliográficas numeradas

Markdown básico no define notas al pie automáticas. Puedes organizar las fuentes como una lista numerada y enlazarlas desde el texto:

Consulta la documentación de [CommonMark][fuente-1] y la guía de [Markdown de VS Code][fuente-2].

1. [CommonMark Specification][fuente-1]
2. [Visual Studio Code — Markdown][fuente-2]

[fuente-1]: https://spec.commonmark.org/
[fuente-2]: https://code.visualstudio.com/docs/languages/markdown

### 8.9 Enlaces con título emergente

```markdown
[CommonMark](https://spec.commonmark.org/ "Especificación de Markdown")
```

Resultado: [CommonMark](https://spec.commonmark.org/ "Especificación de Markdown").

---

## 9. Imágenes

### 9.1 Imagen local

```markdown
![Diagrama de arquitectura](./images/arquitectura.png)
```

### 9.2 Imagen alojada en Internet

```markdown
![Descripción de la imagen](https://example.com/imagen.png)
```

### 9.3 Imagen con referencia

```markdown
![Diagrama del sistema][diagrama-sistema]

[diagrama-sistema]: ./images/diagrama-sistema.png "Diagrama general del sistema"
```

### 9.4 Imagen que también funciona como enlace

```markdown
[![Texto alternativo](./images/diagrama.png)](https://example.com/)
```

### 9.5 Recomendaciones para imágenes

- Utiliza rutas relativas para imágenes almacenadas junto al proyecto.
- Guarda los recursos en carpetas como `images/` o `assets/`.
- Escribe un texto alternativo descriptivo entre los corchetes.
- Comprueba que el archivo existe y que la ruta coincide en mayúsculas y minúsculas.
- Para imágenes remotas, considera que el destino donde publiques el Markdown debe permitir cargar ese recurso.

---

## 10. Tablas y alineación (GFM)

Las tablas con barras verticales son una extensión de uso común conocida como GitHub Flavored Markdown (GFM). No forman parte del núcleo estricto de CommonMark, pero se muestran en la vista previa integrada de VS Code sin necesidad de CSS personalizado.

En VS Code, la vista previa integrada muestra estas tablas sin que tengas que añadir una hoja CSS. Markdown/GFM ofrece tablas sencillas mediante barras verticales (`|`) y una fila separadora con guiones (`-`). Los dos puntos (`:`) de esa fila controlan la alineación. El estilo visual de los bordes depende del tema y del renderizador.

### 10.1 Ejemplo mínimo de tabla

```markdown
| ID | Nombre | Estado |
|----|--------|--------|
| 1  | Cliente | Activo |
| 2  | Producto | Pendiente |
```

| ID | Nombre | Estado |
|----|--------|--------|
| 1 | Cliente | Activo |
| 2 | Producto | Pendiente |


### 10.2 Tabla con tres registros

```markdown
| ID | Nombre | Estado |
|----|--------|--------|
| 1  | Cliente | Activo |
| 2  | Producto | Pendiente |
| 3  | Factura | Completado |
```

Resultado:

| ID | Nombre | Estado |
|----|--------|--------|
| 1 | Cliente | Activo |
| 2 | Producto | Pendiente |
| 3 | Factura | Completado |

### 10.3 Tabla con alineación a la izquierda, centro y derecha


```markdown
| Columna izquierda | Columna centrada | Columna derecha |
|:------------------|:----------------:|----------------:|
| Texto a la izquierda | Texto al centro | 100 |
| Otro texto | Otro valor | 2500 |
```

| Columna izquierda | Columna centrada | Columna derecha |
|:------------------|:----------------:|----------------:|
| Texto a la izquierda | Texto al centro | 100 |
| Otro texto | Otro valor | 2500 |

Regla de alineación:

| Sintaxis del separador | Alineación |
|:--|:--|
| `:---` | Izquierda |
| `:---:` | Centro |
| `---:` | Derecha |
| `---` | Predeterminada (normalmente izquierda) |


```markdown
| Izquierda | Centro | Derecha |
|:----------|:------:|--------:|
| Texto A   | Texto B | 100 |
| Texto C   | Texto D | 2500 |
```

Resultado:

| Izquierda | Centro | Derecha |
|:----------|:------:|--------:|
| Texto A | Texto B | 100 |
| Texto C | Texto D | 2500 |

### 10.4 Reglas de alineación

| Sintaxis de la fila separadora | Alineación |
|:--|:--|
| `|:------|` | Izquierda |
| `|:-----:|` | Centro |
| `|------:|` | Derecha |
| `|------|` | Alineación predeterminada del visor |

### 10.5 Tabla con texto largo

| Área funcional | Descripción | Observación |
|:--|:--|:--|
| Integración | Obtiene datos desde los sistemas fuente y los entrega al destino correspondiente. | Validar registros y errores. |
| Almacenamiento | Conserva información histórica y operacional. | Definir retención y acceso. |
| Analítica | Presenta indicadores y resultados del negocio. | Verificar definiciones de KPI. |

### 10.6 Tabla con código en las celdas

| Elemento | Ejemplo | Descripción |
|:--|:--|:--|
| SQL | `SELECT * FROM dbo.Clientes;` | Consulta SQL |
| Python | `print("Hola")` | Instrucción Python |
| Archivo | `config.json` | Archivo JSON |

### 10.7 Tabla con énfasis

| Prioridad | Estado | Acción |
|:--|:--|:--|
| **Alta** | **Pendiente** | Revisar hoy |
| Media | *En progreso* | Dar seguimiento |
| Baja | Completado | Archivar evidencia |

### 10.8 Tabla con celdas vacías

| ID | Responsable | Comentario |
|:--|:--|:--|
| 1 | Ana | Validado |
| 2 | Luis | |
| 3 | | Pendiente de asignación |

### 10.9 Limitaciones de bordes y estilos

La sintaxis Markdown de tablas no permite elegir el estilo de las líneas. El borde, el color y el espaciado se determinan por el motor de visualización y su tema. Por tanto, con esta plantilla nativa:

- Puedes crear tablas con `|` y filas separadoras de guiones.
- Puedes alinear columnas a la izquierda, al centro o a la derecha.
- No puedes solicitar mediante Markdown puro una tabla sin bordes, con bordes dobles, punteados o con colores particulares.
- No se incluyen tablas HTML ni reglas CSS para conseguir esos efectos.

---

## 11. Bloques de código

### 11.1 Código en línea

Puedes incluir una instrucción dentro de un párrafo: ejecuta `SELECT * FROM dbo.Clientes;` y revisa la variable `customer_id`.

Escribe `SELECT * FROM dbo.Customers;` dentro de una oración utilizando un solo acento grave a cada lado.

### 11.2 Bloque de código sin identificar un lenguaje (Bloque de código sin resaltado)

```
Este es un bloque de texto plano.
No aplica colores de sintaxis específicos de un lenguaje.
Se utiliza para logs, salidas de consola o texto literal.
```
---

````markdown
```
Este es un bloque de texto literal.
Puede utilizarse para mostrar una salida breve o contenido sin resaltado específico.
```
````

Resultado:

```
Este es un bloque de texto literal.
Puede utilizarse para mostrar una salida breve o contenido sin resaltado específico.
```

### 11.3 Bloque de texto plano

```text
2026-11-02 08:30:00 INFO  Inicio del proceso ETL
2026-11-02 08:30:05 INFO  Registros leídos: 1250
2026-11-02 08:30:09 WARN  Se encontraron 3 registros incompletos
2026-11-02 08:30:12 INFO  Proceso finalizado
```

### 11.4 Bloque con número de línea

Markdown no define una opción universal para numerar las líneas de un bloque de código. El visor puede mostrar números según su implementación o configuración. Si necesitas que los números formen parte del texto, escríbelos en el propio bloque:

```text
1  Primera instrucción
2  Segunda instrucción
3  Tercera instrucción
```

### 11.5 Bloques de código anidados

Si necesitas mostrar un bloque de código Markdown dentro de otro bloque de código, utiliza cuatro acentos graves en el bloque exterior:

````markdown
```python
print("Este bloque aparece dentro de otro ejemplo")
```
````

### 11.6 Bloque de código delimitado con virgulillas

También puedes utilizar tres virgulillas (`~`) como delimitador:

~~~text
Este bloque se abre y se cierra con tres virgulillas.
~~~

### 11.7 Recomendaciones

- Especifica el lenguaje después de los tres acentos graves para activar el resaltado de sintaxis.
- Utiliza `text` cuando no quieras un resaltado específico.
- Mantén la indentación del código para que sea legible.
- El resaltado de sintaxis solo colorea el código; no lo ejecuta ni valida.

---

## 12. Ejemplos de distintos lenguajes

El identificador que se escribe después de los tres acentos graves indica al visor qué gramática de resaltado utilizar. Estos identificadores son habituales en VS Code; el resultado exacto depende de la gramática disponible.

### 12.1 Texto plano — `text`

```text
Proceso: carga de clientes
Estado: completado
Registros leídos: 1250
Registros rechazados: 3
Duración: 00:00:12
```

### 12.2 SQL — `sql`

```sql
SELECT
    CustomerID,
    CustomerName,
    CreatedDate
FROM dbo.Customers
WHERE IsActive = 1
ORDER BY CreatedDate DESC;
```

### 12.3 T-SQL — `sql`

```sql
DECLARE @StartDate date = '2026-01-01';
DECLARE @EndDate   date = '2027-01-01';

SELECT COUNT(*) AS TotalOrders
FROM dbo.Orders
WHERE OrderDate >= @StartDate
  AND OrderDate <  @EndDate;
```

### 12.4 Python — `python`

```python
from collections import Counter

records = ["SQL", "Python", "SQL", "ETL", "Python", "SQL"]
counts = Counter(records)

for name, quantity in counts.items():
    print(f"{name}: {quantity}")
```

### 12.5 C# — `csharp`

```csharp
using System;

public class Customer
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;

    public void Print()
    {
        Console.WriteLine($"Customer: {Name}");
    }
}
```

### 12.6 C — `c`

```c
#include <stdio.h>

int main(void)
{
    printf("Hello, Markdown!\n");
    return 0;
}
```

### 12.7 C++ — `cpp`

```cpp
#include <iostream>
#include <string>

int main()
{
    std::string message = "Hello, Markdown!";
    std::cout << message << std::endl;
    return 0;
}
```

### 12.8 BASIC — `basic`

```basic
10 REM Example in classic BASIC
20 LET TOTAL = 10 + 20
30 PRINT "TOTAL = "; TOTAL
40 END
```

### 12.9 Visual Basic / VB.NET — `vbnet`

```vbnet
Module Program
    Sub Main()
        Dim customerName As String = "Ana"
        Console.WriteLine("Customer: " & customerName)
    End Sub
End Module
```

### 12.10 XML — `xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<customers>
    <customer id="1001">
        <name>Ana López</name>
        <status>Active</status>
    </customer>
</customers>
```

### 12.11 HTML como código fuente — `html`

El siguiente ejemplo se muestra como código, no se interpreta como diseño HTML de este documento:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo HTML</title>
</head>
<body>
    <h1>Hola, Markdown</h1>
    <p>Este HTML está dentro de un bloque de código.</p>
</body>
</html>
```

### 12.12 JSON — `json`

```json
{
  "customerId": 1001,
  "customerName": "Ana López",
  "isActive": true,
  "orders": 3,
  "tags": ["VIP", "Retail"]
}
```

### 12.13 YAML — `yaml`

```yaml
application:
  name: data-platform
  environment: development
  enabled: true
  owners:
    - data-engineering
    - analytics
```

### 12.14 JavaScript — `javascript`

```javascript
const customers = ["Ana", "Luis", "Sofía"];

customers.forEach((customer) => {
    console.log(`Customer: ${customer}`);
});
```

### 12.15 TypeScript — `typescript`

```typescript
interface Customer {
    id: number;
    name: string;
}

const customer: Customer = { id: 1001, name: "Ana" };
console.log(customer.name);
```

### 12.16 Java — `java`

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, Markdown!");
    }
}
```

### 12.17 Bash / Shell — `bash`

```bash
#!/usr/bin/env bash
set -euo pipefail

echo "Starting process"
python --version
```

### 12.18 PowerShell — `powershell`

```powershell
$CustomerName = "Ana"
Write-Output "Customer: $CustomerName"
Get-Date
```

### 12.19 CSS como código fuente — `css`

Este bloque es únicamente un ejemplo de código CSS; no modifica el estilo de esta plantilla:

```css
.notice {
    color: #1565C0;
    background-color: #E3F2FD;
    padding: 8px;
}
```

### 12.20 Diff — `diff`

```diff
- STATUS = "PENDING"
+ STATUS = "COMPLETED"
  RETRIES = 3
```

### 12.21 Markdown dentro de un bloque — `markdown`

````markdown
# Título de ejemplo

- Elemento uno
- Elemento dos

**Texto en negrita**
````

### 12.22 Otros identificadores que puedes probar

VS Code dispone de resaltado para muchos lenguajes y formatos. Algunos identificadores habituales son:

| Identificador | Lenguaje o formato |
|:--|:--|
| `go` | Go |
| `rust` | Rust |
| `ruby` | Ruby |
| `php` | PHP |
| `r` | R |
| `kotlin` | Kotlin |
| `swift` | Swift |
| `scala` | Scala |
| `dockerfile` | Dockerfile |
| `ini` | Archivos INI |
| `toml` | TOML |
| `makefile` | Makefile |
| `graphql` | GraphQL |
| `powershell` | PowerShell |
| `plaintext` o `text` | Texto sin lenguaje específico |

Si no se aplica el resaltado, prueba el identificador habitual del lenguaje o deja el bloque sin identificador.

---

## 13. Árboles de carpetas y jerarquías

Markdown no posee una sintaxis especial para árboles de directorios. Una forma portable es escribir la estructura dentro de un bloque de código `text` y utilizar caracteres Unicode de líneas.

### 13.1 Árbol de directorios

```text
Workspace/
├── Documentation/
│   ├── Architecture.md
│   ├── Data_Model.md
│   └── User_Guide.md
├── Source/
│   ├── API/
│   ├── Database/
│   └── Web/
├── Tests/
│   ├── Unit/
│   └── Integration/
└── README.md
```

### 13.2 Jerarquía de proyecto

```text
Workspace
├── Space: Personal
│   ├── Folder: Learning
│   │   ├── List: Python
│   │   ├── List: SQL
│   │   └── List: Data Engineering
│   └── Folder: Personal Projects
└── Space: Work
    ├── Folder: Client A
    │   ├── List: Backlog
    │   └── List: Issues
    └── Folder: Client B
        └── List: Backlog
```

### 13.3 Caracteres útiles

| Carácter | Uso |
|:--:|:--|
| `├──` | Rama que continúa en el mismo nivel |
| `└──` | Última rama del nivel |
| `│` | Línea vertical de continuidad |
| `──` | Línea horizontal |
| `   ` | Espacios de indentación |

---

## 14. Símbolos y caracteres especiales

Puedes utilizar directamente caracteres Unicode en el texto Markdown. Su apariencia depende de la fuente y del sistema operativo.

| Símbolo | Uso habitual |
|:--:|:--|
| ✓ | Correcto |
| ✗ | Incorrecto |
| ⚠ | Advertencia |
| ℹ | Información |
| ★ | Destacado o favorito |
| → | Flujo o dirección |
| ← | Dirección inversa |
| ↑ / ↓ | Arriba / abajo |
| • | Viñeta |
| … | Continuación |
| © | Copyright |
| ® | Marca registrada |
| ™ | Marca comercial |
| € / $ / £ | Monedas |
| ≤ / ≥ / ≠ / ≈ | Operadores matemáticos |
| → / ⇒ | Dirección o implicación |
| × / ÷ / ± | Operadores matemáticos |

Ejemplo de estados: ✅ Completado · 🟡 En progreso · ⏳ Pendiente · ❌ Fallido · 🔍 En revisión.

### 14.1 Caracteres comunes en documentación técnica

- Flechas: `←` `→` `↔` `↑` `↓` `⇒` `⇐`
- Matemáticas: `±` `×` `÷` `≈` `≠` `≤` `≥` `∞`
- Viñetas: `•` `◦` `▪` `▫`
- Casillas: `☐` `☑` `☒`
- Estados: `✓` `✗` `⚠` `ℹ`

---

### 14.2 Catálogo ampliado de símbolos y emojis

Puedes utilizar directamente muchos caracteres Unicode:

| Símbolo | Significado o uso |
|:--:|:--|
| ✓ | Correcto |
| ✗ | Incorrecto |
| ⚠ | Advertencia |
| ℹ | Información |
| ★ | Favorito / destacado |
| → | Flujo o dirección |
| ← | Dirección inversa |
| ↑ ↓ | Arriba / abajo |
| • | Viñeta |
| … | Continuación |
| © | Copyright |
| ® | Marca registrada |
| ™ | Marca comercial |
| € $ £ | Monedas |
| ≤ ≥ ≠ ≈ | Operadores matemáticos |

Ejemplo de estados: ✅ Completado · 🟡 En progreso · ⏳ Pendiente · ❌ Fallido · 🔍 En revisión.

### 14.3 Entidades HTML

También puedes escribir entidades HTML:

```html
&amp;   &lt;   &gt;   &quot;   &copy;   &nbsp;
```

Resultado: &amp; &lt; &gt; &quot; &copy;.

---

## 15. Escapar caracteres de Markdown

Algunos caracteres tienen significado especial en Markdown. Si deseas mostrarlos literalmente, coloca una barra invertida `\` antes del carácter.

### 15.1 Ejemplos de escape

```markdown
\*Esto no será cursiva\*
\# Esto no será un encabezado
\- Esto no será una viñeta
\[Esto no será un enlace\]
\> Esto no será una cita
\`Esto no será código en línea\`
```

Resultado:

\*Esto no será cursiva\*

\# Esto no será un encabezado

\- Esto no será una viñeta

\[Esto no será un enlace\]

\> Esto no será una cita

\`Esto no será código en línea\`

### 15.2 Caracteres que pueden escaparse

Entre los caracteres de puntuación que se pueden escapar están:

```text
\  `  *  _  {  }  [  ]  (  )  #  +  -  .  !  |
```

Dentro de una tabla, utiliza `\|` si necesitas mostrar una barra vertical como contenido de una celda.

---

## 16. HTML dentro de Markdown

VS Code permite utilizar determinados elementos HTML en el preview Markdown, sujeto a las reglas de seguridad y sanitización del visor. HTML no es sintaxis Markdown y el soporte de etiquetas y atributos puede variar entre renderizadores.

---

## 21. Front Matter YAML

El *front matter* es un bloque YAML opcional situado al principio del archivo Markdown, antes del contenido del documento. Se utiliza para registrar metadatos como título, fecha, autor, etiquetas o idioma. El ejemplo siguiente está dentro de un bloque de código para mostrar su sintaxis; para usarlo como metadatos reales, copia el bloque al inicio de otro archivo `.md` y quita los delimitadores de código.

Ejemplo:

```yaml
---
title: "Documento de arquitectura"
author: "Nombre del autor"
date: 2026-11-02
status: "Draft"
tags:
  - architecture
  - data
  - documentation
---
```

En VS Code 1.121 y posteriores, el preview integrado representa el front matter como una tabla de forma predeterminada. La opción `markdown.preview.frontMatter` permite cambiar la presentación a `table`, `codeBlock` o `hide`. Algunos generadores de sitios estáticos también utilizan el front matter para controlar la publicación del documento.

---
---

## 26. Resumen rápido de sintaxis

| Necesidad | Sintaxis |
|:--|:--|
| Encabezado H1 | `# Título` |
| Encabezado H2 | `## Título` |
| Encabezado H3 | `### Título` |
| Encabezado H4 | `#### Título` |
| Encabezado H5 | `##### Título` |
| Encabezado H6 | `###### Título` |
| Negrita | `**texto**` |
| Cursiva | `*texto*` |
| Negrita y cursiva | `***texto***` |
| Tachado (GFM) | `~~texto~~` |
| Código en línea | `` `código` `` |
| Cita | `> texto` |
| Viñeta | `- elemento` |
| Lista numerada | `1. elemento` |
| Separador horizontal | `---` |
| Enlace | `[texto](URL)` |
| Imagen | `![descripción](ruta)` |
| Enlace con referencia | `[texto][id]` y `[id]: URL` |
| Bloque de código | ```` ```lenguaje ```` |
| Tabla (GFM) | `| columna | columna |` |
| Alinear tabla a la izquierda | `:---` |
| Alinear tabla al centro | `:---:` |
| Alinear tabla a la derecha | `---:` |
| Mostrar un carácter especial | `\carácter` |

---

## 27. Referencias oficiales

### Especificaciones y guías generales

- [CommonMark Specification](https://spec.commonmark.org/): especificación del núcleo de Markdown.
- [GitHub Flavored Markdown Specification](https://github.github.com/gfm/): especificación de extensiones como tablas, tachado y listas de tareas.
- [Markdown Guide](https://www.markdownguide.org/): tutorial y referencia de sintaxis.

### Documentación de Visual Studio Code

- [Visual Studio Code — Markdown](https://code.visualstudio.com/docs/languages/markdown): vista previa, enlaces, imágenes, Mermaid, fórmulas KaTeX, Front Matter, seguridad y estilos CSS personalizados.
- [VS Code 1.121 — Mermaid diagrams in Markdown preview and YAML front matter](https://code.visualstudio.com/updates/v1_121/): incorporación de Mermaid y opciones de presentación del Front Matter.
- [VS Code — Markdown Extension API](https://code.visualstudio.com/api/extension-guides/markdown-extension): cómo las extensiones incorporan sintaxis y estilos al preview.

---

**Fin de la guía.** Conserva este archivo como catálogo de referencia y copia los fragmentos que necesites en tus propios documentos Markdown.

---
---
---
-- =====================  
-- **Fin de la guía.**  
-- =====================  
·  

---
---
---
-- =====================  
-- **Inicio notas Yimmy en Derevo**  
-- =====================  
·  
·  
Handbook Derevo  
·  



001.010 
002.010 
002.020 
002.030 
002.040 
002.050 
002.060 
002.070 
002.080 
002.090 
002.100 
002.110 
002.120 
002.130 
002.140 

003.010 
003.020 
003.030 
003.040 





https://example.avatar.service/u/{email}/avatar.png


yimmy.rengifo@derevo.com.mx

https://example.avatar.service/u/yimmy.rengifo@derevo.com.mx/avatar.png



---
---
---
-- =====================  
-- **Meeting yyyy-mmm-dd _______**  
-- =====================  
·  
-- =====================  
-- **EOF**  
-- =====================  
°°°°°°°  
·  