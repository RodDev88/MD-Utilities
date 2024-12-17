# Conceptos básicos de arreglos en JavaScript

Un **arreglo** (o array) en JavaScript es una estructura de datos que permite almacenar una colección ordenada de elementos. Estos elementos pueden ser de cualquier tipo: números, cadenas, objetos, otros arreglos, etc.

## Conceptos básicos sobre arreglos

1. **Índices**:  
   Los elementos de un arreglo están ordenados y cada uno tiene un índice, que comienza desde `0`. Por ejemplo, el primer elemento tiene índice `0`, el segundo índice `1`, y así sucesivamente.

2. **Creación de un arreglo**:  
   Puedes crear un arreglo utilizando:

   - Corchetes `[]`.
   - La palabra clave `new Array()` (aunque esta última no se usa comúnmente).

3. **Métodos y propiedades**:  
   Los arreglos tienen métodos y propiedades que permiten manipularlos. Por ejemplo:
   - `.length`: Devuelve la cantidad de elementos en el arreglo.
   - `.push()`: Agrega un elemento al final del arreglo.
   - `.pop()`: Elimina el último elemento del arreglo.
   - `.shift()`: Elimina el primer elemento.
   - `.unshift()`: Agrega un elemento al inicio.
   - `.forEach()`, `.map()`, `.filter()`, etc., son métodos avanzados para recorrer o transformar arreglos.

## Ejemplo básico de un arreglo

```javascript
// Crear un arreglo con algunos elementos
const frutas = ["manzana", "banana", "cereza"];

// Acceder a elementos del arreglo
console.log(frutas[0]); // "manzana"
console.log(frutas[1]); // "banana"

// Modificar un elemento del arreglo
frutas[1] = "naranja";
console.log(frutas); // ["manzana", "naranja", "cereza"]

// Agregar un nuevo elemento
frutas.push("uva");
console.log(frutas); // ["manzana", "naranja", "cereza", "uva"]

// Eliminar el último elemento
frutas.pop();
console.log(frutas); // ["manzana", "naranja", "cereza"]

// Saber cuántos elementos tiene el arreglo
console.log(frutas.length); // 3
```

## ¿Qué es un ciclo `for`?

Un **ciclo `for`** en JavaScript es una estructura de control que permite repetir un bloque de código un número determinado de veces. Es muy útil para recorrer arreglos, realizar cálculos repetitivos o ejecutar cualquier tarea en la que se necesite iteración.

### Estructura básica de un ciclo `for`

```javascript
for (inicialización; condición; actualización) {
  // Bloque de código que se ejecuta en cada iteración
}
```

**_Inicialización:_** Se ejecuta una vez al inicio del ciclo. Generalmente, se utiliza para declarar e inicializar una variable de control (como i).

**_Condición:_** Se evalúa antes de cada iteración. Si es true, el bloque de código dentro del ciclo se ejecuta. Si es false, el ciclo termina.

**_Actualización:_** Se ejecuta al final de cada iteración y, normalmente, se utiliza para modificar la variable de control.

### Ejemplo ciclo `for`

```javascript
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
//salida en consola
1;
2;
3;
4;
5;
```

### Explicación del ejemplo

Inicialización: let i = 1
Se declara la variable i y se le asigna el valor inicial de 1.

Condición: i <= 5
El ciclo continuará ejecutándose mientras i sea menor o igual a 5.

Bloque de código: console.log(i)
En cada iteración, se imprime el valor actual de i.

Actualización: i++
Después de cada iteración, el valor de i aumenta en 1.

### Recorrer un arreglo con un ciclo `for`

Los ciclos for son especialmente útiles para trabajar con arreglos. Aquí tienes un ejemplo práctico:

```javascript
const colores = ["rojo", "verde", "azul", "amarillo"];

for (let i = 0; i < colores.length; i++) {
  console.log(`Color en posición ${i}: ${colores[i]}`);
}
//salida en consola
Color en posición 0: rojo
Color en posición 1: verde
Color en posición 2: azul
Color en posición 3: amarillo

```

### Explicación del ejemplo con arreglo

Inicialización: let i = 0
Comenzamos desde el primer índice del arreglo (0).

Condición: i < colores.length
El ciclo se ejecuta mientras i sea menor que la longitud del arreglo.

Bloque de código:
Se utiliza colores[i] para acceder al elemento actual del arreglo.

Actualización: i++
Incrementamos i en 1 después de cada iteración.

### Revisión de línea de código

```javascript
console.log(`Color en posición ${i}: ${colores[i]}`);
```

