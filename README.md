# L03-Población mundial

AUTORA: Toñi Reina

REVISORES: José Antonio Troyano, Daniel Mateos, Mariano González

ÚLTIMA MODIFICACIÓN: 07/10/2019


En este proyecto trabajaremos con datos de población mundial, representados mediante listas. Implementaremos una serie de funciones que nos permitirán mostrar gráficas de evolución de la población, así como comparar la población en distintos países.

## Estructura de las carpetas del proyecto

* **/src**: Contiene los diferentes módulos de Python que conforman el proyecto.
    * **poblacion.py**: Contiene funciones para explotar los datos sobre la población mundial.
    * **poblacion_test.py**: Contiene funciones de test para probar las funciones del módulo `poblacion.py`. En este módulo está el main
* **/data**: Contiene el dataset o datasets del proyecto
    * **population.csv**: Archivo con los datos de población de diversos paises o agrupaciones de paises en distintos años.
* **/doc**: Contiene archivos con documentación acerca del proyecto.
    * **Enunciado.pdf**: Archivo con el enunciado del laboratorio.
 
## Funciones a implementar:

* **lee_poblaciones(fichero)** : lee el fichero de entrada y devuelve una lista de tuplas 
    (nombre_pais, cod_pais, anyo, num_habitantes)
* **calcula_paises(poblaciones)**: toma una lista de tuplas (nombre_pais, cod_pais, anyo, num_habitantes) y devuelve una lista ordenada con los nombres de los paises o conjuntos de paises para los que hay datos.
* **filtra_por_pais(poblaciones, pais)**: toma una lista de tuplas (nombre_pais, cod_pais, anyo, num_habitantes) y devuelve una lista de tuplas (anyo, num_habitantes) con los datos del pais que se pasa como parámetro. El pais se puede dar con su nombre completo o con su código.
* **filtra_por_paises_y_anyo(poblaciones, anyo, paises)**: toma una lista de tuplas (nombre_pais, cod_pais, anyo, num_habitantes) y devuelve una lista de tuplas (nombre_pais, num_habitantes) con los datos del año pasado como parámetro para los paises incluidos en el parámetro paises. 
* **muestra_evolucion_poblacion(poblaciones, pais)**: toma una lista de tuplas (nombre_pais, cod_pais, anyo, num_habitantes) y genera un gráfico con la evolución de la población del pais dado como parámetro. El pais se puede dar con su nombre completo o con su código.
* **muestra_comparativa_paises_anyo(poblaciones, anyo, paises)**: toma una lista de tuplas (nombre_pais, cod_pais, anyo, num_habitantes), un año y un grupo de paises y genera un gráfico de barras con la población de esos países en el año dado como parámetro.

## Ayuda para el uso de matplotlib

Para digujar un diagrama de barras usando la librería `matplotlib` puedes usar un trozo de código similar al siguiente, teniendo en cuenta que `titulo` debe ser una variable que contenga el título que se le va a dar al gráfico, `l_habitantes` una lista con números que representan la altura que deben tener las distintas barras del gráfico  y `l_paises` una lista con las etiquetas que para cada barra aparececerán en el eje X, que en el contexto de este proyecto serán nombres de paises.s
     
 ```python     plt.title(titulo))    indice = range(len(l_paises)))    plt.bar(indice, l_habitantes))    plt.xticks(indice, l_paises, fontsize=8))    plt.show()
````