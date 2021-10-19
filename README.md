# Recogida de información I (Buscadores, Shodan, GHDB)

## Práctica del módulo de **Seguridad y Alta Disponibilidad** de ASIR para el IES Punta del Verde

- Alumno: Angel Ignacio Rodriguez
- Curso: 2ºB - A.S.I.R.


Se realizara una documentacion en formato de texto y video para este ejercicio que consiste en el uso combinado de dorks para uso en busquedas en Google y Bing.
Tambien se documentara del uso de Shodan, un buscador para encontrar equipos conectados a internet, desde una cámara o una nevera inteligente a un servidor. Además permite realizar búsquedas avanzadas y permite saber información sobre los mismos, por ejemplo, puertos abiertos/filtrados con los servicios disponibles.

-----------------------------------------------------------------------------------------------------------------------------

### Hacking con buscadores como Google, Bing o Shodan

-	## Que son los archivos “robots.txt”

El archivo robots.txt es un archivo de texto plano en el cual se configurarán las páginas web que, de cara a los rastreadores de Google, queremos o no que se muestren.
En los archivos “robots.txt” las etiquetas más usadas son “Disallow” y “Allow”.
Con “Disallow” le estaremos diciendo a los rastreadores de Google que no muestre ese archivo y/o directorio y la etiqueta “Allow” hará lo contrario, decirles a los navegadores que si debe mostrar en las búsquedas.


-	## Obtención de información y hacking con robots.txt

Realizando una búsqueda más refinada, podremos obtener información sobre directorios y/o archivos los cuales pueden contener información sensible de terceros o privilegiada.


### Ejemplos de búsquedas:
-	inurl:robots.txt filetype:txt "Disallow: /phpmyadmin"
-	inurl:"/robots.txt" + "Disallow: passwords.txt"


-   ## Dorks

A la hora de realizar una búsqueda en Google, hay ciertas palabras clave y operadores que funcionan como un lenguaje de consulta estructurado y los mismos se utilizan para filtrar los resultados.
Los usuarios pueden apoyarse en estos operadores para encontrar resultados relevantes de forma más rápida y precisa, aunque, por otra parte, una persona con fines malintencionados podría utilizar estas mismas técnicas para obtener información sensible, y esto es lo que se conoce como “Google Dorks” o "Bing Dorks"


-	## Google Dorks

Aquí dejo algunos de los ejemplos interesantes de Dorks para la búsqueda avanzada en Google:

-	index.of.dcim => Búsqueda de resultados indexados de páginas webs de dispositivos móviles.

-	“you have an error in your sql syntax” inurl:/events.php?id= => búsqueda de errores en bases de datos SQL


-	## Operadores de Bing 

Ejemplos de operadores y búsquedas con ellos en Bing:
-	ext:pdf google hacking => Con “ext” podemos buscar un tipo de extensión concreta.

-	contains:pdf => Nos muestra URL’s que contenga un pdf

-	intitle:index => Al igual que en Google, nos buscara en el título de la pagina

-	domain:facebook.com => nos buscara toda la información de un dominio en concreto


-	## Bing Dorks

Ejemplos de dorks y búsquedas con ellos en Bing:
-	contains:rdp intitle:”index.of” => nos buscara en el titulo archivos indexados de rdp que son Escritorios remotos

-	feed:hacking loc:es => Buscara canales RSS relacionados con el hacking en dominios de España (no tiene por qué estar en español)


-	## Shodan

Shodan es un motor de búsqueda en el que, a diferencia de Google y otros buscadores, no podemos buscar, por ejemplo, una imagen o un texto.

Este motor de búsqueda está enfocado únicamente a buscar sistemas y servicios conectados a internet.

Ejemplos de operadores:
-	country (filtrar por países)

-	port (filtrara por puertos)

-	title (buscara por cabeceras)

-	os (nos filtrara por sistema operativo)

Ejemplos de Dorks:
-	port:5432 PostgreSQL

-	producto:MySQL

-	country:es os:"Playstation 4"

-	Android Webcam Server -Authenticate