1.  Uso de Template Literals (Plantillas de cadena)
    En lugar de usar comillas simples ' ' o comillas dobles " ", se están usando backticks (acento grave: `). Esto se conoce como Template Literals en JavaScript.

        - Los Template Literals permiten:

            Incluir variables y expresiones dentro de una cadena usando ${}.

            Escribir cadenas de texto en varias líneas sin necesidad de concatenar.

---

2. La expresión ${i}

   - i es la variable de control del ciclo for que va cambiando en cada iteración.
   - Al colocar ${i} dentro del Template Literal, JavaScript reemplaza esa expresión con el valor actual de i.

     - Ejemplo:

     Si i = 0, entonces ${i} será reemplazado por 0.

---

3. La expresión ${colores[i]}

- Colores es un arreglo que contiene varios elementos, como "rojo", "verde", etc.
- colores[i] accede al elemento del arreglo en la posición i.
  Ejemplo:

        Si i = 0, entonces colores[i] será colores[0], que es "rojo".

        Si i = 1, entonces colores[i] será colores[1], que es "verde".

---

4. El resultado final

- Al combinar todo en el Template Literal, JavaScript reemplaza las expresiones ${i} y ${colores[i]} con sus respectivos valores.

- Por ejemplo, si el arreglo colores es:

```javascript
const colores = ["rojo", "verde", "azul", "amarillo"];
```

Durante cada iteración del ciclo for:

**_Primera iteración (i = 0):_**

```javascript
console.log(`Color en posición ${i}: ${colores[i]}`);
```

Color en posición 0: rojo;

**_Segunda iteración (i = 1):_**

Color en posición 1: verde;

y así sucesivamente...

**_El console.log combina texto fijo con valores dinámicos usando Template Literals.
La sintaxis ${} permite insertar variables o expresiones dentro de una cadena sin necesidad de concatenar manualmente._**

---

# Estructuras de control, iteración y variable de control en JavaScript

## 1. ¿Qué son las estructuras de control en JavaScript?

Las **estructuras de control** son bloques de código que permiten tomar decisiones o repetir acciones en función de ciertas condiciones. Se dividen principalmente en dos tipos:

### a) **Estructuras condicionales**

Permiten ejecutar un bloque de código solo si se cumple una condición.

- **`if`, `else if`, `else`**:

  ```javascript
  const edad = 18;

  if (edad >= 18) {
    console.log("Eres mayor de edad.");
  } else {
    console.log("Eres menor de edad.");
  }
  ```

- **`switch`** (para múltiples casos):

  ```javascript
  const dia = "lunes";

  switch (dia) {
    case "lunes":
      console.log("Inicio de semana.");
      break;
    case "viernes":
      console.log("Fin de semana cerca.");
      break;
    default:
      console.log("Día común.");
  }
  ```

---

### b) **Estructuras de bucle o repetición**

Permiten ejecutar un bloque de código varias veces (iteraciones).

- **`for`**: Itera un número específico de veces.

  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }
  ```

- **`while`**: Se ejecuta mientras la condición sea verdadera.

  ```javascript
  let i = 0;
  while (i < 5) {
    console.log(i);
    i++;
  }
  ```

- **`do...while`**: Ejecuta al menos una vez, luego verifica la condición.

  ```javascript
  let i = 0;
  do {
    console.log(i);
    i++;
  } while (i < 5);
  ```

- **`for...of`**: Recorre elementos de un arreglo o iterable.

  ```javascript
  const colores = ["rojo", "verde", "azul"];
  for (const color of colores) {
    console.log(color);
  }
  ```

- **`for...in`**: Recorre las propiedades de un objeto.
  ```javascript
  const persona = { nombre: "Ana", edad: 25 };
  for (const clave in persona) {
    console.log(`${clave}: ${persona[clave]}`);
  }
  ```

---

## 2. ¿Qué es una iteración?

Una **iteración** es cada **repetición** que ocurre dentro de un bucle. Es decir, cuando el bloque de código dentro de una estructura de repetición se ejecuta, decimos que ha ocurrido una iteración.

### Ejemplo de iteraciones con un ciclo `for`:

```javascript
for (let i = 1; i <= 3; i++) {
  console.log(`Iteración número: ${i}`);
}
//salida de consola

Iteración número: 1
Iteración número: 2
Iteración número: 3

```

Aquí el ciclo realiza 3 iteraciones, porque el bloque de código se ejecuta 3 veces.

---

## 3. ¿Qué es la variable de control en un ciclo for?

La variable de control es una variable que controla cuántas veces se ejecutará un ciclo. Generalmente se declara en la inicialización del ciclo for.

Ejemplo:

```javascript
Copiar código
for (let i = 0; i < 3; i++) {
    console.log(i);
}
```

### Desglose del ciclo:

let i = 0: Aquí se inicializa la variable de control i con el valor 0.

i < 3: Esta es la condición. Mientras i sea menor que 3, el ciclo se ejecutará.

i++: Esto actualiza la variable de control, incrementando su valor en 1 después de cada iteración.
