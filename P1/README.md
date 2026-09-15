
# Documentación de práctica

<div align="justify">
En esta primera práctica, se ha realizado un total de cuatro tareas, siguiendo enfoques y objetivos distintos, tal y como se muestra a continuación:
<br>
<br>
En la primera tarea, se ha generado un tablero de ajedrez siguiendo un razonamiento natural utilizando un método iterativo para pintar el diseño alternado de cuadrados blancos y negros propios del ajedrez. Además, como segunda tarea se ha solicitado a la inteligencia generativa (gemini pro 3.1) que solucione el mismo problema sin ninguna directriz específica, creando un método declarativo que utiliza la librería de Numpy para pintar de forma alternada los cuadrados blancos y negros. 
<br>
<br>
  
<div align="center">

| Iterativo | Declarativo |
| --- | --- |
| 0.00013 ± 0.00003 s | 0.00467 ± 0.00085 s |

</div>

<br>
Por tanto, para poder realizar una comparativa de la eficiencia al implementar cada una de las versiones se ha calculado el promedio de tiempo de ejecución con su respectiva desviación estándar haciendo uso de la librería time. Esta comparativa nos permite concluir que el método implementado sin IA (iterativo) es significativamente más eficiente al tratar el espacio como bloques rectangulares frente a la solución declarativa, que trata cada pixel como caso individual a estudiar.

<br>
<br>
En cuanto a la tercera tarea, se utilizó la librería OpenCV para generar una imagen artística del estilo Mondrian. Representándose líneas negras que forman con sus intersecciones rectángulos, que se han pintando para lograr una imagen de diseño asimétrico con múltiples colores logrando replicar el carácter artístico de las obras del autor.
</div>
