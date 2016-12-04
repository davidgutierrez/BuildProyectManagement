# “Problem identification and task identification” 
 
Eduard A. Avendaño Camacho, Cristian D. Gutierrez Gil, Carlos I. Zubieta León 
Universidad de los Andes, Bogotá, Colombia 
{ea.avendano, cd.gutierrez, ci.zubieta}@uniandes.edu.co 
Fecha de presentación: Octubre 4 de 2016 
  
## Business Comprehension:  
 
### About the company
 
AGZ is a multinational what work in the field of the construction and instalation of Industries projets.

### Direct Client
 
Our client is the PMO (Project Management Office). One of its main tasks is to present to the board of directors the progress of each of the projects compared to the baseline. 
 
### Identification of the problem 

In order to guarantee and control each of its projects the **PMO** must generate weekly and monthly reports from different departments to constantly verify the progress of the project and the administration of Money and Activities in each area.

These reports should be unified from different sources and formats of data that each department handles to be presented in a single format that is directed to the management area. Based on these unified final reports, management makes adjustments and restructuring decisions in each project, if necessary. This final format should be clear, understandable and should highlight the characteristics most relevant to the project.

Currently the process of ** verification and unification of the sources is done by hand ** through multiple tables of Excel, on the other hand, part of the information is processed by software called ** Primavera ** by ** Oracle ** that allows the administration and control of multiple projects, for this case, the benefit provided by the tool is not relevant, because the client **does not handle multiple projects at the same time**. Primavera also generates a kind of dashboard that is **very restrictive in terms of displaying the parameters of interest of the client**. 

The client has been working on improving the process of generating the reports of:
- Activity and Performance.
- Costs. 
 
Con este propósito ha venido trabajando con los múltiples departamentos y con la gerencia para determinar los datos relevantes y la presentación de los datos para cada uno de los informes. Gracias a este trabajo se logro un dashboard de actividad y desempeño depurado con solo los parámetros de interés para la empresa. Para este dashbord el cliente necesita mejorar la forma de presentación y navegación, ya que actualmente **debe gastar tiempo en la generación del dashboard cada vez que requiera generar el informe semanal y mensual para cada proyecto**. 
Sobre el dashboard de Costos el cliente se encuentra en el proceso de depuración y coordinación entre los departamentos y la gerencia. **Por el momento cuentan con una base del tablero de costos  que no es definitivo**, por lo cual requieren una propuesta para representar los costos que implica cada proyecto. 
Adicionalmente nos manifestó que con el proceso actual le cuesta mucho esfuerzo y tiempo **detectar desviaciones de tiempo y dinero en la ejecución de cada uno de los proyectos.** 
 
## Characterization of the Data 
### What 
Los datos están en forma de **tabla** (Todas las tablas se encuentran en un libro de Excel que fue obtenido desde el programa “Primavera”).  
En cuanto a los **atributos**, la mayoría son de tipo cuantitativo secuencial.  Pero también existen unos con una semántica especial (Usan una semántica temporal), los cuales se utilizan para identificar una fecha (día, mes y año). 
 
### Why 
 
#### Valor ganado 
- **T1.** *Identificar* cuales son las desviaciones en *Ingeniería, Procura y Construcción* que más influyen en el desempeño. 
- **T2.** *Presentar* la tendencia del *Valor planeado (Pv)*, el ¨*Valor Ganado (EV)* y el *Costo Actual (AC)* en Global. 
- **T3.** *Comparar* la distribución del *PV*, el *EV* y el *AC* para las áreas de Ingeniería, Procura y Construcción. 
- **T4.** *Identificar* en una semana en específica los valores para el *PV*, el *EV* y el *AC*. 
 
#### Histograma 
- **T5.** *Presentar* cuales son los las horas consumidas tanto directa como directamente 
- **T6.** *Comparar* las Horas hombre Programadas con las Reales por cada periodo. 
 
#### Productividad 

- **T7.** *Comparar* la distribución planeada de los parámetros más relevantes en el proyecto (Concreto, Acero, Estructura, Soldadura) vs la distribución real para determinar los cruces de tiempo y los periodos en donde no se cumplieron los valores esperados para cada parámetro.
- **T8.** *Navegar* sobre los parámetros de productividad para seleccionar y *presentar* los parámetros más relevantes para cada proyecto.
- **T9** *Presentar* el acumulado de cada corte en el periodo de fecha seleccionado, e *identificar* los rangos de producción en donde los parámetros observados se encuentran dentro del rango normal esperado.
- **T10.** *Comparar* la relación entre los múltiples parámetros de producción para determinar causa y efectos que explique el comportamiento de la producción esperada vs la real.
 
### How 
  
Dashboard de Desempeño 
 
#### Valor ganado 
 
Las marcas utilizadas son las líneas con posición horizontal y vertical, las cuales poseen el canal del color para identificar el EV, PV y AC. 
 
