# README - Algoritmos en Wolfram Language (Mathematica)

### 1. PolinomioTaylor.nb
**Descripción:**
Este script calcula la aproximación de \( \cos(x) \) usando una serie de Taylor.

**Funcionamiento:**
- Solicita al usuario un valor de `x` en radianes.
- Pide el número de términos `N` para la aproximación.
- Calcula la aproximación mediante la serie de Taylor y la compara con el valor real.

Código en acción:
```mathematica
PolinomioTaylorCos[x_, N_] := Sum[(-1)^n * x^(2 n) / Factorial[2 n], {n, 0, N}]
```

---

### 2. Biseccion.nb
**Descripción:**
Implementa el método de bisección para encontrar una raíz de una función en un intervalo dado.

**Funcionamiento:**
- Solicita al usuario una función `f(x)`, el intervalo `[a, b]`, una tolerancia y un número máximo de iteraciones.
- Verifica que `f(a)` y `f(b)` tengan signos opuestos.
- Aplica el método de bisección hasta encontrar una aproximación de la raíz.

Código en acción:
```mathematica
Biseccion[f_, a_, b_, tol_: 10^-6, maxIter_: 100] := Module[
  {c, iter = 0},
  While[(b - a) > tol && iter < maxIter,
    c = (a + b)/2;
    If[Abs[f[c]] < tol, Return[c]];
    If[f[a] * f[c] < 0, b = c, a = c];
    iter++;
  ];
  Return[c]
]
```

---

### 3. esPrimo.nb
**Descripción:**
Determina si un número ingresado por el usuario es primo.

**Funcionamiento:**
- Verifica si el número es menor que 2 (caso no primo).
- Comprueba divisibilidad hasta la raíz cuadrada del número.
- Retorna si el número es primo o no.

Código en acción:
```mathematica
EsPrimo[n_] := Module[{i},
  If[n < 2, Return[False]];
  For[i = 2, i <= Sqrt[n], i++, 
    If[Mod[n, i] == 0, Return[False]]
  ];
  Return[True];
]
```

---

### 4. Euclides.nb
**Descripción:**
Implementa el algoritmo de Euclides para calcular el Máximo Común Divisor (MCD) de dos números.

**Funcionamiento:**
- Solicita al usuario dos números enteros positivos.
- Aplica dos versiones del algoritmo:
  - **Recursiva:** Utiliza llamadas recursivas hasta que `b` sea cero.
  - **Iterativa:** Usa un bucle para calcular el MCD.

Código en acción:
```mathematica
MCDRecursivo[a_, b_] := If[b == 0, a, MCDRecursivo[b, Mod[a, b]]]
```

---

### 5. Factorial.nb
**Descripción:**
Calcula el factorial de un número usando métodos recursivos e iterativos.

**Funcionamiento:**
- Solicita un número entero no negativo.
- Calcula el factorial de forma:
  - **Recursiva:** Llama a sí misma hasta llegar al caso base.
  - **Iterativa:** Usa un bucle acumulativo.

Código en acción:
```mathematica
FactorialRecursive[n_] := If[n == 0, 1, n * FactorialRecursive[n - 1]]
```

---
