# “Planteamiento del problema e identificación de las tareas de análisis” 
 
Eduard A. Avendaño Camacho, Cristian D. Gutierrez Gil, Carlos I. Zubieta León 
Universidad de los Andes, Bogotá, Colombia 
{ea.avendano, cd.gutierrez, ci.zubieta}@uniandes.edu.co 
Fecha de presentación: Octubre 4 de 2016 
  
## Comprensión del Negocio:  
 
### Acerca de la compañia
 
Una multinacional que se encarga de la construcción e instalación de proyectos. 

### Cliente Directo 
 
El cliente directo es el Director de PMO (Project Management Office).  Una de sus principales labores es presentar a la junta directiva los avances de cada uno de los proyectos comparándolos con la línea base. 
 
### Identificación del Problema 
 
Con el fin de garantizar y controlar cada uno de sus proyectos **la oficina de administración de proyectos** debe generar reportes semanales y mensuales de diferentes departamentos para verificar constantemente el avance del proyecto y la administración de dinero en cada área.  
Estos reportes deben ser unificados de diferentes fuentes y formatos de datos que maneja cada departamento para ser presentado en un único formato que va dirigido al área gerencial. Basado en estos reportes finales unificados la gerencia toma decisiones de ajustes y restructuración en cada proyecto de ser necesario. Este formato final debe ser claro, entendible y debe resaltar las características más relevantes para el proyecto.  
Actualmente el proceso de **verificación y unificación de las fuentes se hace a mano** a través de múltiples tablas de Excel, por otro lado, parte de la información es procesada por un software llamado **primavera** propietaria de **Oracle** que permite la administración y control de múltiples proyectos, para el caso del cliente lo que le aporta esta herramienta no es muy relevante ya que ellos **no manejan múltiples proyectos a la vez**. Primavera también genera una especie de dashboard que es **muy restrictivo en cuanto a la visualización de los parámetros de interés del cliente**. 
El cliente ha venido trabajando en el mejoramiento del proceso de generación de los informe de : 
- Actividad y Desempeño. 
- Costos. 
 
Con este propósito ha venido trabajando con los múltiples departamentos y con la gerencia para determinar los datos relevantes y la presentación de los datos para cada uno de los informes. Gracias a este trabajo se logro un dashboard de actividad y desempeño depurado con solo los parámetros de interés para la empresa. Para este dashbord el cliente necesita mejorar la forma de presentación y navegación, ya que actualmente **debe gastar tiempo en la generación del dashboard cada vez que requiera generar el informe semanal y mensual para cada proyecto**. 
Sobre el dashboard de Costos el cliente se encuentra en el proceso de depuración y coordinación entre los departamentos y la gerencia. **Por el momento cuentan con una base del tablero de costos  que no es definitivo**, por lo cual requieren una propuesta para representar los costos que implica cada proyecto. 
Adicionalmente nos manifestó que con el proceso actual le cuesta mucho esfuerzo y tiempo **detectar desviaciones de tiempo y dinero en la ejecución de cada uno de los proyectos.** 
 
## Caracterización de los Datos 
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
 
### How 
  
Dashboard de Desempeño 
 
#### Valor ganado 
 
Las marcas utilizadas son las líneas con posición horizontal y vertical, las cuales poseen el canal del color para identificar el EV, PV y AC. 
 
**T1, T2 y T3**:  4 gráficos que usan el idioma de "Line chart" donde en el eje **x** se ubica las fechas con intervalos de semana a semana, en el eje **y** se ubican los valores en moneda de Valor Planeado, Valor ganado y Costo Actual, usando el canal del color para cada uno de ellos.  

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095498/86aa1b54-8a5b-11e6-97cd-985011271fbf.png">  
<br>
Gráfica de Valor Ganado.  En esta se muestran los Linecharts de Ingeniería, Procura y Construcción junto con el linechart Global. 
</p>
El uso de linechar se justifica porque este idioma es muy efectivo para la representación de grandes volúmenes de datos que tienen lugar en un intervalo continuo de tiempo, y esto sucede en este caso, ya que nos interesa ver el comportamiento del PV, EV y AC en periodo de tiempo. 

Una ventaja importante del uso del line chart es que se puede observar fácilmente la subida o caída de los puntos de los datos además permite la comparación de los items gráficados, en este caso se poseen 3 items (PV, EV y AC) que se comparan en un mismo periodo.
 
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

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/13947710/19095536/c495a42e-8a5b-11e6-8c5c-d5bc7bf576d5.png">  
<br>
Gráfica del control para el filtrado por fecha.</p>
 
- Zoom pop up 
- Tool tip que muestre la fecha y el valor en ese punto para cada gráfico 
- Que al dar clic en cada una de las líneas se resalta en cada uno de los gráficos 
- Drill down para cada gráfico 
  
#### Histograma de personal Horas hombre 
Las marcas utilizadas son las Barras con posición vertical, las cuales poseen el canal del color para identificar el El programado y el Real.
**T5, T6:**  2 gráficos que usan el idioma de "Bar chart" donde en el eje **x** se ubica las fechas con intervalos sobre los cuales se puede hacer zoom según la necesidad, donde el defecto es semanal y el minimo es el dia a dia, en el eje **y** se ubican los valores de las horas Hombre, usando el canal del color para cada uno de ellos.  

<p align="center"> 
<img src="https://cloud.githubusercontent.com/assets/1551324/19095319/b0e9cd66-8a5a-11e6-92c8-d566773f7770.png">  
<br>
Gráfica del horas hombre.</p>

Otra de las interacciones es permitir a los usuarios pasar el mouse sobre cada una de las barras para que aparezca un tooltip que muestre el detalle de cual es el la ubicación en la fecha, la clase (indirecta, directa) y el valor en moneda que representa.  También tendrá la manipulación que permite dar clic a cada una de las barras o campos para resaltarla sobre las demás. 
 
 
 
￼ 
### Bibliografía 
- Munzner, T. (2014). Visualization Analysis and Design. Boca Raton: CRC Press. 
- Oracle. (30 de 09 de 2016). www.oracle.com. Obtenido de http://www.oracle.com/partners/esa/products/applications/primavera/get-started/index.html 
- Enote. (30 de 09 de 2016). www.enotes.com.  Obetenido de http://www.enotes.com/homework-help/what-advantages-using-line-graph-represent-data-514721
- Fuente de ejemplo de visualizaciones.  http://square.github.io/crossfilter/

