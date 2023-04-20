## POO en Python

Dadas el siguiente programa de Python:

```
class Figura:
    def __init__(self,nombre):
        self.nombre = nombre
    def calcular_area(self):
        pass
    def calcular_perimetro(self):
        pass
    def __str__(self):
        return self.nombre

class Circulo(Figura):
    def __init__(self, radio):
        self.radio = radio
        super().__init__("Circulo")
    def calcular_area(self):
        return pi * self.radio ** 2
    def calcular_perimetro(self):
        return 2 * pi * self.radio

class Cuadrado(Figura):
    def __init__(self, lado):
        self.lado = lado
        super().__init__("Circulo")
    def calcular_area(self):
        return self.lado ** 2
    def calcular_perimetro(self):
        return 4 * self.lado

class Triangulo(Figura):
    def __init__(self, base, altura):
        self.base = base
        self.altura = altura
        super().__init__("Triangulo")
  def calcular_area(self):
        return self.base * self.altura / 2
    def calcular_perimetro(self):
        return self.base + 2 * (self.altura ** 2 + self.base ** 2) ** 0.5
```



Responder a las siguientes preguntas.

## Cuestionario

1. ¿Qué clase es la clase base en este programa?
   1. La clase base es figura.
2. ¿Qué métodos tienen todas las clases en común?
   1. Tienen los métodos en común, *calcular_area*, *calcular_perimetro* y *str*.
3. ¿Qué método se debe implementar en cada clase derivada para calcular el área de la figura?
   1. Se debe implementar *calcular_area.*
4. ¿Qué método se debe implementar en cada clase derivada para calcular el perímetro de la figura?
   1. Se debe implementar *calcular_perimetro*.
5. ¿Qué significa la palabra clave `super()` en el método `init` de las clases derivadas?
   1. Es una función que llama a un método existente de la clase heredada y la incorpora a la subclase.
6. ¿Qué método se utiliza para imprimir el nombre de la figura?
   1. Se utiliza el método str para imprimir el nombre de figura.
7. ¿Qué es la herencia en programación orientada a objetos (POO)? ¿Cómo se aplica en las clases `Circulo`, `Cuadrado` y `Triangulo` del programa?
   1. Es un paradigma de la programación que permite crear una clase a partir de otra heredando sus propiedades.
   2. A la hora de crear la clase señalamos entre paréntesis (animal) de la clase que va heredar como podemos observar en el constructor de cada subclase llamamos al constructor de la clase con super para añadir el nombre a estas y los métodos que tienen son re escribidos.
8. ¿Qué es el polimorfismo en POO? ¿Cómo se aplica en las clases `Circulo`, `Cuadrado` y `Triangulo` del programa?
   1. Es la capacidad que permite un objeto tomar diversas formas, teniendo en común una clase la cual hereda sus propiedades (métodos..etc.), en estos ejemplos podemos observar los métodos que comparten son los mismos pero han sido ajustados respecto a su subclase.
9. ¿Qué es la encapsulación en POO? ¿Cómo se aplica en las clases del programa presentado?
   1. La encapsulación es un mecanismo que permite controlar la accecibidad de las propiedades de las clases, en este caso tenemos a al constructor init y el método str
10. ¿Qué es la abstracción en POO? ¿Cómo se aplica en las clases del programa presentado?
    1. La abstracción es un mecanismo que obliga a implementar a las clases unos métodos definidos en las clase de la que heredan, en estos ejemplos podemos observar que la clase animal a definido los métodos de calcular área y perímetro y las clases son las encargadas de implementarlas adaptándolas a las necesidades de cada subclase.

