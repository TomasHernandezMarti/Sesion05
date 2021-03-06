# Introducción a la programación para el Diseño de interacción

### Bootstrap v5 + p5.js

- - - - - - - - 

#### Lectura

Existen [muchas bibliotecas de JavaScript](https://en.wikipedia.org/wiki/List_of_JavaScript_libraries), además de [p5.js](https://p5js.org/es/). 

Antes de explorar otras, nos conviene tener completa claridad respecto de los tipos de datos que se usan en JavaScript "a secas", porque esa es la base sobre la que operan todas las bibliotecas.

Para comenzar a clarificar las cosas, partamos con el número 18261884. 

Si nos entregan tal número, sin contexto alguno, resultaría inútil. Pero es distinto de la siguiente manera: 

| País      |  Población       | Superficie     |
|:----------|:-----------------|:---------------|
| Chile     | 18261884         | 756102         |

Entendiendo cómo funciona una tabla, contamos con una clara orientación para la utilización de tal número como información sobre algo concreto: La población en Chile. 

Además del dato de la población de Chile, contamos con su superficie. Si dividimos el primer dato numérico por el segundo, obtenemos la densidad de la población en Chile. El resultado de aquella división es 24,15267252.

Los números 18261884 y 24,15267252 tienen una diferencia que corresponde apuntar:

- **18261884** es un número entero, un `int` (del inglés *integer*).

- **24,15267252** es un número de coma flotante, un `float` (del inglés *floating point number*; y no se olviden de esta diferencia, lo que para nosotros es coma, *for them* es punto, y el *coding* se hace en *english*).

A estos dos tipos de datos, podemos agregar: 

- **true** o **false** como las dos opciones posibles de un [tipo de dato lógico](https://es.wikipedia.org/wiki/Tipo_de_dato_l%C3%B3gico) (bool: *boolean*)

- **"A"** como un carácter (char: *character*)

Notemos que en el tipo de dato numérico y booleano no se usan comillas, pero en el caso del caracter sí. 

Mencionamos `int`, `float`, `bool` y `char` porque son palabras que en lenguajes de programación más clásicos se reservan para **declarar que tal variable almacenará tal tipo de dato**. 

**En JavaScript podemos crear toda variables con una única palabra reservada,`var`**. También podemos usar `let` y `const`. Para entender la diferencia, nos conviene consultar el artículo [Var, let y const. ¿Donde, cuando y por qué?](https://medium.com/@tatymolys/var-let-y-const-donde-cuando-y-por-qu%C3%A9-d4a0ee66883b).

Usando únicamente `var`, en JavaScript podemos asignar como contenido de la variable todas las siguientes alternativas:

```
var a = 18261884;
var b = 24.15267252;
var c = true;
var d = "Lisa the Vegetarian";
var e = ["Marge Simpson", "Homer Simpson", "Bart Simpson", "Lisa Simpson", "Maggie Simpson"];
var f = {
    mom: "Luann Van Houten",
    dad: "Kirk Van Houten",
    child: "Milhouse Van Houten"
};
var g = {
    mom: "Marge Simpson",
    dad: "Homer Simpson",
    children: ["Bart Simpson", "Lisa Simpson", "Maggie Simpson"]
};
var h = [
    {
        mom: "Luann",
        dad: "Kirk",
        children: ["Milhouse"]
    },
    {
        mom: "Marge",
        dad: "Homer",
        children: ["Bart", "Lisa", "Maggie"]
    },
    {
        mom: "Manjula",
        dad: "Apu",
        children: ["Poonam", "Sashi", "Pria", "Uma", "Anoop", "Sandeep", "Nabendu", "Gheet"]
    }
];

```

**Lo que cambia viene después del signo igual `=`, que en este caso está asignando contenido a cada variable.** 

Las variables `a`, `b` y `c` no requieren comillas. La variable `d`, que contiene una cadena de caracteres (*string*) sí usa comillas. 

La variable `e`, que contiene un arreglo, usa paréntesis cuadrado y cada elemento, por tratarse de un *string*, usa comillas (si fuesen números o booleanos no las usarían). 

La variable `f`, que contiene un objeto, usa paréntesis de llave que en su interior contiene pares de `nombre:valor`. 

Las variables `g` y `h` son mezclas de las anteriores.

Si necesitamos el valor de las variables `a`, `b`, `c` o `d`, basta con pedirlo directamente. Pero el caso es distinto si necesitamos un valor específico dentro de las variables  `e`, `f`, `g` o `h`.

Para comprender de mejor manera lo recién expuesto, sigamos aprovechando el [p5.js Web Editor](https://editor.p5js.org/profesorfaco/sketches/55-yg0wx0) y partir por la variable `e`: 

Digamos que necesitamos a `Marge Simpson`. Para solicitarla tenemos que escribir `e[0]`, porque se encuentra en la primera posición del arreglo asignado como valor a la variable `e`. Si escribimos `e[1]` el resultado sería `Homer Simpson`. Corresponde **recordar que la primera posición es cero, no uno**.

Pasemos a la variable `f`: 

Si necesitamos escribir la frase `Fue Kirk Van Houten quien intentó dibujar la dignidad`, tendríamos que escribir `'Fue ' + f.dad + ' quien intentó dibujar la dignidad'`.

Vamos por la variable `g`: 

Si necesitamos escribir la frase `El chupete de Maggie Simpson`, tendríamos que escribir `'El chupete de ' + g.children[2]`.

Llegando a la variable `h` convendría aprovechar a los octillizos Nahasapeemapetilon para explorar:

- el [método `sort()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/sort);

- el [método `forEach()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/forEach); y

- el [método `includes()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/includes).

- - - - - - -

#### Práctica

https://profesorfaco.github.io/interaccion/sesion_05/

- - - - - - - 

[← CLASE ANTERIOR](https://github.com/profesorfaco/interaccion/tree/main/sesion_04) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/interaccion/tree/main/sesion_06)
