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

Antes de continuar es importante conocer lo que es el polimorfismo. 
Como ya vimos antes, es posible hacer clases heredadas, es decir,  que a partir de una clase poder crear una subclase más especifica, tal fue el caso desde la clase Mamífero a Persona, siendo esta una nueva subclase derivada de Mamífero. 

El **Polimorfismo** se refiere a la capacidad que tiene el lenguaje de, a partir de una clase con un método no implementado, generar nuevas subclases que implementen ese método solo definido y hacerlo de manera distinta para cada subclase si así se desea, a continuación mostrará un ejemplo códficado en Java ya que en este lenguaje deberá ser escrito el proyecto y además claro que es un lenguaje orientado a objetos

**Ejemplo:**
``` java
// Clase base Animal
class Animal {
    public void hacerSonido() {
        // Método base sin implementación específica
    }
}

// Clase derivada Perro
class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Woof!");
    }
}

// Clase derivada Gato
class Gato extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Miau!");
    }
}

public class Main {
    // Función que usa polimorfismo
    public static void hacerRuido(Animal animal) {
        animal.hacerSonido();
    }

    public static void main(String[] args) {
        // Crear instancias de las clases derivadas
        Perro perro = new Perro();
        Gato gato = new Gato();

        // Llamar a la función hacerRuido con diferentes objetos
        hacerRuido(perro);  // Output: "Woof!"
        hacerRuido(gato);   // Output: "Miau!"
    }
}

```

**Explicación:**
 1. Clase Animal: 
		Primero se crea una clase llamada *Animal*, esta solo contiene un método o acción, esta es **hacerSonido()**, como se puede observar, antes tiene escrito las palabras *public void*. 
			**Public:** Es un modificador que especifica quién tiene acceso a este método, el modificador **public** permite que el método *hacerSonido()* sea accesible desde cualquier parte del programa.
			**Void:** Ya lo conocemos bien desde el lenguaje C, este funciona para especificar el tipo de retorno de la función, el caso de Void es que nunca devolverá algo o ningún valor, solo se ejecutará pero no será necesario regresar ningún valor de esta.
		Como se puede ver el método **public void hacerSonido()** está definido, pero no implementado, es decir, existe pero no se dice realmente qué hace esa acción, esta abierto a que se defina, es un método vacío, no implementado. 
		
2. Clase Perro: 
		Tiene escrito **class Perro extends Animal**, esta sintaxis funciona para lo siguiente:
			**class Perro** especifica que se esta creando una clase llamada Perro, la parte extends es la que hace que la clase Perro se vuelva una clase heredada de **Animal**.
			Por lo tanto se trata de la declaración de una nueva clase llamada **Perro** que es heredada de Animal por medio de la palabra **extends**, esto significa que heredará sus variables (atributos o propiedades) y métodos (acciones)