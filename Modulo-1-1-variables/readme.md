# Variables

* Para poder sacar por pantalla en contenido de una variable podemos usar la palabra clave `print`
print(a)

* En la función `print()` los paréntesis `()` especifican los datos sobre los que tiene que actuar la función.

## Tipos de variables

1. Los números enteros en inglés se denominan `integer` ('int'), y son todos los números sin decimales tanto positivos como negativos.

2. Los números decimales en inglés se denominan `float` ('float'), y son todos los números con decimales tanto positivos como negativos.

3. Las cadenas de caracteres se llaman `string` ('str') en inglés y pueden delimitarse con comillas simples ' ' o dobles " " indistintamente.

* Python nos permite cambiar el tipo de dato de `int` a `float` o viceversa. `int()` ,`float()`
* El cambiar el tipo de un dato se llama *type casting* o conversión de tipos. 
* `type()` comprueba el tipo de variable
* para comprobar si una variable tiene el tipo que esperabas, también puedes usar la función `isinstance()`, que requiere dos argumentos, que como siempre se separan con una coma: primero el nombre de la variable que quieres comprobar, y segundo el tipo. 
 ej.
```
print(isinstance(c5a,float))
```
* Tambien podemos usarlo con booleano. 
ej.
```
print(isinstance(d1,bool))
```
* El resultado sera true/false

## Operaciones algebraicas

1. la suma y la resta se hacen con `+` y `-`respectivamente.

2. La multiplicación y la división se hacen con `*` y `/` respectivamente.
3. En vez de usar la división normal `/`, también podemos usar la división entera `//` y el residuo `%`. Ojo que aunque sea el símbolo de porcentaje no lo es.
4. El operador `**` se usa para elevar un número a otro. ej. paquete_litros = (paquete_cm / 10) ** 3
5. Para redondear tenemos la función `round()`. Como argumento le damos la variable o el número que tiene que redondear. Opcionalmente puedes añadir un segundo argumento a esta función para decirle cuántos decimales te interesan. Si no añades nada más, ese segundo valor se queda por defecto en `0`. ej. perros = round (8/13, 2).


## Operaciones binarias

##### En la sección de tipos de datos introducimos las variables booleanas. Son útiles a la hora de querer evaluar sentencias, o comparar contenidos de variables.

* Para comprobar ina igualdad (si algo NO ES IGUAL que algo) utilizaremos `==`
* Podemos utilizar también `is`, pero hay que tener en cuenta que no es exactamente lo mismo por lo que en algunos casos no será equivalente puesto que significa específicamente algo ES algo.
* Usaremos `is not` justo en el sentido contrario (algo NO ES algo) y tambien podemos usar `!=` (algo ES NO ES IGUAL a algo )
* Usaremos `>` y `<` mayor que y menor que.
* Por último tenemos `>=` y `<=` mayor o igual y menor o igual.
##### Todas las evaluaciones que vimos se han evaluado a un `True` o un `False`.

Para comprobar si se cumplen múltiples criterios se puede usar las palabras `and` y `or`, que se traducen a las palabras *y* y *o* en castellano.

## La función input()

Para poder insertar tu propio nombre, y guardarlo en la variable `nombre`, usamos la función `input()`. Si trabajas en VS Code, al ejecutar la celda aquí abajo, abrirá un campo para escribir arriba en la ventana. No hace falta clicear en ello, simplemente escribe tu nombre y da a la tecla `Enter`. El programa espera en la línea que dice `input()` hasta que reciba el `Enter` para ejecutar el resto del código.
```
dia_cumple = input('¿qué día es tu cumpleaños?')
print(dia_cumple)
```
'Diciembre'

## Métodos de strings

##### Un `str` realmente es una cadena de caracteres. No importa si han sido definidos con comillas simples `''` o dobles `""`. La cadena se puede ampliar con más caracteres sueltos u otras cadenas predefinidas y guardadas en otra variable. Como ya sabemos, las cadenas se pueden visualizar con `print()`.

### `upper()`
Pone todas las letras en mayúscula.
```
print(variable.upper())
```

### `lower()`
Pone todas las letras de nuestro *string* en minúscula. 

```
print(variable.lower())
```

### `capitalize()`
Para poner la primera letra de la frase en mayúscula.
```
print(variable.capitalize())
```

### `title()`
Para poner la primera letra de cada palabra en mayúscula.
```
print(variable.title())
```

### `swapcase()`
Para convertir las mayúsculas en minúsculas y las minúsculas en mayúsculas.
```
print(variable.swapcase())
```

### `strip()`
Quita todos los espacios que haya al principio y al final del *string*
```
print(variabls.strip())
```

### `split()` 
El método split() divide un *string* en una lista.

(Podemos especificar el separador, el cuál por defecto es cualquier espacio en blanco.)
```
saludo_separado = saludo.split()
saludo_separado
```
['Buenos',
 'dias',
 'chicas,',
 'sigamos',
 'aprendiendo',
 'métodos',
 'de',
 'los',
 'strings']

Pero también podemos especificar un separador, en este caso, separaremos por las "d".
```
saludo_separado2 = saludo.split("d")
saludo_separado2
```
['Buenos ',
 'ias chicas, sigamos apren',
 'ien',
 'o méto',
 'os ',
 'e los strings']


### `replace()`
Sustituye una frase especificada por otra frase especificada.

ej.En este caso, queremos reemplazar la palabra "chicas" por "Adalabers". 
```
saludo_adalaber = saludo.replace("chicas", "Adalaber")
saludo_adalaber
```
'Buenos dias Adalaber, sigamos aprendiendo métodos de los strings'

### `join()` 
Toma todos los elementos de un iterable (una lista o una tupla) y los une en un *string*.

(Debemos especificar un *string* como separador)

```
lista_saludo = ["Hola", "que tal estas", "Adalaber"]
string_saludo1 =  " ".join(lista_saludo)
string_saludo1
```

'Hola que tal estas Adalaber'

```
string_saludo2 =  "_".join(lista_saludo)
string_saludo2
```
'Hola_que tal estas_Adalaber'

### `find()`
Encuentra la primera aparición del valor especificado. Este método va a devolver -1 si no se encuentra el valor. Si encuentra una coincidencia, nos devuelve el número de la posición donde se encuentra el *string* que estamos buscando. 

El método `find() `es prácticamente igual que el método `index()`, la única diferencia es que el método index() lanza una excepción si no se encuentra el valor.

Su sintaxis es: 

```
string.find(valor, inicio, final)
```
Donde: 

1. `valor`: hace referencia a el *string*  que queremos buscar.

2. `inicio`: hace referencia a la posición donde queremos empezar a buscar.

3. `final`: hace referencia a la posición donde queremos finalizar la búsqueda.

Ej.Vamos a querer buscar todas las "m" de nuestro saludo. Empezando por la letra que está en la posición 10, hasta la letra que esta en posición 30
```python
saludo.find("m", 10, 30)

(En nuestro saludo, hat una "m" en la posición 24.)