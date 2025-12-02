# Secuencia binaria y múltiplos de 3 en Fibonacci

En la tabla inicial se muestra la representación binaria de varios números de Fibonacci, con un énfasis en los que están marcados con `*`. Dichos números (2, 8, 34, 144, 610, 2584) corresponden a posiciones múltiplos de 3 dentro de la secuencia:

- F₃ = 2
- F₆ = 8
- F₉ = 34
- F₁₂ = 144
- F₁₅ = 610
- F₁₈ = 2584

## Tabla de representación binaria

| number |        binary | sequence |
| -----: | ------------: | :------: |
|      1 |             1 |          |
|      1 |             1 |          |
|      2 |            10 |    \*    |
|      3 |           011 |          |
|      5 |          0101 |          |
|      8 |          1000 |    \*    |
|     13 |         01101 |          |
|     21 |        010101 |          |
|     34 |       0100010 |    \*    |
|     55 |       0110111 |          |
|     89 |      01011001 |          |
|    144 |     010010000 |    \*    |
|    233 |     011101001 |          |
|    377 |    0101111001 |          |
|    610 |   01001100010 |    \*    |
|    987 |   01111011011 |          |
|   1597 |  011000111101 |          |
|   2584 | 0101000011000 |    \*    |

## Patrón repetitivo `1-1-0`

| number | binary |
| -----: | -----: |
|    110 |      6 |

- Al observar los **bits menos significativos** (LSB) en binario de los números de Fibonacci, aparece un patrón repetitivo `1-1-0`.
- Este ciclo se repite cada 3 términos de Fibonacci, lo cual coincide exactamente con que **cada tercer término es divisible por 2** y además múltiplo de 3 en la secuencia de índices.
- Ejemplo:
  - F₁ = 1 → termina en `1`
  - F₂ = 1 → termina en `1`
  - F₃ = 2 → termina en `0` → divisible por 2 → marcado

## Significado del número `110` (binario)

- El patrón `110` equivale a **6 en decimal**.
- El número 6 es clave porque es un múltiplo de 3.
- Las posiciones de Fibonacci múltiplos de 3 están asociadas con este patrón binario, de ahí la correspondencia con los números marcados.

## Propiedad general de divisibilidad en Fibonacci

Una propiedad conocida es que:

\[ F*m \,|\, F*{kn} \quad \text{para cualquier entero } k \]

Esto implica que si F₃ = 2, entonces todo término en la posición múltiplo de 3 (F₆, F₉, F₁₂, …) será divisible por 2. Esto explica el patrón binario finalizado en `0`.

## Conclusiones

1. **Ciclos binarios en Fibonacci**: los bits menos significativos de los números de Fibonacci siguen un ciclo de longitud 3 (`1-1-0`), revelando una periodicidad clara en la secuencia cuando se observa en base 2.
2. **Conexión con múltiplos de 3**: los términos en posiciones múltiplos de 3 (F₃, F₆, F₉, …) siempre terminan en `0` en binario y son divisibles por 2, lo que los distingue dentro de la secuencia.

3. **Significado del número 6**: el patrón `110` en binario (que equivale a 6) conecta la periodicidad en base 2 con la periodicidad en la posición de los múltiplos de 3 dentro de Fibonacci.

4. **Aplicaciones posibles**: este tipo de observación se relaciona con:
   - Criptografía (análisis de patrones en secuencias pseudoaleatorias).
   - Teoría de la computación (estudio de secuencias automáticas y periodicidad en distintas bases).
   - Matemática recreativa y exploración de propiedades modulares en Fibonacci.
