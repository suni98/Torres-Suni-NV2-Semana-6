# Torres-Suni-NV2-Semana-6
# Clase base
class Animal:
    def __init__(self, nombre, edad):
        self._nombre = nombre  # Atributo protegido (encapsulación)
        self._edad = edad  # Atributo protegido (encapsulación)

    def hacer_sonido(self):
        raise NotImplementedError("Subclase debe implementar este método")

    def info(self):
        print(f"Soy un animal llamado {self._nombre} y tengo {self._edad} años.")

# Clase derivada Perro
class Perro(Animal):
    def __init__(self, nombre, edad, raza):
        super().__init__(nombre, edad)
        self._raza = raza  # Atributo protegido (encapsulación)

    def hacer_sonido(self):
        print("Guau guau!")

    def info(self):
        print(f"Soy un perro de raza {self._raza}, me llamo {self._nombre} y tengo {self._edad} años.")

# Clase derivada Gato
class Gato(Animal):
    def __init__(self, nombre, edad, color):
        super().__init__(nombre, edad)
        self._color = color  # Atributo protegido (encapsulación)

    def hacer_sonido(self):
        print("Miau miau!")

    def info(self):
        print(f"Soy un gato de color {self._color}, me llamo {self._nombre} y tengo {self._edad} años.")

# Polimorfismo a través de métodos sobrescritos
def describir_animal(animal):
    animal.info()
    animal.hacer_sonido()

# Crear instancias de las clases y usar sus métodos
perro = Perro("Firulais", 5, "Labrador")
gato = Gato("Michi", 3, "Blanco")

describir_animal(perro)  # Polimorfismo
describir_animal(gato)   # Polimorfismo
