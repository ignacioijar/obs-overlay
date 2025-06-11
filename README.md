# OBS Overlay - Artemis vs Seirit

Este proyecto es un overlay para OBS que muestra dos gráficos de barras actualizables con datos tomados en tiempo real desde una hoja de Google Sheets.

---

## Cómo funciona

- Usa Google Sheets para almacenar datos numéricos para dos equipos: **Artemis** y **Seirit**.
- El overlay consulta la hoja cada 10 segundos y actualiza las barras automáticamente.
- Ideal para streaming o presentaciones en vivo.

---

## Preparar Google Sheets

1. Crea una hoja con esta estructura:

| Equipo  | A  | B  | C  |
|---------|----|----|----|
| Artemis | 10 | 20 | 15 |
| Seirit  | 5  | 12 | 18 |

2. Publica la hoja en la web:  
   **Archivo > Publicar en la web** y selecciona toda la hoja.

3. Copia el ID de la hoja de la URL, ejemplo:  
   `https://docs.google.com/spreadsheets/d/ID_DE_LA_HOJA/edit`

4. Pega ese ID en el archivo `index.html` en la línea:

```js
const sheetId = 'ID_DE_LA_HOJA';
