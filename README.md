![Diferencias sintaxis entre JavaScript y Python](https://github.com/sergiecode/diferencia-js-y-py/blob/master/js_y_py.jpg?raw=true)

# Diferencias básicas de sintaxis entre JavaScript y Python

En este documento, exploraremos algunas de las diferencias fundamentales en la sintaxis entre JavaScript y Python. Cubriremos ejemplos de declaración de variables, estructuras de control y salida en consola en ambos lenguajes.

## Declaración de variables

### JavaScript

En JavaScript, se pueden declarar variables utilizando la palabra clave `var`, `let` o `const`.

    var numero = 10;
    let texto = "Hola";
    const pi = 3.14;

### Python

En Python, no se requiere especificar el tipo de variable al declararla.

    numero = 10
    texto = "Hola"
    pi = 3.14

## Estructuras de control

### Condicional if-else

#### JavaScript

    if (edad >= 18) {
      console.log("Eres mayor de edad");
    } else {
      console.log("Eres menor de edad");
    }

#### Python

    if edad >= 18:
      print("Eres mayor de edad")
    else:
      print("Eres menor de edad")

### Bucle for

#### JavaScript

    for (let i = 0; i < 5; i++) {
      console.log(i);
    }

#### Python

    for i in range(5):
      print(i)

## Salida en consola

### JavaScript

    console.log("Hola, mundo");

### Python

    print("Hola, mundo")

## Manipulación de arrays

### JavaScript

    const numeros = [1, 2, 3, 4, 5];
    
    // Obtener la longitud del array
    console.log(numeros.length);
    
    // Acceder a un elemento específico
    console.log(numeros[0]);
    
    // Agregar elementos al final del array
    numeros.push(6);
    
    // Iterar sobre los elementos del array
    numeros.forEach((numero) => {
      console.log(numero);
    });

### Python

    numeros = [1, 2, 3, 4, 5]
    
    # Obtener la longitud del array
    print(len(numeros))
    
    # Acceder a un elemento específico
    print(numeros[0])
    
    # Agregar elementos al final del array
    numeros.append(6)
    
    # Iterar sobre los elementos del array
    for numero in numeros:
      print(numero)

## Funciones

### JavaScript

    // Definir una función
    function saludar(nombre) {
      console.log("Hola, " + nombre);
    }
    
    // Llamar a la función
    saludar("Juan");

### Python

    # Definir una función
    def saludar(nombre):
      print("Hola, " + nombre)
    
    # Llamar a la función
    saludar("Juan")

## Manipulación de cadenas de texto

### JavaScript

    const texto = "Hola, mundo";
    
    // Obtener la longitud de la cadena de texto
    console.log(texto.length);
    
    // Obtener un substring
    console.log(texto.substring(0, 4));
    
    // Reemplazar parte de la cadena de texto
    console.log(texto.replace("mundo", "amigo"));

### Python

    texto = "Hola, mundo"
    
    # Obtener la longitud de la cadena de texto
    print(len(texto))
    
    # Obtener un substring
    print(texto[0:4])
    
    # Reemplazar parte de la cadena de texto
    print(texto.replace("mundo", "amigo"))

## Objetos y Diccionarios

### JavaScript

    // Definir un objeto
    const persona = {
      nombre: "Juan",
      edad: 30,
      profesion: "Desarrollador"
    };
    
    // Acceder a propiedades del objeto
    console.log(persona.nombre);
    console.log(persona["edad"]);
    
    // Agregar una nueva propiedad
    persona.ciudad = "Madrid";
    
    // Iterar sobre las propiedades del objeto
    for (let clave in persona) {
      console.log(clave + ": " + persona[clave]);
    }

### Python

    # Definir un diccionario
    persona = {
      "nombre": "Juan",
      "edad": 30,
      "profesion": "Desarrollador"
    }
    
    # Acceder a valores del diccionario
    print(persona["nombre"])
    print(persona.get("edad"))
    
    # Agregar una nueva clave-valor
    persona["ciudad"] = "Madrid"
    
    # Iterar sobre las claves y valores del diccionario
    for clave, valor in persona.items():
      print(clave + ": " + str(valor))

## Métodos de Array/List

### JavaScript

    const numeros = [1, 2, 3, 4, 5];
    
    // Map
    const numerosDobles = numeros.map((numero) => numero * 2);
    
    // Filter
    const numerosPares = numeros.filter((numero) => numero % 2 === 0);
    
    // Reduce
    const suma = numeros.reduce((acumulador, numero) => acumulador + numero, 0);

### Python

    numeros = [1, 2, 3, 4, 5]
    
    # map
    numeros_dobles = list(map(lambda numero: numero * 2, numeros))
    
    # filter
    numeros_pares = list(filter(lambda numero: numero % 2 == 0, numeros))
    
    # reduce (requiere importar functools)
    import functools
    suma = functools.reduce(lambda acumulador, numero: acumulador + numero, numeros, 0)

## Manejo de Excepciones

### JavaScript

    try {
      // Código que podría generar una excepción
      throw new Error("Algo salió mal");
    } catch (error) {
      console.log(error.message);
    } finally {
      console.log("Este bloque se ejecuta siempre");
    }

### Python

    try:
      # Código que podría generar una excepción
      raise Exception("Algo salió mal")
    except Exception as error:
      print(str(error))
    finally:
      print("Este bloque se ejecuta siempre")

## Bucles while

### JavaScript

    let i = 0;
    while (i < 5) {
      console.log(i);
      i++;
    }

### Python

    i = 0
    while i < 5:
      print(i)
      i += 1

## Operadores lógicos

### JavaScript

    const a = true;
    const b = false;
    
    // AND
    console.log(a && b);
    
    // OR
    console.log(a || b);
    
    // NOT
    console.log(!a);

### Python

    a = True
    b = False
    
    # AND
    print(a and b)
    
    # OR
    print(a or b)
    
    # NOT
    print(not a)

## Manipulación de fechas

### JavaScript

    const fecha = new Date();
    
    // Obtener el año
    console.log(fecha.getFullYear());
    
    // Obtener el mes (0-11)
    console.log(fecha.getMonth());
    
    // Obtener el día del mes (1-31)
    console.log(fecha.getDate());

### Python

    import datetime
    
    fecha = datetime.datetime.now()
    
    # Obtener el año
    print(fecha.year)
    
    # Obtener el mes (1-12)
    print(fecha.month)
    
    # Obtener el día del mes (1-31)
    print(fecha.day)

## Importar módulos/librerías

### JavaScript

    // Importar un módulo
    const axios = require("axios");
    
    // Usar el módulo importado
    axios.get("https://api.example.com/data")
      .then(response => console.log(response.data))
      .catch(error => console.log(error));

### Python

    # Importar una librería
    import requests
    
    # Usar la librería importada
    response = requests.get("https://api.example.com/data")
    if response.status_code == 200:
      print(response.json())
    else:
      print(response.text)
## Manejo de archivos

### JavaScript

    const fs = require("fs");
    
    // Leer contenido de un archivo
    fs.readFile("archivo.txt", "utf8", (error, data) => {
      if (error) {
        console.log(error);
      } else {
        console.log(data);
      }
    });
    
    // Escribir contenido en un archivo
    fs.writeFile("archivo.txt", "Hola, mundo", (error) => {
      if (error) {
        console.log(error);
      } else {
        console.log("Archivo creado correctamente");
      }
    });

### Python

    # Leer contenido de un archivo
    try:
      with open("archivo.txt", "r") as archivo:
        contenido = archivo.read()
        print(contenido)
    except FileNotFoundError as error:
      print(error)
    
    # Escribir contenido en un archivo
    try:
      with open("archivo.txt", "w") as archivo:
        archivo.write("Hola, mundo")
        print("Archivo creado correctamente")
    except Exception as error:
      print(error)

## Expresiones regulares

### JavaScript

    const texto = "Hola, 123 mundo";
    const patron = /\d+/g;
    
    // Buscar coincidencias
    const coincidencias = texto.match(patron);
    console.log(coincidencias);
    
    // Reemplazar coincidencias
    const nuevoTexto = texto.replace(patron, "NUMERO");
    console.log(nuevoTexto);

### Python

    import re
    
    texto = "Hola, 123 mundo"
    patron = r"\d+"
    
    # Buscar coincidencias
    coincidencias = re.findall(patron, texto)
    print(coincidencias)
    
    # Reemplazar coincidencias
    nuevo_texto = re.sub(patron, "NUMERO", texto)
    print(nuevo_texto)

## Operaciones matemáticas básicas

### JavaScript

    const a = 5;
    const b = 2;
    
    console.log(a + b); // Suma
    console.log(a - b); // Resta
    console.log(a * b); // Multiplicación
    console.log(a / b); // División
    console.log(a % b); // Módulo
    console.log(a ** b); // Potencia

### Python

    a = 5
    b = 2
    
    print(a + b) # Suma
    print(a - b) # Resta
    print(a * b) # Multiplicación
    print(a / b) # División
    print(a % b) # Módulo
    print(a ** b) # Potencia

## Trabajando con JSON

### JavaScript

    // Convertir objeto a JSON
    const objeto = { nombre: "Juan", edad: 30 };
    const json = JSON.stringify(objeto);
    console.log(json);
    
    // Convertir JSON a objeto
    const jsonTexto = '{"nombre": "María", "edad": 25}';
    const objetoDeserializado = JSON.parse(jsonTexto);
    console.log(objetoDeserializado.nombre);

### Python

    import json
    
    # Convertir objeto a JSON
    objeto = {"nombre": "Juan", "edad": 30}
    json_texto = json.dumps(objeto)
    print(json_texto)
    
    # Convertir JSON a objeto
    json_texto = '{"nombre": "María", "edad": 25}'
    objeto_deserializado = json.loads(json_texto)
    print(objeto_deserializado["nombre"])

## Manejo de argumentos de línea de comandos

### JavaScript

    // Obtener argumentos de línea de comandos
    const argumentos = process.argv.slice(2);
    console.log(argumentos);
    
    // Ejemplo: node programa.js argumento1 argumento2

### Python

    import sys
    
    # Obtener argumentos de línea de comandos
    argumentos = sys.argv[1:]
    print(argumentos)
    
    # Ejemplo: python programa.py argumento1 argumento2

## Expresiones lambda/funciones anónimas

### JavaScript

    // Expresión lambda en función
    const sumar = (a, b) => a + b;
    console.log(sumar(2, 3));
    
    // Función de orden superior
    const operar = (a, b, operacion) => operacion(a, b);
    console.log(operar(5, 3, (a, b) => a * b));

### Python

    # Expresión lambda en función
    sumar = lambda a, b: a + b
    print(sumar(2, 3))
    
    # Función de orden superior
    def operar(a, b, operacion):
      return operacion(a, b)
    
    print(operar(5, 3, lambda a, b: a * b))

## Generadores

### JavaScript

    // Generador en JavaScript
    function* contador() {
      let i = 0;
      while (true) {
        yield i;
        i++;
      }
    }
    
    const miGenerador = contador();
    console.log(miGenerador.next().value);
    console.log(miGenerador.next().value);
    console.log(miGenerador.next().value);

### Python

    # Generador en Python
    def contador():
      i = 0
      while True:
        yield i
        i += 1
    
    mi_generador = contador()
    print(next(mi_generador))
    print(next(mi_generador))
    print(next(mi_generador))

## Uso de Set (conjuntos)

### JavaScript

    // Crear un conjunto
    const numeros = new Set();
    
    // Agregar elementos al conjunto
    numeros.add(1);
    numeros.add(2);
    numeros.add(3);
    
    // Verificar si un elemento está en el conjunto
    console.log(numeros.has(2)); // Devuelve true
    
    // Eliminar un elemento del conjunto
    numeros.delete(3);
    
    // Iterar sobre los elementos del conjunto
    for (const numero of numeros) {
      console.log(numero);
    }

### Python

    # Crear un conjunto
    numeros = set()
    
    # Agregar elementos al conjunto
    numeros.add(1)
    numeros.add(2)
    numeros.add(3)
    
    # Verificar si un elemento está en el conjunto
    print(2 in numeros) # Devuelve True
    
    # Eliminar un elemento del conjunto
    numeros.remove(3)
    
    # Iterar sobre los elementos del conjunto
    for numero in numeros:
      print(numero)

## Trabajando con módulos

### JavaScript

    // Exportar funciones y variables desde un módulo
    export const sumar = (a, b) => a + b;
    export const PI = 3.1416;
    
    // Importar funciones y variables en otro módulo
    import { sumar, PI } from "./modulo.js";
    console.log(sumar(2, 3));
    console.log(PI);

### Python

    # Definir funciones y variables en un módulo
    def sumar(a, b):
      return a + b
    
    PI = 3.1416
    
    # Importar funciones y variables desde un módulo
    from modulo import sumar, PI
    print(sumar(2, 3))
    print(PI)

## Expresiones condicionales compactas

### JavaScript

    // Expresión condicional compacta
    const edad = 18;
    const mensaje = edad >= 18 ? "Eres mayor de edad" : "Eres menor de edad";
    console.log(mensaje);

### Python

    # Expresión condicional compacta
    edad = 18
    mensaje = "Eres mayor de edad" if edad >= 18 else "Eres menor de edad"
    print(mensaje)

## Uso de bibliotecas populares

### JavaScript

    // Biblioteca para manipulación de fechas y horas
    const fechaActual = new Date();
    console.log(fechaActual.toISOString());
    
    // Biblioteca para realizar peticiones HTTP
    axios.get("https://api.example.com/data")
      .then(response => console.log(response.data))
      .catch(error => console.log(error));

### Python

    # Biblioteca para manipulación de fechas y horas
    from datetime import datetime
    fecha_actual = datetime.now()
    print(fecha_actual.isoformat())
    
    # Biblioteca para realizar peticiones HTTP
    import requests
    response = requests.get("https://api.example.com/data")
    if response.status_code == 200:
      print(response.json())
    else:
      print(response.text)
