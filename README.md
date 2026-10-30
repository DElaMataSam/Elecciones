# Modelo de estimación electoral · Elecciones generales 29-N 2026

Agregación de encuestas → swing proporcional por provincia → D'Hondt (umbral 3 %) → simulación Montecarlo.

**Dashboard:** activa GitHub Pages (rama `main`, carpeta `/docs`) y estará en `https://TU_USUARIO.github.io/modelo-29n/`

## Método
1. Media ponderada de encuestas (peso = raíz del tamaño muestral y decaimiento a 14 días; una voz por casa).
2. Cada partido se escala en cada provincia según su resultado de 2023 (swing proporcional).
3. Reparto de escaños por D'Hondt provincia a provincia (52 circunscripciones, umbral 3 %).
4. 2.000 simulaciones con ruido nacional (SD 7 %) y provincial (SD 8 %).

## Limitaciones
- El ruido no está calibrado con un backtest (2019, 2023).
- Sumar y Podemos van juntos; no se modelan listas nuevas.
- El swing es uniforme: no recoge diferencias regionales.
- 176 escaños no equivalen a formar gobierno.

## Reproducir
Datos de 2023: Ministerio del Interior (infoelectoral.interior.gob.es), ficheros .DAT. Ejecuta `notebook.ipynb` de arriba abajo.

## Fuentes
- Encuestas: Wikipedia, *Opinion polling for the next Spanish general election* (CC BY-SA).
- Resultados 2023: Ministerio del Interior.
