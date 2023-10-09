La Programación Orientada a Objetos toma un paradigma totalmente distinto a lo visto antes en C. 
En la programación orientada a objetos es importante conocer lo que es la ***abstracción*** como concepto elemental, ya que es uno de los cuales esta fuertemente cimentado.

**Abstracción**: Proceso en el que se toman en cuenta los detalles más importantes de un ente de la realidad, así logrando crear una representación sintetizada del ente original.

Otro concepto de igual manera importante es el de clase, pero primero debemos preguntarnos. ¿Qué es **clasificar**?

**Clasificar**: Es el proceso mediante el cuál a partir de un conjunto se agrupan elementos de este mismo en otros subconjuntos nuevos, según sus características o propiedades similares.

Esto se puede ya empezar a ver desde un punto de vista de *Programación Orientada a Objetos.*

Una clase de manera primitiva se observa de esta manera:
```
Clase ={Propiedades = {Propiedad_1, Propiedad _2, Propiedad_3 ... Propiedad_n}
Acciones = {Accion_1, Accion_2, ... Accion_m}}
```
Un ejemplo de una clase es:
```
Mamifero = {Propiedades = {Ojos, Naríz, Boca, ...}
			Métodos = {Comer(), Dormir(), Caminar()}}
```
La clase *Mamífero* tiene sus características o propiedades como un conjunto especifico de seres vivos y también métodos, estos son como funciones o acciones que lleva a cabo un mamífero.

La clase Mamífero es una clase porque sabemos que dentro del gran conjunto que son los seres vivos, los mamíferos son un subconjunto de los seres vivos que comparten características especificas que al cumplirlas es posible que entren a este subconjunto.

Una instancia es es un objeto de una clase, es decir, mamífero es mi clase, pero esto abarca a todos los seres vivos, si yo quiero referirme solo a un mamífero tengo a los *perros*, *gatos*, *humanos*, etc. Todos estos son objetos de la clase Mamífero, ya que cumplen con las características de uno. 
Por lo tanto las instancias de la clase ***Mamífero*** pueden ser las siguientes:
```
Mamíferos = {Perro, Gato, Persona, ...}
```
De manera que se puede decir que Mamíferos nació desde el conjunto enorme o clase enorme de los seres vivos en general, también es posible crear un nuevo subconjunto a partir del conjunto Mamíferos, esta se llamará **subclase** ya que se deriva de una clase especifica.

En este ejemplo sabemos que uno de los objetos o cosas que cumplen las características para ser considerado parte de la clase Mamífero es *Persona*, pero de esta se pueden derivar otras instancias según que también cumplen las características de *Mamífero* y de *Persona*, por lo que *Persona* se convierte en una subclase de *Mamífero* que cumplen otras características más especificas, un ejemplo de como se vería las instancias u objetos de esta subclase es la siguiente:
```
Persona{Doctor, Luis, Maestra, Mamá, Emperador, Cliente}
```
#### Polimorfismo

Antes de continuar es importante conocer lo que es el polimorfismoç

ACabar de explicar poliformismos con diagramas de flujo de mermaid de tipo clase, impmmenteacion de ejemplo de chat gpt, explicacion detallada y yap, Suerte Fidel del futuro, siempre quieres hacer muchas cosas y no te da timepo, mañanan te levantas como a la 6 y ya son las 2 aeme,, pide ayuda
