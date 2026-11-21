# Proyecto 2 – Segunda parte: Regresión Lineal Múltiple

Descripción:

Modelo de Regresión Lineal Múltiple que predice las ventas de un producto (miles de unidades) 
a partir de la inversión en publicidad (miles de dólares) en tres medios:

- tv: inversión en publicidad de TV
- radio: inversión en publicidad de radio
- newspaper: inversión en publicidad en diarios

Dataset: Advertising (Kaggle) – https://www.kaggle.com/ashydv/advertising-dataset – 200 mercados, sin datos faltantes. 
Archivo: advertising.csv.

Conclusiones

¿Cuál fue el desempeño del modelo?

Muy bueno. En Test el R² fue de 0,906: el modelo explica alrededor del 91 % de las variaciones de las ventas. 
El error promedio (MAE) fue de 1,27 miles de unidades y el RMSE de 1,71. 
Como las ventas promedio son de unas 15,1 miles de unidades (y van de 1,6 a 27,0), es un error chico. 
Es decir, el modelo aprendió una relación real.

¿Qué variable fue la más influyente según los coeficientes del modelo?

Los coeficientes son tv = 0,0545, radio = 0,1009 y newspaper = 0,0043 (miles de unidades más por cada mil dólares invertidos). 
Por cada dólar, la radio rinde casi el doble que la TV, y el diario casi no rinde. 
Pero en la práctica, la inversión en TV varía mucho más que la de radio, así que la TV es la que más pesa en las ventas. 
Cuando la inversión en TV cambia un desvío estándar, las ventas cambian unas 4,7 miles de unidades, contra 1,6 en radio y 0,09 en diario. Esto coincide con la correlación, la TV tiene la más alta con las ventas (0,90).

¿Las features extraídas del dataset fueron buenas predictoras? ¿Sugieren otras?

La TV fue una predictora muy buena (correlación de 0,90 con las ventas). 
La radio aportó menos (0,35) y el diario casi nada (0,16). 
Las tres variables tienen poca relación entre sí (la mayor es radio-diario, 0,35), por eso los coeficientes son confiables. 
Otras variables que podrían mejorar el modelo son precio del producto, época del año, publicidad en redes sociales, tamaño del mercado y publicidad de la competencia.

Comparativa de resultados con datos de Entrenamiento y de Test

| Métrica | Entrenamiento | Test |
|---|---|---|
| R2 | 0,900 | 0,906 |
| MAE | 1,234 | 1,275 |
| RMSE | 1,636 | 1,705 |

Los resultados son muy parecidos en los dos conjuntos: 
el R2 es apenas mayor en Test y los errores apenas mayores, diferencias mínimas. 

No hay sobreajuste: el modelo funciona igual de bien con datos que no vio.
