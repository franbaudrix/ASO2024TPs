```console
1) 
   a) EL tiempo de ejecucion es relativamente predecible. SI tenemos en cuenta solamente los segundos, estos siempre son iguales en ambos codigos. Sin embargo, si tenemos en cuenta los decimales, ya no es tan predecible, ya que varia bastante respecto de cada ejecucion.
   
   b)
	Tiempos de companiero          Mis tiempos de ejecucion

			    ---sinhilos.py---
	1- 5.28343                              1- 5.44858
	2- 5.31339                              2- 5.44056
	3- 5.27064                              3- 5.46197
	4- 5.35220                              4- 5.43627
	5- 5.25448                              5- 5.44372
	promedio: 5.29483                       promedio: 5.44622

	Tiempos de companiero           Mis tiempos de ejecucion

	                    ---conhilos.py---
	1- 4.05864                              1-4.03202
	2- 4.03445                              2-4.04277
	3- 4.06325                              3-4.06753
	4- 4.11431                              4-4.03352
	5- 4.08229                              5-4.03515
	promedio: 4.07059                       promedio: 4.04220

	RTA: Los tiempos de ejecucion no son iguales, en el archivo sinhilos.py su promedio es mas bajo, mientras que en el archivo conhilos.py el mio es mas bajo.
   

     c) El tiempo de ejecucion con las lineas comentadas es, en promedio, 0.045 segundos. Por otro aldo, sin esas lineas comentadas este  aumenta significativamente, alcanzando un promedio de 11.23 segundos aproximadamente.
Esto es producido porque al quitar los comentarios, los for loops relantizan la ejecucion de los threads, por lo que se sobrecarga el procesador ya que se suman iteraciones que colisionan con ellos, generando en cierto punto una race condition. La dificultad en el planificador de tareas para dividir la suma y la resta surge cuando los threads utilizan una misma variable global (acumulador), convirtiéndola en una zona crítica entre ambos. Como resultado, el acumulador, que generalmente sería 0, puede terminar siendo cualquier otro número mucho mayor, generando asi una race condition. Este fenomeno ocurre con el codigo comentado o no, pero comentado es menos ocurrente.
  
2) 
     a) https://github.com/franbaudrix/ASO2024TPs/blob/master/TP3/filesTP3/con_race_condition.c

     b) https://github.com/franbaudrix/ASO2024TPs/blob/master/TP3/filesTP3/flujo.png
