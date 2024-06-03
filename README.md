# VBA_2
SQL to TXT, una función para generar listados en texto a partir de consultas o SQL

---

Se presenta aquí una función concebida para formatear el texto de salida de una SQL, a la que pasaremos el nombre de una tabla, consulta o directamente una sentencia SQL (una que devuelva un conjunto de registros) y otro parámetro denominado "Otros" en el que de una forma un poco críptica configuraremos varias propiedades de las columnas: visibilidad, anchura, alineación, formato y si se deben sumar totales.

--- 

La explicación extraida de los comentarios del código --
Devuelve un listado formateado de la SQL, con un título, las cabeceras de las columnas, sus valores y totales que se soliciten
el parámetro sOtros se utiliza como sigue: por ejemplo: "0110111,00101500301212,0230133,0510188,0000011
                                                         VVV....,AaAaAa........,LLL....,FFF....,TTT....
V: es un valor de un dígito 0/1 que indica si se imprime la columna correspondiente al la posicion , ej: 101, ...-> se imprimen las columnas 1ª y 3ª, la 2ª no.
Aa: valor de dos dígitos donde se indica la anchura de la columna correspondiente (hay que ocupar los de las columnas que no se  impriman, ej: 101,100018,... la 1ª columna tiene una anchura de 10 caracteres y la 3ª de 18
L: valor de un dígito que indica la alineación de los valores en la columna: 1= alin. izquierda, 2 = centrada, 3 = derecha
F: valor de un dígito que indica el formato de los datos: 1: sin formato, 2: Horas:Minutos., 3: €, 4: #.##0, 5: dd/mm/yy, 6: %,00 , 7: % , 8: #.##0,00
T: es un valor de un dígito 0/1 que indica si se calcula total de la columna correspondiente al la posicion EN LA PRIMERA COLUMNA NO SE CALCULA TOTAL
Si la SQL tiene más columnas que las indicadas en sOtros, las columnas restantes repiten los valores de parámetros de la última columna.

Se ofrecen 2 ejemplos de demostración y un 3º para probar tú mism@ modificando los parámetros de la función.
