# Análisis estadístico y modelado de la rotación de empleados con R

## Descripción

Proyecto de análisis de datos de recursos humanos orientado a explorar la relación entre las características de los empleados y la rotación laboral (*employee attrition*). El análisis utiliza una base de datos con **1.470 observaciones y 31 variables iniciales** y se desarrolla en R.

El trabajo integra preparación de datos, análisis exploratorio, detección de posibles valores atípicos y modelado mediante regresión logística binomial.

## Objetivos

- Preparar y depurar los datos para el análisis estadístico.
- Identificar variables constantes o irrelevantes para el modelado.
- Transformar variables nominales y ordinales según su naturaleza.
- Examinar datos faltantes y posibles observaciones atípicas.
- Explorar la asociación entre variables laborales y la rotación de empleados.
- Interpretar los resultados y reconocer las limitaciones de los modelos estimados.

## Datos

El análisis utiliza el archivo `IBM-HR-Employee-Attrition-ES.csv`.

La base incluye variables demográficas, condiciones laborales, remuneración, trayectoria profesional, satisfacción laboral, relaciones interpersonales y balance entre la vida personal y el trabajo.

**Nota:** verificá las condiciones de uso y redistribución de la base antes de incluir el archivo de datos en el repositorio.

## Metodología

1. **Preparación de datos:** eliminación de variables constantes y de un identificador arbitrario; transformación de variables nominales y ordinales; recodificación de la variable de rotación como binaria.
2. **Control de calidad:** revisión de datos faltantes y exploración de posibles valores atípicos.
3. **Detección de atípicos:** aplicación de la distancia de Mahalanobis para identificar observaciones potencialmente atípicas en términos multivariados y del rango intercuartílico (IQR) para explorar variables numéricas.
4. **Modelado estadístico:** estimación de modelos de regresión logística binomial con distintas especificaciones.
5. **Interpretación:** examen de coeficientes, errores estándar, razones de momios (*odds ratios*) y medidas de ajuste.

## Herramientas y técnicas

- **Lenguaje:** R
- Preparación y transformación de datos
- Análisis exploratorio de datos
- Tratamiento de variables nominales y ordinales
- Distancia de Mahalanobis
- Rango intercuartílico (IQR)
- Regresión logística binomial
- Interpretación de *odds ratios*

## Limitaciones y próximos pasos

Durante el análisis, algunas especificaciones de la regresión logística generan advertencias de falta de convergencia (`glm.fit: algorithm did not converge`). Por este motivo, los resultados deben interpretarse con cautela y el modelo no debe considerarse todavía un modelo predictivo validado.

Como próximos pasos, se propone revisar la especificación del modelo, investigar posibles problemas de separación o estimación y evaluar el desempeño con datos de prueba o validación cruzada antes de formular conclusiones predictivas.

## Reproducibilidad

El análisis fue desarrollado en R. Para reproducirlo, se requiere tener R instalado y disponer del archivo de datos en la ruta utilizada por el código. Es necesario revisar las rutas de entrada y salida antes de ejecutar el análisis.

## Estado actual del proyecto
Se realizó el análisis exploratorio de una base de 1.470 empleados, en la que aproximadamente el 16,1 % presenta rotación. Se revisaron los tipos de variables, se identificaron variables constantes y se detectaron observaciones potencialmente atípicas. Se ajustó un primer modelo de regresión logística binomial, pero presentó problemas de convergencia, por lo que todavía no es posible establecer conclusiones confiables sobre los factores asociados con la rotación. El próximo paso consiste en profundizar el análisis descriptivo, revisar posibles problemas en la estimación y evaluar modelos alternativos.

## Autor

**Carlos Astorga**

Proyecto de aplicación de métodos estadísticos a datos de recursos humanos.

