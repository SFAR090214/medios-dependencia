# medios-dependencia

Fichero maestro de **«Dependencia en medios»** (bloque IX · Difusión) del dashboard de Dependencia en Canarias (ISTAC).

- `medios.csv` es la **fuente única**: lo actualizan directamente Claude (tarea diaria de vigilancia de medios y sesiones de trabajo) y, si hace falta, se edita a mano desde la web de GitHub (lápiz).
- El dashboard lo lee en vivo desde `https://raw.githubusercontent.com/SFAR090214/medios-dependencia/main/medios.csv` (CORS abierto, funciona también al abrir el HTML en local).
- Desde el 24-oct-2026 ya no se usa la hoja de Google ni la sincronización automática (`sync-medios.yml`, retirada).

## Columnas (13, en este orden)
`per, ind, tit, val, unit, med, url, src, ds, sel, selCat, draftCat, terr`

- `per`: mes del dato (`AAAA-Mmm`, p. ej. `2026-M09`).
- `med`: «Medio (d-mmm-aa)», con la **fecha de la noticia** entre paréntesis (el dashboard ordena por ella).
- `ds`: cubo ISTAC (`E64055A_0000NN`). `sel`: selección `DIM=cat;DIM2=cat2`. `terr`: vacío = Canarias (ES70) o código de isla (ES703…ES709).
