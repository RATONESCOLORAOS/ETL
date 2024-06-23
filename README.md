# Proceso ETL para la obtención de los productos de los supermercados Dia y Mercadona

## Descripción

Este repositorio contiene un proceso ETL (Extracción, Transformación y Carga) diseñado para gestionar y procesar datos provenientes de Dia y Mercadona. El objetivo principal es extraer los datos vía web scraping, transformarlos según los requisitos de la app y cargarlos en un mysql Workbench para su posterior uso en la BBDD.

## Estructura del Proyecto

├── data/ # Carpeta principal de datos

│ ├── data_csv/ # Carpeta para los archivos de datos obtenidos por web scraping

│ └── src/ # Carpeta para los archivos .ipynb con el código necesario para el trabajo

## Extracción

Para la extracción de datos hemos decidido utilizar Python como lenguaje de programación para trabajar con la tecnología Selenium para realizar web scraping.

## Transformación

Para transformar y limpiar los datos hemos utilizado la librería Pandas de Python para crear diferentes dataframes con los productos organizados y posteriormente exportarlos como archivos .csv para almacenar la información.

Posteriormente se han unificado todos los archivos en un gran dataframe llamado 'productos_categoría'.
Contiene las columnas: 'producto', 'marca', 'formato', 'cantidad', 'precio', 'supermercado', 'categoría', 'id_producto'.

Por último se creó manualmente el ultimo dataframe llamado 'fuel' que contiene información sobre los precios de los carburantes en España en las diferentes gasolineras disponibles.
Contiene las columnas: 'carburante', 'repsol', 'cepsa', 'galp', 'shell', 'bp'.

## Carga de datos

Para cargar los datos a mysql Workbench utilizamos la librería de Python sqlalchemy junto con el paquete pymysql.
