# Bucles en JS

En JS tenemos varias formas de realizar bucles.

Los bucles se utilizan para hacer algo de manera repetida.

Las sentencias disponibles en JS son las siguientes:

> sentencia for
> sentencia do...while
> sentencia while
> sentencia label
> sentencia break
> sentencia continue
> sentencia for...in
> sentencia for...of


# For

En el caso del bucle ```for```, este sepite hasta que la condición sea falsa.

> for ([expresionInicial]; [condicion]; [expresionIncremento])
>  sentencia

¿Cómo funciona?

La expresión de inicialización 'expresionInicial', si existe, se ejecuta. 
* Esta expresión habitualmente inicializa uno o mas contadores del bucle, pero la sintaxis permite una expresión con cualquier grado de complejidad. Esta expresión puede también declarar variables.
* Se evalúa la expresión condicion. Si el valor de condicion es true, se ejecuta la sentencia del bucle. Si el valor de condicion es false, el bucle for finaliza. Si la expresión condicion es omitida, la condición es asumida como verdadera.
* Se ejecuta la sentencia. Para ejecutar múltiples sentencias, use un bloque de sentencias ({ ... }) para agruparlas.
* Se ejecuta la expresión expresionIncremento, si hay una, y el control vuelve al paso 2.

Un ejemplo:

```
for(var i = 0; var < 10; i++) {
    alert('Esto es un bucle')
}
```

Un ejemplo más avanzado sacado de https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Bucles_e_iteración :

```
<form name="selectForm">
  <p>
    <label for="musicTypes">Choose some music types, then click the button below:</label>
    <select id="musicTypes" name="musicTypes" multiple="multiple">
      <option selected="selected">R&B</option>
      <option>Jazz</option>
      <option>Blues</option>
      <option>New Age</option>
      <option>Classical</option>
      <option>Opera</option>
    </select>
  </p>
  <p><input id="btn" type="button" value="How many are selected?" /></p>
</form>

<script>
function howMany(selectObject) {
  var numberSelected = 0;
  for (var i = 0; i < selectObject.options.length; i++) {
    if (selectObject.options[i].selected) {
      numberSelected++;
    }
  }
  return numberSelected;
}

var btn = document.getElementById("btn");
btn.addEventListener("click", function(){
  alert('Number of options selected: ' + howMany(document.selectForm.musicTypes))
});
</script>
```

Explicación del código:

La siguiente función contiene una sentencia for que cuenta el número de opciones seleccionadas en una lista (un elemento <select> que permite selección múltiple). La sentencia for declara la variable i y la inicializa a cero. Comprueba que i es menor que el número de opciones en el elemento <select>, ejecuta la sentencia siguiente if, e incrementa i en uno tras cada paso por el bucle.

# do while

La sentencia do...while se repite hasta que una condición especificada se evalúa a false. Una sentencia do...while se mostrará como sigue:

```
do
  sentencia
while (condicion);
```
Ejemplo de código:

```
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

En el siguiente ejemplo, el bucle do itera al menos una vez y vuelve a hacerlo mientras i sea menor que 5.

# while

Una sentencia while ejecuta sus sentencias mientras la condición sea evaluada como verdadera. Una sentencia while tiene el siguiente aspecto:

```
while (condicion)
  sentencia
```

Si la condición cambia a falsa, la sentencia dentro del bucle deja de ejecutarse y el control pasa a la sentencia inmediatamente después del bucle.

La condición se evalúa antes de que la sentencia contenida en el bucle sea ejecutada. Si la condición devuelve verdadero, la sentencia se ejecuta y la condición se comprueba de nuevo. Si la condición es evaluada como falsa, se detiene la ejecución y el control pasa a la sentencia siguiente al while.

Un ejemplo de código:
```
n = 0;
x = 0;
while (n < 3) {
  n++;
  x += n;
}
```
Con cada iteración, el bucle incrementa n y añade ese valor a x. Por consiguiente, x y n toman los siguientes valores:

Después del primer paso: n = 1 y x = 1
Después del segundo paso: n = 2 y x = 3
Después del tercer paso: n = 3 y x = 6
Tras completar el tercer paso, la condición n < 3 ya no es verdadera, por tanto el bucle termina.

Ejemplos sacados de la web de Mozilla https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Bucles_e_iteración


