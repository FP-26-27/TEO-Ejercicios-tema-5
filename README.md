# Ejercicios del tema 5: Secuencias, listas y tuplas

Cree una carpeta ``src``, y dentro de la misma un archivo ``ejercicioX.py`` para cada ejercicio que vaya a resolver, sustituyendo la X por el número del ejercicio. Implemente en cada archivo la función solicitada por el ejercicio correspondiente, asegurándose de que las pruebas de la función se realicen como programa principal.

### Ejercicio 1: operaciones con secuencias

#### Apartado a)
Sea una lista con nombres de colores. Escriba la instrucción que hemos de utilizar en cada caso para obtener en pantalla la salida indicada.

```python
colores = ["rojo", "verde", "azul", "amarillo", "magenta", "negro"]

# Salida: ["rojo", "verde", "azul"]
print()

# Salida: ["rojo", "verde", "rojo", "verde", "rojo", "verde", ]
print()

# Salida: ["rojo", "verde", "blanco"]
print()

# Salida: El color azul está en la posición 3
print()

# Salida: El último color es el negro
print()

# Salida: ¿El color naranja está en la lista? False
print()
```

#### Apartado b)
Sea una lista de notas. Escriba la instrucción que hemos de utilizar en cada caso para obtener en pantalla la salida indicada.

```python
notas = [7.5, 8.2, 9.1, 6.5, 10, 9, 8.7, 9]

# Salida: La mayor nota es: 10
print()

# Salida: Lista de notas de mayor a menor: [10, 9.1, 9, 9, 8.7, 8.2, 7.5, 6.5]
print()

# Salida: Lista de notas invertida: [9, 8.7, 9, 10, 6.5, 9.1, 8.2, 7.5]
print()

# Salida: La nota '9' aparece 2 veces
print()
```

#### Apartado c)
Sea una lista de lenguajes. Escriba la instrucción que hemos de utilizar en cada caso para obtener en pantalla la salida indicada.

```python
lenguajes = [("C", 1972), ("Java", 1995), ("Python", 1991), ("Pascal", 1970), ("C++", 1980)]

# Salida: Lenguajes en orden alfabético: [('C', 1972), ('C++', 1980), ('Java', 1995),
#         ('Pascal', 1970), ('Python', 1991)]
print()

# Salida: El lenguaje más reciente es: ('Java', 1995)
print()

# Salida: El nombre del lenguaje más reciente es: Java
print()
```

#### Apartado d)
Escriba una función que reciba una lista y un valor ``tamaño`` y devuelva una lista que tenga como máximo el número de elementos dados por ``tamaño``. Si tiene menos elementos, se quedará como está.

```python
def acorta_lista( ):
    pass
```

Escriba llamadas a la función anterior con la lista que se proporciona y los valores de tamaño que se indican.

```python
lista = ['Roma', 'París', 'Berlín', 'Madrid', 'Helsinki', 'Viena', 'Amsterdam']

print("Lista acortada a 5 ciudades:", )
print("Lista acortada a 20 ciudades:", )
```

#### Apartado e)
Tenemos una lista con las puntuaciones obtenidas por un restaurante a lo largo del tiempo, que son valores comprendidos entre 1 y 5. Complete el código para obtener la valoración media de todas la puntuaciones, y la valoración media de las 5 últimas puntuaciones.


```python
valoraciones = [3, 4, 4, 3, 4, 5, 3, 4, 2, 4, 4, 5, 4, 2, 5, 5, 4, 3, 5, 4, 5]

valoracion_media = 
print(valoracion_media)

suma_ultimas_5 = 
valoracion_media_ultimas_5 = 
print(valoracion_media_ultimas_5)
```

### Ejercicio 2: Operaciones con listas 

Sea la lista `planetas`. Escriba las instrucciones que transforman esta lista en la lista ['Mercurio', 'Venus', 'Tierra', 'Marte']

```python
planetas =["Luna", "Mercurio", "Tierra"]

print(planetas)
```

### Ejercicio 3: Listas por comprensión

El siguiente código obtiene los nombres de los planetas del sistema solar que se encuentran en la llamada [zona de habitabilidad](https://es.wikipedia.org/wiki/Zona_de_habitabilidad).

```python
from collections import namedtuple

Planeta = namedtuple('Planeta', 'nombre, distancia_al_sol')

def planetas_habitables_bucle(planetas_y_distancias, d_min, d_max):
    planetas_habitables = []
    for p in planetas_y_distancias:
        if d_min <= p.distancia_al_sol <= d_max:
            planetas_habitables.append(p.nombre)
    return planetas_habitables

if __name__ == '__main__':
    planetas_y_distancias = [Planeta('Mercurio', 0.39), Planeta('Venus', 0.72),
        Planeta('Tierra', 1.0), Planeta('Marte', 1.53), Planeta('Júpiter', 5.2)]
    d_min = 0.84
    d_max = 1.67
    print(f"Planetas habitables (bucles): {planetas_habitables_bucle(planetas_y_distancias, d_min, d_max)}")
```

Escriba una función `planetas_habitables_comprension` que cree la lista `planetas_habitables` por comprensión.

La lista `puestos` contiene las posiciones ocupadas por un jugador en el ranking a lo largo de la temporada. Complete el código para crear, por comprensión, otra lista que contenga las diferencias entre cada dos posiciones consecutivas, y a partir de ella, mediante un generador por comprensión, el número de puestos que ha subido el jugador en toda la temporada.

```python
def calcula_diferencias(puestos):
    variacion = 
    puestos_subidos = 
    return puestos_subidos

if __name__ == '__main__':
    puestos = [1, 5, 6, 4, 2, 4, 2, 1, 2, 3, 3, 2, 2, 1, 1, 1]
    print(f"Total de puestos subidos: {calcula_diferencias(puestos)}")
```

### Ejercicio 4: Tuplas con nombre

Redefina la tupla `Planetas` usando `NamedTuple` y añadiendo los tipos de los campos. A continuación, cree una tupla para el planeta Marte.


Defina mediante `NamedTuple` una tupla `Persona` con los siguientes campos:
- **nombre**: nombre de la persona
- **fecha_nacimiento**: fecha de nacimiento
- **medidas**: tupla que contiene el peso en kilos y la estatura en centímetros
- **aficiones**: conjunto de cadenas con las aficiones de la persona

A continuación, cree una tupla `persona` que represente a una persona de nombre María, nacida el 19 de noviembre de 2005, con 172 cm de estatura y 61.5 kgs de peso, y con afición por el Tenis, la Música y los Viajes.

