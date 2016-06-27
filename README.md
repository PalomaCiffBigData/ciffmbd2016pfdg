# ciffmbd2016pfdg
### Proyecto 3 CIFF-Finanzas (AF#5)

### Instalacion

pip install ciffmbd2016pfdg

### Autoprediccion

Conjunto de librerias para la depuracion de datos y calculo de predicciones

### Uso

Es necesario dos Dataframes, uno con resultados y el que haya que estimar.
Se comenzará utilizando la funcion limpiaDataFrame(df)
- Establecemos el rango de datos correctos en Q1 - 1.5*RIC y Q3 + 1.5*RIC.
- Rellenamos los espacios en blanco y no NAN con el dato menor del rango.
- Los datos fuera de rango los cambiamos con los limites del rango. Los que queden por debajo, con el minimo y los que quedan por encima con el maximo.

A continuacion utilizamos la funcion RatioSeleccion(df, df_target, dfo) que devuelve un array y dos dataFrame, internamente se ejecutan las funciones:
- crearRatios(df): genera los ratios de suma, resta, multiplicacion, division, cuadrado y relativo de todas las variables.
- seleccionPCA(df, dfo, estimador): nos devuelve dos dataFrame
- seleccionRFR(df,df_target,dfo,estimador): devuelve un array

Terminamos con la funcion algStepwise(df, dfo, df_target, dfo_target) nos devuelve un array. Indica el orden de importancia de las variables.
