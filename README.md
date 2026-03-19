# T-picos-Avanzados-de-Programaci-n--Unidad-2
# Unidad 2 - Componentes y Librerías en Python 🐍

---

## Introducción

En el desarrollo de software moderno, es fundamental construir programas organizados, reutilizables y fáciles de mantener. Para lograr esto, se utilizan conceptos como componentes, módulos, paquetes y librerías, los cuales permiten dividir un sistema en partes más pequeñas y manejables.

En Python, estos elementos son esenciales, ya que el lenguaje está diseñado para fomentar la reutilización de código y la modularidad. A través de esta unidad, se estudia cómo utilizar herramientas ya existentes y cómo crear nuestras propias soluciones reutilizables.

---

##  Objetivo de la Unidad

* Comprender el concepto de componentes, paquetes y librerías.
* Utilizar librerías propias del lenguaje Python.
* Desarrollar componentes personalizados.
* Crear y organizar paquetes o librerías propias.

---

#  2.1 Definición conceptual de componentes, paquetes y librerías

##  ¿Qué es un componente?

Un componente es una unidad independiente de software que realiza una función específica dentro de un sistema. Su principal característica es que puede ser reutilizado en diferentes partes del programa o incluso en otros proyectos.

Los componentes ayudan a:

* Dividir problemas grandes en partes pequeñas
* Facilitar el mantenimiento del código
* Mejorar la legibilidad

###  Tipos de componentes

**1. Componentes funcionales (no visuales):**
Son aquellos que realizan operaciones internas.

Ejemplo:

```python
def calcular_promedio(lista):
    return sum(lista) / len(lista)

print(calcular_promedio([8, 9, 10]))
```

**2. Componentes visuales:**
Se utilizan en interfaces gráficas (GUI).

Ejemplos:

* Botones
* Ventanas
* Formularios

---

##  ¿Qué es una librería?

Una librería es un conjunto de funciones, clases y herramientas previamente desarrolladas que permiten resolver problemas comunes sin necesidad de programarlos desde cero.

###  Importancia de las librerías

* Reducen el tiempo de desarrollo
* Evitan errores al reutilizar código probado
* Permiten acceder a funcionalidades avanzadas

###  Ejemplo con librería math

```python
import math

numero = 25
raiz = math.sqrt(numero)
potencia = math.pow(2, 3)

print("Raíz:", raiz)
print("Potencia:", potencia)
```

---

##  ¿Qué es un paquete?

Un paquete es una estructura que agrupa múltiples módulos en una carpeta. Sirve para organizar proyectos grandes.

###  Ejemplo de estructura de paquete

```
mi_proyecto/
│
├── main.py
├── utilidades/
│   ├── __init__.py
│   ├── operaciones.py
│   └── validaciones.py
```

---

# 🔹 2.2 Uso de librerías proporcionadas por el lenguaje

Python incluye una gran cantidad de librerías estándar que permiten realizar diversas tareas.

---

##  Librería math

Se utiliza para operaciones matemáticas.

```python
import math

print("Valor de PI:", math.pi)
print("Redondeo hacia arriba:", math.ceil(4.2))
print("Raíz cuadrada:", math.sqrt(81))
```

---

##  Librería random

Permite generar valores aleatorios.

```python
import random

print("Número aleatorio:", random.randint(1, 100))
print("Elemento aleatorio:", random.choice(["A", "B", "C"]))
```

---

##  Librería datetime

Se utiliza para manejar fechas y horas.

```python
from datetime import datetime

fecha_actual = datetime.now()

print("Fecha y hora actual:", fecha_actual)
print("Año:", fecha_actual.year)
```

---

##  Librería os

Permite interactuar con el sistema operativo.

```python
import os

print("Directorio actual:", os.getcwd())
```

---

##  Ventajas del uso de librerías

* Código más eficiente
* Desarrollo más rápido
* Mejor organización
* Acceso a herramientas avanzadas

---

# 🔹 2.3 Creación de componentes definidos por el usuario

Crear componentes propios permite personalizar soluciones y reutilizar código.

---

##  Funciones como componentes

```python
def saludar(nombre):
    return f"Hola, {nombre}"

print(saludar("Noel"))
```

---

##  Clases como componentes (POO)

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def mostrar_datos(self):
        print(f"Nombre: {self.nombre}, Edad: {self.edad}")

p1 = Persona("Noel", 20)
p1.mostrar_datos()
```

---

##  Componentes reutilizables

```python
def es_par(numero):
    return numero % 2 == 0

print(es_par(10))
```

---

##  Componentes visuales (interfaz gráfica)

Ejemplo básico usando Tkinter:

```python
import tkinter as tk

ventana = tk.Tk()
ventana.title("Mi aplicación")

label = tk.Label(ventana, text="Hola mundo")
label.pack()

ventana.mainloop()
```

---

# 🔹 2.4 Creación y uso de paquetes/librerías propias

---

##  Crear un módulo propio

Archivo: operaciones.py

```python
def suma(a, b):
    return a + b

def multiplicacion(a, b):
    return a * b
```

---

##  Usar el módulo

```python
import operaciones

print(operaciones.suma(5, 5))
print(operaciones.multiplicacion(3, 4))
```

---

##  Crear un paquete

Estructura:

```
mi_libreria/
│
├── __init__.py
├── operaciones.py
├── calculos.py
```

---

##  Importar desde paquete

```python
from mi_libreria import operaciones

print(operaciones.suma(2, 3))
```

---

##  Ventajas de crear librerías propias

* Reutilización de código
* Mejor organización
* Escalabilidad del proyecto
* Facilita el trabajo en equipo

---

#  Ejemplo integrador

```python
# archivo operaciones.py
def suma(a, b):
    return a + b

# archivo main.py
import operaciones

resultado = operaciones.suma(10, 20)
print("Resultado:", resultado)
```

---

#  Conclusión

El uso de componentes, librerías y paquetes es fundamental en el desarrollo de software moderno. Permiten crear aplicaciones más estructuradas, eficientes y fáciles de mantener. Python facilita enormemente este proceso gracias a su simplicidad y su amplio ecosistema de librerías.

---

# 🚀 Aplicaciones en la vida real

Estos conceptos se utilizan en:

* Desarrollo web (Django, Flask)
* Ciencia de datos
* Automatización
* Desarrollo de interfaces gráficas
* Sistemas empresariales

---

# 👨‍💻 Autor

Nombre: Noel Castillo Villanueva
Materia: Tópicos Avanzados de Programación
Unidad: 2
