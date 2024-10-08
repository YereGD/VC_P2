# VC_P2


En esta practica se han realizado 4 tareas propuestas:


## 1º Tarea

En esta tarea se ha realizado el conteo pixeles blancos en las filas de la imagen de Canny, para ello se ha empleado la funcion de cv2 "reduce" modificando el segundo parametro de un 0 a un 1, así conseguimos obtener un matriz de matrices que tiene en cada fila una matriz con la suma de los pixeles blancos. Con esta información obtenemos la fila con mayor número de pixeles en blanco y realizando comparaciones vemos cuantas superan el 95% de este maximo. Así mismo, se muestra en una grafica en el eje X el numero de fila y en el eje Y el porcentaje de pixeles en blanco de la fila, el eje X va de 0 a 512 y el Y de 0 a 1.

![image](https://github.com/user-attachments/assets/4014d60c-2323-4b49-bd4f-dc200185803a)



## 2º Tarea

Esta tarea es muy similar a la anterior, en este caso se realiza el mismo procedimiento que la anterior tarea, en este caso se aplica un umbralizado a una imagen de Sobel y a esta imagen es a la que se le realiza conteo de píxels blancos de filas y columnas y se calcula el máximo en fila y columna y cuales son las filas y columnas que superan el 95% de este máximo. En esta tarea se comparan los resultados y en la imagen Sobel se remarca con primitivas las filas y columnas.

![image](https://github.com/user-attachments/assets/db017e93-0d3e-4857-9f6b-6edfb4c90724)
![image](https://github.com/user-attachments/assets/7555d63b-486b-49c3-8bb0-66c3e7aecddd)


## 3º Tarea

En esta tarea para demostrar a las personas que no cursan la asignatura algunas funciones de open-cv, hemos decidido usar el umbral y la diferencia. En el caso del umbral, pasamos la imagen a escala de grises y aplicamos un umbral con la función "cv2.threshold", le pasamos el valor del umbral dinámicamente mediante el scroll del ratón. Para la diferencia, usamos la función "cv2.absdiff" y en nuestro caso, hacemos la diferencia de los 10 últimos frames y la mostramos, provocando un efecto de estela en el movimiento.

![2024-10-03 18-44-31](https://github.com/user-attachments/assets/75dcfaeb-30e8-428c-b87a-ac4876bbb5a7)


## 4º Tarea

En la cuarta tarea, lo que hemos intentado hacer es detectar los límites de un objeto en movimiento, en nuestro caso, una persona.

Para ello hemos usado principalmente la función de open-cv “absdiff”, esto es posible porque medimos los cambios entre 2 frames y detectamos por filas y columnas donde empieza y dónde acaba dicho cambio. 

Antes pasamos la imagen capturada a escala de grises, calculamos la diferencia y a la diferencia le aplicamos un threshold que tenemos que calibrar dependiendo del entorno. 

Después hay un bucle que recorre empezando por los dos extremos y hasta que se encuentran los índices para encontrar el primer cambio notable, esto se aplica tanto por filas como por columnas. 

Una vez tenemos la posición de los píxeles donde empieza y acaba el movimiento, le pintamos un rectángulo rojo que rodea el objeto en cuestión.


![2024-10-03 18-45-22](https://github.com/user-attachments/assets/92609b86-523f-4b73-8f0b-5e76d869d6fb)


Autores:

Yeremay García Déniz

Adonai Hernandez Bolaños