**T1, T2 y T3**: Para esta tarea se usa un multiChar Line en  donde el eje **x** representa las fechas con intervalos de periodos de corte de la empresa (Semanas y Meses), en el eje **y** se representa el costo del Valor Planeado, Valor ganado y Costo Actual, para estas categorias se usa el canal hue para identificarlas entre si.  

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095498/86aa1b54-8a5b-11e6-97cd-985011271fbf.png">  
<br>
Gráfica de Valor Ganado.  En esta se muestran los Linecharts de Ingeniería, Procura y Construcción junto con el linechart Global. 
</p>
El uso de linechar se justifica porque este idioma es muy efectivo para la representación de grandes volúmenes de datos que tienen lugar en un intervalo continuo de tiempo, y esto sucede en este caso, ya que nos interesa ver el comportamiento del PV, EV y AC en periodo de tiempo. 

Una ventaja importante del uso del line chart es que se puede identificar facilmente los minimos y maximo en donde la tendecia de los parametros cambia para  este caso se puede determinar  para cada categoria (PV, EV y AC) los periodos en donde estan por debajo de la estimacion planeada.

Para apoyar la **T3**, se utiliza un Popup que se muestra al darle clic al título del gráfico mostrando el gráfico seleccionado en tamaño más grande, de esta manera se puede realizar la comparación de una manera más clara por cada elemento.  Al mostrarse el popup, se podrá dar clic en un botón que permite visualizar los detalles en una tabla (Embebed) donde se mostrarán los valores para el EV, PV y AC en cada semana, esto apoyaría a la **T4**. 

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095513/9b7ffea4-8a5b-11e6-9e2a-bceedc65db79.png">  
<br>
Gráfico del Popup de cada elemento.</p>
<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095525/af22ae52-8a5b-11e6-94c9-9ad35d03939e.png">  
<br>
Tabla de Detalles de PV, EV, AC en cada semana para el elemento de Construcción.</p>
 
Otra de las interacciones es permitir a los usuarios pasar el mouse sobre cada una de las líneas para que aparezca un *tooltip* que muestre el detalle de cual es el la ubicación en la fecha, la categoría seleccionada (EV, PV o AC) y el valor en moneda que representa.  También tendrá la manipulación que permite dar clic a cada una de las líneas para resaltarla sobre las demás. 
 
Existe un control que permitirá el filtrado de las fechas de los anteriores gráficos (este control también filtrará los gráficos para la sección de Horas hombre y el de Productividad), este control filtrará desde la mínima fecha con incrementos de una semana.

Para navegar en un rango de periodo por cortes de la empresa (Semana, Mes) se utilizara un control que permite seleccionar rangos de tiempo y visualizar el comportamiento de las actividades. Este control se comunica con los demas para recalcular los periodos de tiempo.

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095536/c495a42e-8a5b-11e6-8c5c-d5bc7bf576d5.png">  
<br>
Gráfica del control para el filtrado por fecha.</p>

<p align="center"> 
<img src="https://dennyglee.files.wordpress.com/2014/06/crossfilter_2014q1_full.png">  
<br>
Referencia de Filtro por Fecha.(CrossFilter)</p>
   
#### Histograma de personal Horas hombre 
Las marcas utilizadas son las Barras con posición vertical, las cuales poseen el canal del color para identificar el El programado y el Real.
**T5, T6:**  2 gráficos que usan el idioma de "Bar chart" donde en el eje **x** se ubica las fechas con intervalos sobre los cuales se puede hacer zoom según la necesidad, donde el defecto es semanal y el minimo es el dia a dia, en el eje **y** se ubican los valores de las horas Hombre, usando el canal del color para cada uno de ellos.  

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/1551324/19095319/b0e9cd66-8a5a-11e6-92c8-d566773f7770.png">  
<br>
Gráfica del horas hombre.</p>

Otra de las interacciones es permitir a los usuarios pasar el mouse sobre cada una de las barras para que aparezca un tooltip que muestre el detalle de cual es el la ubicación en la fecha, la clase (indirecta, directa) y el valor en moneda que representa.  También tendrá la manipulación que permite dar clic a cada una de las barras o campos para resaltarla sobre las demás. 
 
 ### Productividad 
 
**T7, T10** Matriz de Line charts que permite comparar cada uno del parámetro de producción e identificar los parámetros que tiene relación entre sí.  Al incluir el tiempo dentro de la matriz se puede establecer los periodos en donde la producción está por debajo de la esperada. Para facilitar esta tare el grafico indicara sobre la línea los periodos de tiempos en donde las variables analizadas afectan la productividad del proyecto.
 
**T8** Un filtro de los parámetros categóricos a seleccionar, permite agregar o quitar parámetro para ver con más detalle la relación entre cada uno de ellos. Este filtro indicara las categorías más interesantes para cada tipo de proyecto (Construcción, Electromecánica, Instalación, Mantenimiento, entre otros)
￼ 
### Bibliografía 
- Munzner, T. (2014). Visualization Analysis and Design. Boca Raton: CRC Press. 
- Oracle. (30 de 09 de 2016). www.oracle.com. Obtenido de http://www.oracle.com/partners/esa/products/applications/primavera/get-started/index.html 
- Enote. (30 de 09 de 2016). www.enotes.com.  Obetenido de http://www.enotes.com/homework-help/what-advantages-using-line-graph-represent-data-514721
- Fuente de ejemplo de visualizaciones.  http://square.github.io/crossfilter/

