# README - Algoritmos en Wolfram Language (Mathematica)

Este repositorio contiene diversas implementaciones de algoritmos matemáticos en Wolfram Language (Mathematica). A continuación, se describen los archivos incluidos y su funcionalidad.

## Archivos y Descripción

### 1. PolinomioTaylor.nb
**Descripción:**
Este script calcula la aproximación de \( \cos(x) \) usando una serie de Taylor.

**Funcionamiento:**
- Solicita al usuario un valor de \( x \) en radianes.
- Pide el número de términos \( N \) para la aproximación.
- Calcula la aproximación mediante la serie de Taylor y la compara con el valor real.

**Fórmula utilizada:**
\[
\cos(x) \approx \sum_{n=0}^{N} \frac{(-1)^n x^{2n}}{(2n)!}
\]

---

### 2. Biseccion.nb
**Descripción:**
Implementa el método de bisección para encontrar una raíz de una función en un intervalo dado.

**Funcionamiento:**
- Solicita al usuario una función \( f(x) \), el intervalo \([a, b]\), una tolerancia y un número máximo de iteraciones.
- Verifica que \( f(a) \) y \( f(b) \) tengan signos opuestos.
- Aplica el método de bisección hasta encontrar una aproximación de la raíz.

---

### 3. esPrimo.nb
**Descripción:**
Determina si un número ingresado por el usuario es primo.

**Funcionamiento:**
- Verifica si el número es menor que 2 (caso no primo).
- Comprueba divisibilidad hasta \( \sqrt{n} \).
- Retorna si el número es primo o no.

---

### 4. Euclides.nb
**Descripción:**
Implementa el algoritmo de Euclides para calcular el Máximo Común Divisor (MCD) de dos números.

**Funcionamiento:**
- Solicita al usuario dos números enteros positivos.
- Aplica dos versiones del algoritmo:
  - **Recursiva:** \( MCD(a, b) = MCD(b, a \mod b) \) hasta que \( b = 0 \).
  - **Iterativa:** Usa un bucle para calcular el MCD.

---

### 5. Factorial.nb
**Descripción:**
Calcula el factorial de un número usando métodos recursivos e iterativos.

**Funcionamiento:**
- Solicita un número entero no negativo.
- Calcula el factorial de forma:
  - **Recursiva:** \( n! = n \times (n-1)! \) con caso base \( 0! = 1 \).
  - **Iterativa:** Usa un bucle acumulativo.

---

