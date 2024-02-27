---

# Repositorio del Taller de Clase

Este repositorio contiene la solución al taller de clase, junto con algunas notas importantes sobre los problemas encontrados y las soluciones implementadas.

## Notas

- **Errores en los ejemplos:** Los ejemplos `Example1_1` y `Example1_4` tenían un error; se esperaba "int main" en lugar de solo "main".
- **Conteo de líneas en Example1_1:** Este ejemplo cuenta "/n" como un contador de líneas en el archivo, por lo que si solo hay una línea sin "/n", dice que no hay líneas en el archivo.
- **Problemas al unir Flex con Bison:** Se generaron varios errores al unir Flex con Bison debido a que el libro es antiguo para las versiones actuales de los programas. Las versiones actuales de Bison no suelen utilizar un main, y la página oficial recomienda seguir una estructura diferente.
- **Error en el código de Bison del ejemplo 5:** Existe un error a la hora de apuntar a la expresión para imprimirla.

## Detalles por Punto

### Punto 1
La calculadora tal como está actualmente (guiada por el libro) no acepta una línea solo con un código. El problema radica en una línea sin "exp", lo que causa un error de sintaxis. Para resolver esto, se agregó otra acción en esa regla para que, si hay una línea sin expresión, no haga nada, evitando así el error y permitiendo los comentarios y líneas vacías.

### Punto 2
Ya implementado en la calculadora.

### Punto 3
No hay problemas al volver a utilizar el símbolo "|", ya que la regla de implementación es diferente. Se cambió la estructura del absoluto para que se identificara la diferencia visualmente.

### Punto 4
La diferencia entre "SimpleFlexScanner" (Example 3) y "CalculatorScanner" (Example 4) radica en que el primero utiliza "+" como ADD, mientras que el segundo lo utiliza como "259", que sería el token. Ambos reconocen los mismos tokens pero con códigos de acción diferentes.

### Punto 5
Flex, aunque eficiente en la tokenización y el análisis de texto basado en expresiones regulares, no es ideal para el procesamiento del lenguaje natural (NLP) debido a las complejidades propias de idiomas como el español. Se recomienda evitar la ambigüedad y mantener jerarquías claras al utilizar Flex.

### Punto 6
![Comparacion de tiempo de ejecucion](https://github.com/AlgorithmicPaws/flex-bison/blob/main/ComparationResults.png)
---
