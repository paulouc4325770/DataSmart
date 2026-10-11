# DataSmart - Primera fase: EDA de Olist

## Ejecutar en Windows (PowerShell)
1. Descomprimir este proyecto en una carpeta, por ejemplo `C:\DataSmart_EDA`.
2. Abrir una terminal en la carpeta que contiene `requirements.txt`.
3. Ejecutar `py -m pip install -r requirements.txt`.
4. Ejecutar `py src/eda_olist.py`.

Si `py` no funciona, usa `python` en los comandos.

El ZIP original debe encontrarse en `data/raw/archive.zip` (ya viene incluido).

## Resultados
- `resultados/resumen_tablas.csv`: filas, columnas, nulos y duplicados exactos por tabla.
- `resultados/diccionario_perfilado.csv`: columnas, tipos inferidos, nulos, valores distintos.
- `resultados/indicadores_kpi.csv`: métricas descriptivas básicas.
- `resultados/ventas_mensuales.csv`: serie temporal de importes.
- `resultados/graficos/`: tres visualizaciones PNG.

## Notas metodológicas
- El dataset Olist es histórico y no representa ventas actuales.
- Las ventas reportadas suman `price` de artículos de pedidos entregados y excluyen flete.
- El estado `delivered` se utiliza como filtro para un análisis inicial, no como tratamiento final de todos los datos.
- Los tipos en `diccionario_perfilado.csv` son los inferidos por Pandas, no los tipos definitivos de SQL.
- No eliminar faltantes ni duplicados sin revisar su significado y las claves de las tablas.
