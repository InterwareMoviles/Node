# Estándares de programación en Node.js
Estructura de código
--------------------
La estructura de directorios sigue un patrón MVC:

> |--app
> |.......|--controllers/<br>
> |.......|--routes/<br>
> |.......|--models/<br>
> |.......|--views/<br>
> |.......|--public/<br>
> |.......|--node_modules/<br>
> |--app.js


|  Directorio  |  Descripción  |
|---|---|
|controllers|Archivos que concentran la funcionalidad, son consultados normalmente por las rutas. La convención de nombres es xxxController.js|
|models|Contiene los archivos ORM (Schemas en mongoose). La convención de nombres es: xxx.js|
|views|Contiene las vistas o templates del proyecto. La convención de nombres es xxx.js|
|public|Contiene todo el contenido estático, assest’s, css’s, js’s|
|config| Archivos de configuración que se utilizan en el proyecto|
|routes|Contiene todas las rutas de express, separados por módulos de la aplicación. La convención de nombres  es xxxxRoute.js|
|app.js|Entry point de la aplicación.|
Dónde xxx es un nombre en inglés que describe el contenido del código. 


## Estándares de codificación ##

Los estándares de codificación aseguran la calidad del código lo cual se traduce en:

 - Mejora la lectura del código.
 - Hace sencillo el mantenimiento del código.

**Convención de nombres**

- Siempre utilizar camelCase para nombrar variables y funciones.
- Todos los nombres deben iniciar con una letra.

Ejemplo:

    firstName = "John";
    lastName = "Doe";
    price = 19.9;
    tax = 15;

**Espacios**
<br>Siempre poner espacios antes y después de los operadores ( = + - * /)

    var x = y + z;
    var values = ["este", "es", "un", "ejemplo"];

- Esto aplica también para el operador ; en un for statement
- Después de la palabra reservada function.
- Después de una palabra reservada que se encuentre antes de un signo (
- Después de una “,” 

**Identación de código**
- El código debe ser identado por 2 espacios.
- No usar TABS para identar
- Evitar la líneas muy largas, los lugares ideales para poner un salto de línea son después de: ( paréntesis izq, [ bracket izq, , comma o antes de . punto, ? signo de interrogación o : dos puntos.
- Poner punto y coma al final de cada línea.

**Comentarios**

 - Ser generoso con los comentarios. 
 - Evitar poner comentarios obvios.

Por ejemplo:

    var i = 0 // set variable to zero

- Mantener los comentarios actualizados.
- Utilizar bloques de código /**/ para documentación formal.

**If Statement**
<br>La estructura if, debe tener siempre la siguiente forma:

    if (condition) {
	    statements
	} else if (condition) {
		statements
	}else {
		statements
	}
	
**Switch Statement**
<br>La estructura switch, debe tener siempre la siguiente forma:

    switch(expression) {
	    case expression:
		    statements
		default:
			statements
	}

**Try Statement**
<br>La estructura try-catch, debe tener siempre la siguiente forma:

    try {
	    statements
	} catch (variable) {
		statements
	} finally {
		statements
	}

**Asignaciones**

 - No realizar asignaciones en la parte condicional de una estructura if
   o while. 
 - Usa === o !=== para condicionales, Los operadores != y == no
   verifican el tipo y no deben ser usados para mejorar la legibilidad
   del código.
