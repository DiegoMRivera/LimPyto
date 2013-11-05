LimPyto
=======

En mi trabajo de desarrollo web (maquetado y programación), debo muchas veces retomar códigos fuente HTML que sea están mal estructurados y/o presentados de manera desprolija, desordernada. En tales casos, debo revisar el código línea por línea, identificar los errores (ej.: presencia de html obsoleto, etiquetas html mal cerradas, etc.) y proceder a las correcciones; lo que me lleva mucho tiempo. Normalmente voy a utilizar aplicaciones que se encuentran en la web como "FREEFORMATTER" (http://www.freeformatter.com) aunque me gustaría crear una aplicación propia que puedo modificar según mis necesidades.

Objetivo:

Mi objetivo entonces es de programar una pequeña aplicación usando Python (of course!) que analizará un archivo o página html y corrigirá y ordenará el código según los siguientes criterios:
	
	-Identificar el "DOCTYPE" de la página o archivo HTML (HTML5 o HTML 4.01)
	-Validar luego el código HTML según W3C Markup Validation Service.
	-Corregir automáticamente ciertos errores obvios (ej.: barra de cierre al final de los 	elementos <br>, <input>, <img src>, etc.)
	-Identificar etiquetas abiertas que no han sido cerradas; mostrar cuáles son y esperar que el 	problema sea corregido antes de seguir adelante.
	-Ordenar el código según el DOM  y la relación jerárquica entre sí separando los elementos 	con una indentación de 4 espacios. 
		
		Ejemplo:

	<html>
		<head>
			<title></title>
		</head>
		<body>
			<div id="main">
				<div id="content">
				<h1>Hola Mundo</h1>
				<p>Look at the bright side of life</p>
					<div class="subContent">
						<h2>Adios mundo cruel</h2>
					</div>
				</div>
			</div>
		</body>
	</html>
            
    Finalmente, quisiera guardar el resultado final en un archivo html.
