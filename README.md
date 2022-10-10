Modelos de aprendizaje aplicado a estudio de Cáncer de mama 

                                                                          Nombre: Karina Esther Ramírez Rivera
                                                                          Fecha: 09/10/2022

1	Resumen

En este documento se revisan varios modelos de aprendizaje automático aplicados a un estudio de diagnóstico de cáncer de mama desarrollado por la Universidad de Wisconsin en el año 1991. 


Palabras clave: modelos aprendizaje, machine learning, Python, pandas, numpy



2	Acerca del estudio 

Este trabajo surgió con el objetivo de diagnosticar con precisión el cáncer de mama utilizando muestras de masas mamarias extraídas a través de una punción por aspiración con aguja fina (FNA, por sus siglas en inglés). Posteriormente, la muestra se coloca en un portaobjetos de microscopio y se tiñe para resaltar los núcleos celulares. A continuación, se digitaliza la imagen del portaobjeto y se aísla el núcleo individual usando el software Xcyt.

Una vez que los núcleos han sido aislados, el programa calcula valores para cada una de las diez características de cada núcleo, midiendo el tamaño, la forma y la textura. Estas diez características relevantes para el estudio son:

a)	Radio (media de las distancias del centro a los puntos del perímetro)

b)	Textura (desviación estándar de los valores de la escala de grises)

c)	Perímetro

d)	Área

e)	Suavidad (variación local en longitudes de radio)

f)	Compacidad (perímetro2 / área)

g)	Concavidad (severidad de las porciones cóncavas del contorno)

h)	Puntos cóncavos (número de porciones cóncavas del contorno)

i)	Simetría

j)	Dimensión fractal (regularidad de los bordes)

Adicionalmente, se calcula la media, el error estándar y los valores extremos de estas características, lo que da como resultado un total de 30 características nucleares para cada muestra.




3	Acerca de los datos

Para el ejercicio de prueba se ha tomado un conjunto de datos conocido como Datos de cáncer de mama de Wisconsin. 

3.1	Link de descarga

https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29

3.2	Estructura

•	569 filas/muestras

•	32 columnas/variables


4	Objetivo del trabajo 

Evaluar varios modelos de aprendizaje automático aplicados a un estudio de diagnóstico de cáncer de mama utilizando Python y varias de sus librerías.


5	Preparación de los datos

Fase inicial 

-	Instalar las librerías necesarias
-	Importar archivo de datos 
-	Conocer la información de las variables: se identifica una variable de tipo entero (“ID”), 30 variables tipo float y una variable de tipo object (“Diagnostico”).
-	En la variable de interés (“Diagnostico”) reemplazar ‘M’ por 1 y ‘B’ por 0.
-	No se identifica valores duplicados.
-	No se identifica missing values en minugna variable.
-	Retirar variable “ID” para iniciar el análisis

Análisis exploratorio de datos 

-	Descripción estadística de los datos: aquí podemos revisar los estadísticos básicos de cada una de las variables: frecuencia, la media, desviación estándar, mínimo, máximo y rangos intercuartiles). 
-	Visión gráfica de la variable de interés (“Diagnostico”): Se identifican 357 muestras “Benignas” y 211 “Malignas”.
-	Histograma de las variables: Se observa variables que tienen una distribución sesgada hacia la izquierda (por ejemplo: Radio_m, Compacidad_m, Concavidad_m) y otras siguen una distribución más centradas (Suavidad_m y Simetria_m).
-	Distribuciones bivariadas
Nos ayudan a visualizar la relación entre un par de variables. Al observar las gráficas podemos notar relaciones lineales entre las variables: 
o	Perimetro_m y Radio_m
o	Area_m y Radio_m
o	Compacidad_m y Concavidad_m
o	Concavidad_m y PuntosConcavidad_m

Entre las otras variables no se puede identificar un patrón claro- 
-	Matriz de correlación: Se puede observar que la variable “Diagnostico” tiene mayor relación con las variables Puntosconcavos_m, Radio_m, Perimetro_m, Area_m y Concavidad_m.
6	Modelos de Aprendizaje Automático
El primer paso para trabajar con modelos de aprendizaje automático es separar los datos de entrenamiento y de test. Para el ejercicio se ha separado el 67% de datos para entrenamiento (x_train tiene 380 registros) y el 33% para test (x_test tiene 188 registros).

6.1	Modelo 1: PCA
asdfasd
6.2	Modelo 1: PCA
asdfasd
6.3	Modelo 1: PCA
asdfasd

6.4	Modelo 1: PCA
asdfasd

6.5	Modelo 1: PCA
asdfasd



7	Comparación de modelos


