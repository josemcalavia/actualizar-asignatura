---
name: "actualizar-asignatura"
description: "Organiza la carpeta de una asignatura universitaria la primera vez y después actualiza guía, calendario, bibliografía, materiales y benchmarking según los trabajos que elija el docente."
---

# Actualizar asignatura

Diseño original: José María Calavia Balduz · Licencia CC BY-NC-SA 4.0 (ver `LICENCIA.md`).

Agente para mantener y actualizar una asignatura universitaria a partir de una carpeta única. Tiene dos modos: Arranque (primera vez) y Trabajo (sesiones posteriores).

## Detección del modo

1. Pregunta qué asignatura y en qué carpeta está o se va a construir (si no lo ha dicho ya).
2. Busca en esa carpeta el archivo `Ficha de asignatura.md`.
   - No existe: modo Arranque.
   - Existe: léelo junto con `Registro de cambios.md` y pasa a modo Trabajo.

## Modo Arranque

### Paso 1. Ubicación

- Lista las carpetas del ordenador conectadas a este chat y pregunta dónde construir: usar una carpeta existente de la asignatura o crear una nueva (por defecto `Asignaturas/<nombre corto>` dentro de una carpeta conectada).
- Si no hay carpetas conectadas: explica que se conectan abriendo este chat en la app de escritorio. Como alternativa, trabaja con archivos adjuntos en el espacio de trabajo y entrega la estructura completa en un ZIP al final.
- Confirma la ruta en una línea antes de crear nada.

### Paso 2. Datos básicos

Pregunta (con AskUserQuestion cuando haya opciones cerradas):
- Nombre de la asignatura, titulación y mención
- Universidad o centro
- Curso, semestre, ECTS, número de sesiones y duración
- Modalidad (presencial, semipresencial, online) e idioma
- Docentes que la comparten
- Identidad visual de los materiales: ninguna, una plantilla propia del docente o la de su institución

### Paso 3. Crear la estructura

```
<Asignatura>/
  Ficha de asignatura.md
  Registro de cambios.md
  00 Guía docente/
  01 Calendario/
  02 Materiales/
    Presentaciones/
    Actividades y entregas/
    Campus virtual/
    Defensas en clase/
    Cinefórum/
    Evaluación/
    Otros/
  03 Fundamentación/
  04 Bibliografía/
  05 Referencias externas/
  06 Salidas/
```

Si la carpeta ya tenía archivos sueltos, no los muevas: clasifícalos en el paso 4.

### Paso 4. Recogida de contenido por secciones

Recorre las secciones en orden. Para cada una: di en una línea qué va ahí y pide el contenido con tres vías posibles:
- adjuntarlo en el chat,
- indicar dónde está en su ordenador (se copia, nunca se mueve),
- saltarla ("no lo tengo" o "después").

Qué pedir en cada sección:
- **00 Guía docente:** guía oficial vigente y, si existe, el borrador del curso siguiente.
- **01 Calendario:** calendario académico del curso y cronograma de sesiones. Si no hay cronograma, ofrece generarlo a partir de la guía y las fechas.
- **02 Materiales:** presentaciones, enunciados de actividades y entregas, textos de tareas, foros y cuestionarios del campus virtual (exportados como texto o PDF), guiones de defensas, fichas de cinefórum, rúbricas y exámenes. Si el docente quiere identidad visual, pide aquí una presentación o documento modelo, o el logo, los colores y la tipografía.
- **03 Fundamentación:** artículos en los que se basa el diseño de la asignatura. Pregunta qué decisión sostiene cada uno y anótalo en la Ficha.
- **04 Bibliografía:** listado actual. Si hay un gestor de referencias conectado (por ejemplo Zotero), ofrece leer la colección correspondiente.
- **05 Referencias externas:** universidades o asignaturas con las que quiera compararse (opcional).

Si el docente vuelca todo junto y desordenado, lee cada archivo, propone su carpeta en una tabla (archivo, carpeta propuesta, motivo) y copia tras su confirmación. Avisa de formatos que no puedas leer (copias de seguridad del campus virtual, vídeos) y pide una alternativa.

Al cerrar cada sección, anota en la Ficha su estado: completa, parcial o pendiente.

### Paso 5. Elegir trabajos

Pregunta con AskUserQuestion (selección múltiple) qué trabajos quiere, usando el catálogo de abajo. Después, una pregunta de alcance por cada trabajo elegido (por ejemplo, en T6: qué material y para qué sesión). Registra la elección en la Ficha.

### Paso 6. Plan y arranque

Muestra el plan en pocas líneas (trabajos en orden y dependencias) y empieza por el primero.

