# Análisis de interpolación espacial para datos de precipitación del Estado de Texas

## Resumen

Este repositorio contiene el código y datos de la presentación sobre el proyecto 3 del curso SP-1649 Tópicos de Estadística Espacial Aplicada: El titulo del repositorio es **Analisis de interpolación espacial para datos de precipitación del Estado de Texas**, desarrollado por Melissa Cordero Díaz y Marco Otoya Chavarría, como parte de la Maestría en Estadística de la Universidad de Costa Rica.


- [Análisis de interpolación espacial para datos de precipitación del estado de Texas](#análisis-de-interpolación-espacial-para-datos-de-precipitación-del-estado-de-Texas)
  - [Resumen](#resumen)
  - [Estructura del repositorio](#estructura-del-repositorio)
  - [Datos](#datos)
    - [Fuentes de información](#fuentes-de-información)
    - [Descripción de los datos](#descripción-de-los-datos)
    - [Detalle de las variables](#detalle-de-las-variables)
  - [Análisis](#análisis)
  - [Gráficos y mapas](#gráficos-y-mapas)
  - [Preguntas](#preguntas)

## Estructura del repositorio

El repositorio está compuesto por un archivos de R, usado para realizar el análisis y tres carpetas que contienen los datos, los gráficos producidos y la presentación y el reporte final:

- Los archivos de R, disponibles en formato `.R`, contine el analisis exploratorio de los datos, la aplicación con el método de la distancia inversa ponderada (IDW), la aplicación con el método de  Kriging y la interpolación realizada (`PROYECTO 3 GEOESPACIAL.R`)

- La carpeta `Datos` contiene los datos usados, la carpeta `Plots` contiene los gráficos y mapas producidos y usados en el artículo, y finalmente la carpeta `Reporte` contiene la presentación y el documento final.


## Datos

### Fuentes de información

Se cuenta con los datos reportados de precipitación de 21 estaciones climáticas para el estado de Texas, utilizados en el analisis de “Introducción a SIG y análisis espacial” de Manuel Gimond, edición de septiembre de 2019. Los datos pueden descargarse directamente a los siguientes links:

Datos de precipitación: http://colby.edu/~mgimond/Spatial/Data/precip.rds

Datos del mapa: http://colby.edu/~mgimond/Spatial/Data/texas.rds

### Descripción de los datos

Los datos cuentan con las respectivas coordenadas espaciales y los promedios anuales de precipitación reportados por cada una de las estaciones climáticas. Los datos se encuentran disponibles en formato de puntos espaciales. 

### Detalle de las variables

1) `precipitacion.csv`:

**coords.x1:** Longitud

**coords.x2:** Latitud

**Precip_in :** Promedio anual de precipitación medida en pulgadas

## Análisis

El análisis de los datos se describe en el archivo `PROYECTO 3 GEOESPACIAL.R` y el artículo vinculado al repositorio.

De forma resumida, los análisis consiste en la aplicación de un métodos de interpolación deterministas (método de la distancia inversa ponderada - IDW) y un método de interpolación estadísticos (Kriging) para datos de precipitación anual reportada por estaciones climáticas ubicadas en el Estado de Texas, con el fin de realizar una interpolación de la precipitación a las áreas en donde no se tiene datos. 

Se inicia con un analisis exploratorio de los datos, para posteriormente aplicar método de la distancia inversa ponderada (IDW) y realizar una interpolación de la superficie con los resultados obtenidos. Posteriormente se palica el métoodo de interpolación estadístico (Kriging) mediante tres pasos: Eliminar la tendencia espacial, definir el modelo del variograma que mejor caracterice la autocorrelación espacial de los datos, onterpolación de la superficie y unir la superficie interpolada Kriging a la superficie interpolada de tendencia (resultado final). Finalmente se comparan los resultados obtenidos y se concluye el analisis con la construcción de una mapa de varianci. 

## Gráficos y mapas

Los gráficos estan contenidos en la carpeta `Plots` son generados mediante los comandos del script `PROYECTO 3 GEOESPACIAL.R`, con base en los datos del archivo de Excel `precipitacion.csv`. Estos gráficos estan incluidos en el documentos final con los mismos nombres seguidamente anotados:

- `Grafico1.pdf`: Precipitación anual medida en pulgadas por estación climática, Texas
- `Grafico2.pdf`: Modelos ajustados a variograma residual
- `Mapa1.pdf`: Precipitación anual promedio (en pulgadas) de acuerdo a la estaciones, Texas
- `Mapa2.pdf`: Predicción de la precipitación con el método de distancia inversa ponderada (IDW)
- `Mapa3.pdf`: Superficie kriged final obtenida con los diferentes modelos ajustados
- `Mapa4.pdf`: Variancia obtenida del análisis de Kriging para la precipitación anual promedio, Texas 

## Preguntas

Cualquier pregunta o puede escribirle a los autores y dueños de este repositorio a las siguientes direcciones de correo electrónico:

- Melissa Cordero Díaz: cmeli-2@hotmail.com
- Marco Otoya Chavarría: marco.otoya.chavarria@una.ac.cr
