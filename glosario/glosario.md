# GLOSARIO

Diferencia entre lenguaje interpretado y lenguaje compilado

    Un lenguaje interpretado ejecuta el código línea por línea a través de un intérprete en tiempo real, lo que permite una mayor flexibilidad pero generalmente hace que la ejecución sea más lenta. Un lenguaje compilado, en cambio, convierte el código completo en un archivo ejecutable mediante un compilador antes de su ejecución, lo que suele mejorar el rendimiento pero requiere recompilar cada vez que se hacen cambios.

    Ejemplo lenguaje interpretado: JS

        JavaScript es un ejemplo de un lenguaje interpretado, ya que su código se ejecuta en un entorno que lo interpreta, como el navegador o Node.js, donde es procesado línea por línea en tiempo de ejecución.

    Ejemplo lenguaje compilado: C++

        C++, por otro lado, es un lenguaje compilado. El código C++ debe ser compilado por un compilador (como GCC o Clang) antes de poder ejecutarse, lo que convierte el código fuente en un archivo binario ejecutable que la máquina puede correr directamente.

---

Lógica de negocios

    La lógica de negocios es el conjunto de reglas y procesos que definen cómo opera una aplicación o sistema para cumplir los objetivos específicos de una organización o negocio. Incluye la toma de decisiones, el procesamiento de datos y las operaciones que traducen los requisitos de negocio en funciones que la aplicación ejecuta, separando las reglas del negocio de otros aspectos técnicos de la aplicación.

---

Runtime JS:

    Un runtime de JavaScript es el entorno donde se ejecuta el código JavaScript. Este entorno contiene elementos clave como el motor de ejecución (por ejemplo, V8 en Chrome) y APIs que permiten al código interactuar con el sistema (por ejemplo, para acceder a la red o al sistema de archivos). Los runtimes, como Node.js para entornos de servidor, extienden las capacidades de JavaScript más allá del navegador.

---

Generado dinámicamente

    ¿Qué significa "generado dinámicamente"?
    Cuando se dice que algo es "generado dinámicamente", se refiere a que el contenido o los elementos de la página no están predefinidos en el HTML, sino que se crean o modifican en tiempo real a través de código JavaScript.

    Explicación sencilla:
    Generar dinámicamente significa que el contenido no está en el HTML desde el principio. En lugar de tener una lista fija de elementos, como:

```javascript
<ul>
  <li>Javiera</li>
  <li>Camila</li>
</ul>
```

    Se crea el contenido de la lista después de que la página ha cargado, a través de código. El script de JavaScript genera la lista en el momento en que se ejecuta el código, por ejemplo, al cargar la página o como resultado de una acción del usuario.

    En tu ejemplo:

```javascript
const data = ["Javiera", "Camila", "Francisco"];
for (let item of data) {
  d.innerHTML += `<li> ${item} </li>`;
}
```

    Aquí, los elementos <li> se agregan al <ul> después de que la página ha sido cargada. El contenido no estaba en el HTML original, sino que se creó dinámicamente a través de JavaScript.

    ¿Por qué es importante?
    Flexibilidad: Puedes cambiar o actualizar el contenido de la página sin tener que recargarla.
    Interactividad: El contenido puede adaptarse según las acciones del usuario (como hacer clic, enviar un formulario, etc.).

---
