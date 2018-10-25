
# U1. Tecnológicamente hablando

Moodle responde al esquema de lo suele denominarse aplicaciones de web dinámica. Por decirlo de algún modo sencillo. cuando vemos una página de Moodle, estamos viendo algo que se ha construido en este instante bajo nuestra petición.

 Para ver cualquier página en la Web, lo que hacemos es poner en el navegador de Internet una dirección URL. Esa dirección es un petición que pone en marcha la búsqueda de, digamos para simplificar, un ordenador que posee un programa servidor de páginas web. Dicho ordenador contiene entre sus documentos uno que corresponde a la página que estamos solicitando (a eso le podríamos llamar página estática) o es capaz de generar una página tras nuestra petición (y a eso le llamamos página dinámica).

### Páginas estáticas

![](https://raw.githubusercontent.com/catedu/curso-moodle/master/img/HTML_logo.png)
|**Fig. 1.2 Logo HTML (obtenida de [Wikimedia](http://commons.wikimedia.org/wiki/File:HTML_logo.png?uselang=es).<br/>Licencia CC0 (Dominio público)**

Las páginas estáticas que vemos en Internet están escritas, fundamentalmente, en un lenguaje de programación llamado HTML. Es un lenguaje en forma de etiquetas. Por ejemplo, cuando una palabra nos aparece en negrita en nuestro navegador es que está situada entre dos etiquetas, una de cierre y otra de apertura con un código, que es interpretado por el navegador, para que la ponga en un tamaño y una trama más gruesa, que es lo que conocemos como negrita. También con etiquetas se genera una tabla, se colocan los términos en listas, se insertan imágenes, se producen hiperenlaces, etc.

HTML no dejaba del todo satisfecho a los programadores y diseñadores que utilizaban este lenguaje para crear sus páginas por diversos motivos; entre ellos, si en cada palabra, frase o párrafo que componen una web se iba marcando qué aspecto debían presentar y, si en algún momento se necesitaba cambiar, por ejemplo, un tipo de fuente o tamaño de letra, era necesario acceder a muchos documentos para hacer este cambio. Para solucionar ese problema y otros relacionados con la estructura de una página web, surgió CSS, una manera de separar, si se desea, en un solo documento todo lo relativo a la presentación estética o apariencia de una web, para que en cada documento sólo haya que decir al navegador: "el aspecto de toda esta sección está en este archivo; léelo y represéntalo en la pantalla". El otro gran problema que se solucionaba utilizando los CSS era el de separar la estructura del contenido, de la presentación del mismo. En el HTML se marcan las partes que hay en el documento que se va a presentar; por ejemplo, se indica dónde va cada parte y cuál es el contenido de la cabecera, del menú lateral, de la parte principal, del pie, etc. o qué contenidos constituyen un epígrafe de primer nivel o de segundo o qué debe ser un párrafo. En el archivo o archivos CSS se dice qué aspecto tendrá la fuente de cada una de esas secciones mencionadas, qué aspecto tendrá la sección, cuánto ocupará y en dónde debe aparecer, y cuál es el aspecto de los epígrafes de cada nivel o de los párrafos, etc. De tal forma que, al alterar este documento, se modifican todos los apartados a los que afecta, de forma instantánea.

En casi todas las páginas actuales, además de HTML y CSS, hay javascript. Es un lenguaje de programación que permite dotar a las páginas de pequeños contenidos dinámicos, que dan una cierta impresión de interactividad, por ejemplo, se puede mostrar la fecha del día, que javascript toma del reloj del sistema del cliente, o nos da un mensaje de alerta que dice que no hemos puesto correctamente el DNI en un formulario.

Todo esto que se ha mencionado (HTML, CSS y javascript) está escrito en uno o varios documentos y alojado en un ordenador que sirve páginas en Internet. Esa máquina utiliza un software que le permite exhibir esas páginas, por ejemplo, Apache, que es uno de los más conocidos. Cuando queremos acceder a este tipo de contenidos, escribimos la dirección de Internet en la barra de direcciones del navegador y, por medio de unos protocolos establecidos, se accede al ordenador que contiene el documento que buscamos y el servidor Apache de ese ordenador lo sirve.

### Páginas dinámicas

¿Qué ocurre si lo que estamos buscando en Internet no responde a un contenido estático sino a algo dinámico, es decir, no a un documento que ya está escrito, sino a algo que va a construirse para nosotros en el momento de nuestra petición? Por ejemplo, cuando vemos la primera página de una plataforma Moodle, vemos, entre otras cosas, un listado de cursos disponibles para alumnos/as: aparece el nombre del curso, el nombre de los profesores/as y una descripción del curso con una imagen.

Al escribir en el navegador la dirección de una primera página de Moodle, por ejemplo, [http://formacionprofesorado.educacion.es/apls/moodle/](http://formacionprofesorado.educacion.es/apls/moodle/), se ha pedido del servidor un documento PHP, un archivo. En el archivo hay instrucciones escritas en PHP que contienen consultas o preguntas que se hacen a una base de datos.

Para que una aplicación dinámica funcione, requiere que en el ordenador que nos sirve las páginas se cumplan algunos requisitos. Por ejemplo, en el caso de Moodle tiene que haber:

1. Un servidor de página web. Aunque puede haber otros, ya hemos apuntado anteriormente que uno de los más utilizados es Apache. Su función consiste en que, cuando llegue una petición de un documento determinado por una vía adecuada, él sirva la página pedida.<br/><br/>
<li>
<table align="right" border="0">
<tbody>
<tr>

![](https://raw.githubusercontent.com/catedu/curso-moodle/master/img/Crystal_Clear_mimetype_source_php.png)
</tr>
<tr>
<td>
**Fig. 1.3 Logo de PHP<br/>Obtenido en [Wikipedia](http://commons.wikimedia.org/wiki/File:Crystal_Clear_mimetype_source_php.png?uselang=es).<br/><em style="font-size: 0.8em; text-align: justify;">(Imagen con Licencia <br/>Pública General Reducida <br/>de GNU)**</em>
</td>
</tr>
</tbody>
</table>
Una serie de documentos, de archivos, escritos en un lenguaje de programación que se denomina PHP. En estos documentos escritos en PHP hay código que genera HTML y consultas de varios tipos a una base de datos. Cuando Apache está correctamente configurado y le llega una petición de una página dinámica, sabe que tiene a su disposición un intérprete de PHP que entiende el lenguaje y produce respuestas apropiadas a las peticiones que se hacen.<br/><br/></li>
1. Una base de datos, en principio, son una serie de datos integrados en tablas, es decir, filas y columnas. En las filas va la información de un registro; digamos que hay un registro por cada elemento de una tabla. Por ejemplo, si tuviéramos una tabla con nuestros CDs, en cada fila iría un CD que constituiría un registro. De ese CD tendríamos diversos datos: el nombre del artista, el nombre del disco, la fecha de edición, etc. Cada uno de estos datos iría en una columna y a cada uno de ellos les llamamos "campo". Cada base de datos tiene varias tablas. Las aplicaciones dinámicas utilizan un gestor de base de datos para crear, mantener y modificar la base de datos. Un gestor ampliamente utilizado con Moodle es MySQL.

Hay que fijarse en que tanto los datos como la presentación han sido preparados en ese momento. No es una tabla que ya estaba escrita, sino un documento que se ha creado para nosotros.

Cuando hacemos alguna interacción con Moodle, está sucediendo algo parecido, pero puede que el resultado de nuestra interacción no sea una simple lectura de datos en una base de datos y su consiguiente exposición en pantalla; puede que sea una modificación del contenido de las tablas. Imaginemos que estamos contestando una tarea en línea en Moodle; en esta tarea tenemos que escribir nuestra respuesta en un una caja de texto y enviarla para que la lea nuestro profesor a distancia. Lo que se hace es poner en marcha una página PHP, que lleva unas instrucciones para que lo que escribimos en la caja de texto se introduzca en un campo de una base de datos. Así, cuando nuestro profesor/a entre a ver nuestra respuesta, volverá a pedirse mediante instrucciones PHP que se consulte cuál fue nuestra respuesta y se exponga en la pantalla. Es más, si podemos editar nuestra contribución, la correspondiente combinación de PHP y MySQL cambiaría la antigua anotación en la base de datos por nuestra nueva respuesta. O sea que el resultado a veces no es una mera consulta, sino que modifica el contenido de una campo o más dentro de  una base de datos. &lt;p"&gt;

### 
Lenguajes y programas que encontramos relacionados con Internet



El extraordinario desarrollo de Internet está relacionado con una serie de lenguajes de programación y otros programas de los cuales mencionamos algunos a continuación:



Lenguajes de cliente. Llamados así porque se interpretan en el ordenador local: es el navegador del ordenador del usuario el que trabaja con ellos. 


<li>
	HTML:  HyperText Markup Language o Lenguaje de Marcado de Hipertexto, en español. Si nos fijamos en nuestro navegador de Internet cuando esté accediendo
	a páginas escritas en este lenguaje, éstas tendrán la extensión htm o html (o
	sea .htm o .html). </li>
- CSS: Cascading Style Sheets u Hojas de estilo en cascada, en español.
<li>JavaScript: lenguaje de programación.
	</li>


Software de servidor: se halla en el servidor de Internet, en el ordenador remoto.


- PHP Hypertext Pre-processor o Pre-procesador de hipertexto PHP, en español. Es un lenguaje de programación. Si nos fijamos en nuestro navegador de Internet, cuando esté accediendo a páginas escritas en este lenguaje, éstas tendrán la extensión php (o sea .php). 
- MYSQL:  Structured Query Language o Lenguaje de Consulta Estructurado, en español. Es un sistema de gestión de bases de datos. 
- Apache: es el servidor de páginas web.


Obtención de datos estadísticos:


<li>
	Datos de uso de servidores web:<br/>
[http://news.netcraft.com/archives/category/web-server-survey/](http://news.netcraft.com/archives/category/web-server-survey/)
</li>
<li>
	Datos de uso de navegadores de Internet:
	<br/>
[http://www.w3schools.com/browsers/browsers_stats.asp](http://www.w3schools.com/browsers/browsers_stats.asp)
</li>

## Algunas siglas que conviene conocer:


 


- **URL:** Uniform Resource Location: es un nombre que se utiliza para designar un documento en Internet. Sirve para localizar e identificar el documento.  

- **CMS: **Content Management System o Sistema de Gestión de Contenidos, en español. Programas que sirven para organizar y exponer contenidos. Se basan en sistemas de web dinámica.

- **LMS: **Learning Management System o Sistema de Gestión de Aprendizajes, en español.

