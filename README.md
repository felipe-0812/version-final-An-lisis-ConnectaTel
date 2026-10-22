# version-final-An-lisis-ConnectaTel
Objetivo General del proyecto:
En el proyecto de conectaTel, se analizo para entender el comportamiento de los usuarios jovenes, adulto y adulto mayores, por medio de llamadas, cantidad de mensajes y tiempo de llamdas, asi evidenciar como impacta el mercado de las telecomunicaciones en la poblacion de acuerdo a sus necesidades. 

DATASETS:
los dataset utilizados fueron 3, uno contenian los datos de los usuarios, el segundo plans.csv, ccontenia los detalles de los planes basico y premium, y el tercer dataset, me daba informacion mas detallada de las llamdas y mensajes de texto
plans.csv:
users_latam.csv: 
usage.csv

Etapas:
cargar y explorar: vision clara de la estructura y tipos de columnas
identificacion de problemas de calidad: lista priorizada de problemas que pueden sesgar decisiones
limpieza basica: datos consistentes y listos para analisis estadistico.
visiaulizacion y outliers: Medidas clave que muestren el comportamiento tipico y extremo
segmentacion: visualizacion de sesgos, patrones de usuarios o datos atipicos
insight ejecutivo: segmentos accionables que permiten diseñar ofertas y campañas

Recomendacion variedad de mercado incentivar a usuarios jovenes, inclueyndo nuevos planes que sean atractivos para ellos

se incorporaron las siguientes librerias 
pandas as pd
seaborn as sns
matplotlib as plt

se exploraron los archivos con 
.head()
.info()
.shape()
identificacion de problemas con los codigos porcentuar y sumar los datos faltantes 
.isna().sum()
.isna().sum()
se realizo cambios y rellenos en los archivos users y usage 
pd.to_datetime se cambio a fecha UTC=True
.de.year.unique = mostrar unicos años
se realiza limpieza de datos basico, sacando la mediana de edades y reemplazandolo con el error -999
.median()
.where()
se corrigieron sentinels y fechas imposibles con 
.isna()
.astype(int)
.groupby()
agrupacion por comportamiento de uso, renombrando las columnas
con .groupby().count().reset_index()
renombre las columnas con. rename(columns={
reagrupacion y union de tablas con las columnas key user_id
pd.merge
se realizaron histogramas para la visualizacion de distribuciones y outliers
sns.histplot()  plt.show()
se genero bucle para los boxplots guardando las columnas dentro de columnas_numericas
for col in columnas_numericas:
sns.boxplot()
se creo dos columnas nuevas grupo_uso y grupo edad
def llamada(row)
.apply()
'Bajo uso' cuando llamadas < 5 y mensajes < 5
'Uso medio' cuando llamadas < 10 y mensajes < 10
'Alto uso' para el resto de casos
< 30 jovenes
< 60 adultos
> 60 adultos mayores
se crearon dos graficas para las variables categoricas grupo_uso y grupo_edad
sns.countplot()
plt.title()
plt.xlabel()



