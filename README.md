# SOC_estimation
Herramienta para analizar los datos de descarga de una batería obtenidos con una Carga Electrónica Rigol

## Formas de llamar al Script

    $ python3 estimate_SOC.py csv_name degree_regression internal_resistor

En caso de no indicarse parámetros, se toma por defecto una aproximación de grado
4 y apertura del fichero DL_RecordData0.

## Funciones disponibles

- `calc_Voc(internal_R, voltage, current)`: Calcula el Voltaje de circuito abierto
de la celda.

- `calc_SOC(internal_R, capacity, voltage, current)`: Calcula el estado de carga en función de la Tensión en circuito abierto.

- `plot_SOC_data(Voc, SOC, PLOT_NAME, FILE_PATH)`: Grafica la curva SOC-V open Circuit.

- `plot_polinomical_reg (Voc, SOC, degree_inf, degree_sup, PLOT_NAME, FILE_PATH)`:
Realiza un cálculo de las funciones polinómica desde el grado inferir indicado hasta el superior y representa dichas curvas.

- `calc_polinomical_reg (Voc, SOC, degree, PLOT_NAME, FILE_PATH)`: Representa la curva de regresión del grado indicado frente a la curva real de SOC.

- `plot_my_curve(Voc, SOC, degree, coefs, PLOT_NAME, FILE_PATH)`: Representa una curva arbitraria dada por sus coeficientes, frente a la curva SOC empírica proporcionada.
