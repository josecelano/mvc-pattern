# mvc-pattern
Conceptos relacionados con MVC

La gente de https://codely.tv/ hizo un directo hace poco titulado:

Aplica MVC Correctamente con Laravel | la función CodelyTV 27
https://www.youtube.com/watch?v=0xMY40aK3fk

Iba a ponerles un comentario en el video pero como tenía varias cosas que poner lo dejo por aquí y voy agregando material según vaya descubriendo más cosas.

La discusión va de si Laravel es MVC, y de como los framework nos encaminan a acoplar persistencia con los modelos de dominio.

Solo quería comentar que en un video de Uncle Bob explica el origen del patrón MVC y de como se usaba solamente en la capa de presentación. Los conceptos clave según yo los entiendo son:

* El framework completo es la capa de delivery no contiene lógica de negocio.
* El patrón MVC se usa a nivel de la capa de presentación no es un modelo de arquitectura.
* El MVC original se usaba para pequeños componentes gráficos
* En ese contexto el modelo es solo una estructura de datos que usa en controllador y la vista.

Por lo tanto el "Model" de los frameworks se podría ver como un modelo de lectura no como un modelo de escritura. A lo mejor ahí podría estar la confusión con el paper que leen en el video, y que parece que puede encapsular la datos de la base de datos, de una API externa (no dice API sino network), etcetera.

Yo creo que habría que distinguir dos tipos de modelos distintos:
* Modelo de dominio (que es el que hacen referencia en el video con el ejemplo del usuario mayor de edad).
* Y el modelo de lectura del patrón MVC que no es más que un DTO.
El modelo de dominio es el que tiene las invarariantes de negocio (como el ejemplo del usuario mayor de edad) pero realmente los framework no nos fuerzan a que sea el "Model" (Active Record). Podríamos interpretar ese Model como modelo de lectura. Como ejemplo de esa forma de usar el framework yo hice un ejemplo hace tiempo que pueden ver aquí:
https://github.com/josecelano/ddd-laravel-sample

La charla donde Uncle Bob habla de MVC, origen y relación con arquitectura web es:
Charla Uncle Bob: What About MVC
Donde empieza a hablar de MVC: https://youtu.be/WpkDN78P884?t=1748

Creo que el que inventó el patrón es:
Trygve Reenskaug
https://en.wikipedia.org/wiki/Trygve_Reenskaug

Este es un paper (creo que anterior al que mencionan en el video)
http://heim.ifi.uio.no/~trygver/2003/javazone-jaoo/MVC_pattern.pdf

Y creo que esto debe ser donde primero se mencionó (pero no estoy seguro)
http://heim.ifi.uio.no/~trygver/themes/mvc/mvc-index.html

Esto de que el MVC es solo cosa de la capa de presentaión también lo menciona Uncle Bob en este post:
https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html
"The models are likely just data structures that are passed from the controllers to the use cases, and then back from the use cases to the presenters and views."

Y finalmente, hay un artículo de Duilio Palacios que lo explica mejor que yo:
Duilio Palacios
https://styde.net/porque-laravel-no-es-mvc-y-tu-deberias-olvidarte-de-mvc/
Y muy relacionado también con el tema del video.

Creo que hay otro video de Uncle Bob donde habla muco más de MVC pero no lo encuentro.





