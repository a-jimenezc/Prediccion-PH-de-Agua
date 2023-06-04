## Predicción del PH de Planta de Tratameinto de Agua Potable Achachicala

### Objetivo

El objetivo del presente trabajo es desarrollar un modelo que permita predecir la nivel de PH de la planta de tratamiento de agua Achichicala a partir de los datos tomados diariamente en un lapso de 6 meses.

### Prerequisitos

Las librerias necesarias están listadas en requirements.txt. También se incluye environment.yml para los usuarios de Anaconda.

### Datos

Los datos provienenen de las mediciones del nivel de PH tomados de la planta Achachicala, ubicada en la ciudad de La Paz en Bolivia, y como parte del control normado por Ley. El rango de tiempo es de 6 meses, con una frecuencia de una muestra por día. La muestra se tomó entre el primero de enero y el 30 de junio del 2021.

### Exploración Inicial de Datos

Se grafica la serie de tiempo junto con un gráfico de violín por semana.

<img src="referencias/images/serie.png" alt="Alt text 1" width="500"/> 

<img src="referencias/images/violin.png" alt="Alt text 2" width="500"/>

Visualmente, no hay tendencia ni variaciones estacionarias. 

Tambien, se muestra un gráfico de frecuencias para visualizar la ausencia de tendencia y la distribción normal de los datos respecto al promedio. 

<img src="referencias/images/freq.png" alt="Alt text 1" width="300"/>

Finalmente, se ejecuta un test de Dickey-Fuller y con un *p-value* de 3.908e-12 se descarta la hipóteis *Null* y se acepta que nuestros datos son estacionarios.

### Construcción del modelo
Se probaron tres modelos diferentes. El primero fue un modelo ARMA, el segundo un modelo RNN (*Recurrent Neural Network*) y el tercero fue un LSTM (*Long-Short Term Memory). los resultados se muestran a continuación.

<img src="referencias/images/arma.png" alt="Alt text 1" width="400"/> 

<img src="referencias/images/rnn.png" alt="Alt text 1" width="300"/>  <img src="referencias/images/lstm.png" alt="Alt text 1" width="300"/> 

### Selección del modelo

A pesar de la complejidad de los algoritmos de Deep Learning utilizados, RNN y LSTM, no se observa una mejora significativa respecto al modelo más simple de ARMA. Por lo tanto, se prefiere tomar este último como el modelo para realizar las predicciones. 


### Conclusiones

El modelo ARMA se desempeña bastante bien y tiene una arquitectura simple. Esto se debe a la naturaleza de los datos. Sin embargo, en caso de tener datos en un rango de tiempo mucho mas amplio, es posible que tendencias y variaciones estacionarias surjan. En este caso, modelos mas complejos puede entregar mejores resultados.

### Contacto

[Linkedin](https://www.linkedin.com/in/antonio-jimnzc/)


