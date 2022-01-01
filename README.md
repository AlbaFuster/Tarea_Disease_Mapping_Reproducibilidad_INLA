# Tarea_Disease_mapping_INLA_Reproducibilidad

## Introducción 
<p align="justify">
En este repositorio se introduce un ejemplo al análisis de datos espaciales en redes de localizaciones fijas enfocado a mapeo de enfermedades. El banco de datos se corresponde con la mortalidad en hombres por enfermedad isquémica en la provincia de Aragón. Se utilizarán modelos jerárquicos bayesianos con métodos de MCMC e INLA para ajustar un modelo de Besag. Así mismo, se han empleado recursos que permiten la reproducibilidad de la práctica.
</p>

## Requisitos 

<p align="justify">
Para el correcto funcionamiento del repositorio es necesario tener instalado R-INLA y los siguientes paquetes.

1. Instalar R-INLA (en caso de problemas con la instalación acceder a [r-inla.org](https://www.r-inla.org/)):

install.packages("INLA",repos=c(getOption("repos"),INLA="https://inla.r-inla-download.org/R/stable"), dep=TRUE)

install.packages("INLA",repos=c(getOption("repos"),INLA="https://inla.r-inla-download.org/R/testing"), dep=TRUE)


2. Instalar paquetes:

install. packages(c("sp", "Matrix", "spdep","maptools", "lattice", "coda", "boot", "R2WinBUGS", "denstrip", "rgdal", "dplyr", "viridis", "denstrip",
"rgdal","gridExtra", "RColorBrewer")) 

  
3. Cambiar directorio WinBUGS: al descargar las carpetas del repositorio es necesario cambiar el directorio de WinBUGS (bugs.directory), cambia la ruta donde hayas descargado todo el respositorio.

set.seed(12345)
result2 <-
  bugs(
    model = model,
    data = data,
    inits = inits,
    parameters = param,
    bugs.directory = "C:/Users/albaf/OneDrive/Escritorio/tarea_mapas_Alba/WinBUGS14",
    n.iter = 10000,
    n.burnin = 1000,
    #debug = TRUE
  )

</p>
