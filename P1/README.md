
# Documentación de práctica

<div align="justify">
En esta primera práctica, se ha realizado un total de cuatro tareas, siguiendo enfoques y objetivos distintos, tal y como se muestra a continuación:
<br>
<br>
En la primera tarea, se ha generado un tablero de ajedrez siguiendo un razonamiento natural utilizando un método iterativo para pintar el diseño alternado de cuadrados blancos y negros propios del ajedrez. Además, como segunda tarea se ha solicitado a la inteligencia generativa (gemini pro 3.1) que solucione el mismo problema sin ninguna directriz específica, creando un método declarativo que utiliza la librería de Numpy para pintar de forma alternada los cuadrados blancos y negros. 
<br>

<br>
Por tanto, para poder realizar una comparativa de la eficiencia al implementar cada una de las versiones se ha calculado el promedio de tiempo de ejecución con su respectiva desviación estándar haciendo uso de la librería time. Esta comparativa nos permite concluir que el método implementado sin IA (iterativo) es significativamente más eficiente al tratar el espacio como bloques rectangulares frente a la solución declarativa, que trata cada pixel como caso individual a estudiar.

<br>
<br>

<div align="center">

| Iterativo | Declarativo |
| --- | --- |
| 0.00013 ± 0.00003 s | 0.00467 ± 0.00085 s |

</div>
<br>
En cuanto a la tercera tarea, se utilizó la librería OpenCV para generar una imagen artística del estilo Mondrian. Representándose líneas negras que forman con sus intersecciones rectángulos, que se han pintando para lograr una imagen de diseño asimétrico con múltiples colores logrando replicar el carácter artístico de las obras del autor.
<br>
<br>
La cuarta tarea consiste en detectar y señalar con un círculo el píxel más claro y el más oscuro de cada fotograma capturado por la cámara. Para ello se convierte previamente cada fotograma a escala de grises, de modo que la comparación se realice sobre un único valor de intensidad por píxel en lugar de sobre los tres canales de color. Se han implementado dos versiones con el fin de comparar su comportamiento en tiempo real.
<br>
<br>
La primera versión, desarrollada sin inteligencia generativa, recorre el fotograma píxel a píxel mediante dos bucles anidados, actualizando el mínimo y el máximo junto con sus coordenadas. El resultado no es fluido, sino que avanza a saltos con un retardo claramente perceptible: para una resolución de 640×480 se evalúan más de 300.000 píxeles por fotograma dentro del intérprete de Python, lo que impide alcanzar una tasa de refresco aceptable.
<br>
<br>
Para acelerarlo se ha solicitado a la inteligencia generativa una alternativa optimizada, que sustituye por completo el doble bucle por la función <code>cv2.minMaxLoc()</code> de OpenCV. Esta función devuelve en una única llamada los valores mínimo y máximo junto con sus posiciones, delegando el recorrido a código nativo compilado y vectorizado. Con este cambio la visualización pasa a ser fluida, confirmando que el cuello de botella no era la operación en sí, sino el recorrido explícito del array desde Python.
<br>
<br>
Finalmente, la quinta tarea recoge una propuesta propia de pop art elaborada a partir de la señal de vídeo en directo. El fotograma se divide en tres tiras verticales de igual anchura que se recolocan en un orden distinto al original, generando una composición fragmentada y repetida característica del movimiento. Sobre cada tira se aplica además una manipulación diferente de los canales de color: en la primera se permutan los canales, mientras que en las dos restantes se invierte uno de ellos mediante el complemento <code>255 - canal</code>. El resultado son tres variantes cromáticas saturadas y de alto contraste de una misma imagen, en la línea de las serigrafías repetidas de Andy Warhol.

<br>
<br>
**Uso de inteligencia artificial:** en el desarrollo de esta práctica se ha utilizado la inteligencia generativa para realizar las actividades que requerían su uso, así como, para también para consultar que estrategia sigue el código autogenerado y realizar consultas sobre la librería time. Nota: el modelo utilizado es gemini pro 3.1. 
</div>
