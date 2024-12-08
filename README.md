# MDD-Proyecto-Parte-2
Primera parte del proyecto de curso

## Tecnologías

* R versión 4.3.2
* RStudio versión 2024.09.0
* Google Colab

## Librerías

* arules
* dplyr
* tidyverse
* tensorflow

## Pasos para ejecución en R

1. Clonar respositorio
2. Descargar zip de datos ubicado aquí -> [Datos](https://drive.google.com/file/d/1vmzETxuv_Hg7rVRYzRe0O37MxJ4iFJvU/view?usp=drive_link).
3. Descomprimir el zip de datos y mover los archivos de datos a la misma carpeta de Proyecto-Parte-1.Rmd
4. Ejecutar código

## Pasos para ejecución en Google colab

1. Cargue los archivos generados después de ejecutra las instrucciones R (Se ubicaran en la misma del proyecto)
2. Ejecutar notebook

## Instrucciones nuevas

Se utilizaron algunas instrucciones adicionales a las vistas en clase que facilitaron la manipulación de la información de los datos. Se muestran a continuación

* Lectura de archivos xlsx: read_xlsx
``` r
PI2017 <- readxl::read_xlsx("PI2017.xlsx");
```
* Renombrar columnas de dataframes: rname
``` r
PI2023_COL_RENAME = PI2023 %>% 
  rename(c(EJERCICIO = ejercicio, ENTIDAD = codigoEntidad, DEPTO = codigoDepto, CLASE = codigoClase, SECCION = codigoSeccion,
           GRUPO = codigoGrupo, COD_ECONOMICO = codNivelEconomicoOperativo, RECURSO = codigoRecurso, ASIGNADO = asignado, VIGENTE = vigente,
           DEVENGADO = devengado
           ))
```

* Combinar dataframes: rbind
``` r
df_ingresos <- rbind(PI2023_READY, PI2022_READY, PI2021_READY, PI2020_READY, PI2019_READY, PI2018_READY, PI2017_READY, PI2016_READY);
df_ingresos
```

*Agregar columna: add_column
``` r
PE2016_NEWCOLUM = PE2016 %>%
  add_column(EJERCICIO = 2016);
```
