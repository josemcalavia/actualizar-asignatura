# Actualizar asignatura

[![Licencia: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23249239.svg)](https://doi.org/10.5281/zenodo.23249239)

Diseño original: **José María Calavia Balduz** · Licencia CC BY-NC-SA 4.0

Una skill para Claude que organiza la carpeta de una asignatura universitaria la primera vez y, en las sesiones siguientes, actualiza la guía docente, el calendario, la bibliografía, los materiales y el benchmarking con otras universidades, según los trabajos que elija el docente.

## Para quién es

Para profesorado universitario que quiere tener su asignatura ordenada en una sola carpeta y revisarla cada curso con ayuda de IA: comprobar la coherencia entre guía, actividades y evaluación, verificar y actualizar referencias, compararse con asignaturas equivalentes y producir materiales nuevos. No hace falta saber programar.

## Qué hace

- **Modo Arranque** (primera vez): crea una estructura de carpetas estándar, recoge por secciones la guía, el calendario, los materiales, la fundamentación y la bibliografía, y te deja elegir trabajos.
- **Modo Trabajo** (sesiones posteriores): lee la ficha y el registro de cambios, detecta archivos nuevos y continúa lo pendiente.
- **Catálogo de trabajos**: inventario y mapa (T1), coherencia interna (T2), actualización bibliográfica (T3), benchmarking (T4), propuesta de cambios (T5), producción de materiales (T6) y calendario del nuevo curso (T7).

Los originales no se modifican nunca: todo lo generado va a `06 Salidas`, y las decisiones pedagógicas son siempre del docente.

## Qué necesitas

- Una cuenta de Claude con skills disponibles (Claude Pro o superior), en la web, la aplicación de escritorio o Claude Code.
- Para trabajar con carpetas de tu ordenador, la aplicación de escritorio de Claude o Claude Code.

## Instalación

### En Claude (web o aplicación de escritorio)

1. Descarga [`descarga/actualizar-asignatura.skill`](descarga/actualizar-asignatura.skill) o el mismo archivo adjunto en la [última versión](https://github.com/josemcalavia/actualizar-asignatura/releases/latest).
2. En Claude, ve a **Ajustes**, **Capacidades**, sección de skills.
3. Pulsa para subir una skill y elige el archivo `.skill`.
4. Comprueba que aparece activada.

### En Claude Code

Copia la carpeta [`actualizar-asignatura/`](actualizar-asignatura) de este repositorio en `~/.claude/skills/`:

```bash
git clone https://github.com/josemcalavia/actualizar-asignatura.git
cp -R actualizar-asignatura/actualizar-asignatura ~/.claude/skills/
```

Reinicia Claude Code para que la detecte.

## Uso básico

Escribe algo como:

> Quiero actualizar mi asignatura de Desarrollo motor.

La skill te pregunta en qué carpeta está la asignatura. Si es la primera vez, la organiza y recoge el contenido; si ya existe la `Ficha de asignatura.md`, te muestra el estado y te pregunta qué trabajo quieres hacer hoy. También puedes pedir un trabajo concreto, por ejemplo:

> Actualiza la bibliografía de la asignatura.
> Compárala con otras universidades.

Revisa siempre lo que genere antes de usarlo: está hecho con IA y quien lo usa responde de su contenido.

## Qué hay en el repositorio

| Archivo | Para qué sirve |
|---|---|
| `actualizar-asignatura/SKILL.md` | Instrucciones de la skill |
| `actualizar-asignatura/LICENCIA.md` | Condiciones de uso, dentro de la skill |
| `descarga/actualizar-asignatura.skill` | Paquete listo para subir a Claude |
| `LICENCIA.md`, `LICENSE` | Condiciones de uso y texto legal de la licencia |
| `CITATION.cff`, `.zenodo.json` | Metadatos para citar y archivar en Zenodo |

## Autoría

**José María Calavia Balduz** ([ORCID 0009-0001-7105-2022](https://orcid.org/0009-0001-7105-2022)), CSEU La Salle (adscrito a la UAM) y Centro Tangram.
Contacto: josemcalavia@me.com

## Licencia

[Creative Commons Reconocimiento-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es). Puedes usarla, compartirla y adaptarla sin fines comerciales, manteniendo la autoría original y la misma licencia. Los materiales que generes con ella son tuyos o de tu institución. Detalles en [`LICENCIA.md`](LICENCIA.md).

## Cómo citar

Calavia Balduz, J. M. (2026). *Actualizar asignatura: skill para Claude* (Versión 1.0.0) [Software]. Zenodo. https://doi.org/10.5281/zenodo.23249239

Este DOI (10.5281/zenodo.23249239) agrupa todas las versiones y siempre apunta a la más reciente; cada versión tiene además su propio DOI en Zenodo. También puedes usar el botón «Cite this repository» de GitHub, que lee `CITATION.cff`.