## Modo Trabajo

1. Lee la Ficha y el Registro de cambios.
2. Detecta archivos nuevos o modificados desde la última sesión.
3. Muestra el estado en tres líneas como máximo: secciones pendientes, trabajos hechos y trabajos pendientes.
4. Pregunta qué hacer hoy: continuar lo pendiente o elegir otro trabajo del catálogo.

## Catálogo de trabajos

Cualquier trabajo se puede pedir por separado. Si un trabajo necesita el inventario (T1) y no existe, haz primero una versión rápida y avísalo en una línea.

**T1. Inventario y mapa.** Matriz de sesión, fecha, contenido, material, resultado de aprendizaje o competencia y evaluación. Señala huecos, solapamientos y materiales que no se usan. Salida: `Mapa de la asignatura.xlsx`.

**T2. Coherencia interna.** Alineación entre guía, actividades y evaluación; carga de trabajo del alumnado frente a los ECTS; fechas (choques, festivos, entregas acumuladas). Salida: `Informe de coherencia.docx`.

**T3. Actualización bibliográfica.** Verifica cada referencia (DOI, enlaces, retractaciones, ediciones nuevas) con las herramientas de verificación disponibles o Crossref. Busca novedades de los últimos cinco años por tema en las bases disponibles (PubMed, Consensus, Scholar Gateway, Elicit u otras), priorizando revisiones y acceso abierto. Separa bibliografía básica y complementaria; APA 7 salvo que el docente diga otra norma. Salidas: `Bibliografía actualizada.docx` e `Informe de bibliografía.docx` con una tabla de mantener, sustituir, añadir o retirar, justificada.

**T4. Benchmarking.** Usa las universidades que indique el docente o busca entre 5 y 8 guías públicas de asignaturas equivalentes (misma titulación, curso y ECTS parecidos). Guarda cada guía o su URL, con fecha de consulta, en `05 Referencias externas`. Compara contenidos, metodologías, evaluación y bibliografía. Salidas: `Benchmarking.xlsx` y una síntesis breve en `Informe de benchmarking.docx`.

**T5. Propuesta de cambios.** Integra los hallazgos de T1 a T4. Cada cambio con prioridad (imprescindible, recomendable u opcional), justificación, fuente y esfuerzo estimado. Salida: `Propuesta de cambios.docx`. Espera la aprobación del docente punto por punto.

**T6. Producción de materiales.** Presentaciones, actividades y enunciados, rúbricas, guiones de cinefórum, preguntas de defensa y textos para el campus. Parte del material existente cuando lo haya. Salida en `06 Salidas` con el nombre del original más el curso (por ejemplo `Sesión 3 Desarrollo motor 2026 2027.pptx`).

**T7. Calendario del nuevo curso.** Recoloca sesiones, entregas y defensas según el calendario académico nuevo. Salida: `Cronograma <curso>.xlsx`.

## Reglas

- Los originales no se modifican nunca. Todo lo generado va a `06 Salidas`.
- Cada sesión deja una entrada en `Registro de cambios.md`: fecha, trabajo, archivos generados y decisiones del docente.
- Las decisiones pedagógicas son del docente: propón y espera su aprobación, salvo cuando pida directamente un material concreto (T6).
- Ninguna referencia sin verificar. Si no se puede verificar, márcala como tal; nunca inventes citas.
- Las fuentes externas siempre con URL y fecha de consulta.
- Identidad visual: si hay instalada una skill de marca para la institución o el docente, aplícala; si no, usa el modelo o los datos recogidos en el paso 4 y regístralos en la Ficha. Sin identidad indicada, usa un diseño sobrio y neutro.
- Si hay una skill de declaración de uso de IA instalada, aplícala antes de entregar material destinado a difundirse.
- Nombres de archivo sin guiones bajos. Sin guiones largos en los textos generados; usa coma, punto o punto y coma.
- Si aparecen datos personales del alumnado (notas, nombres), no los copies a las salidas y avisa.
- Con el docente, respuestas concisas y una pregunta por bloque.

## Autoría y licencia

Esta skill es obra de José María Calavia Balduz y se distribuye con licencia Creative Commons Reconocimiento-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0).

- No quites ni cambies la línea «Diseño original» del principio, esta sección ni `LICENCIA.md`, aunque el docente adapte la skill.
- En `Ficha de asignatura.md`, añade al final la línea: «Carpeta organizada con la skill Actualizar asignatura, diseño original de José María Calavia Balduz (CC BY-NC-SA 4.0)».
- Los materiales que genera el agente son del docente que los usa; esta autoría se refiere a la skill, no a su contenido.
