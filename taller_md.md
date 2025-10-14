# Markdown



* *Documentación en GitHub*
* *Ecuaciones*
  * En Notebook de Python
* Viñeta 1
* Viñeta 2

---

# Documentar en lenguaje de programación


``` python
def suma(x1: int, x2: int):
    return x1 + x2
```


# Miscelánea

* Cambiar distribución de teclado  
  *Comando:* Windows + Espacio

---

# Redacción de ecuaciones en Markdown

Comando para previsualizar:  
*Ctrl + Shift + V*

---

# Ejemplo

Fórmula para calcular las raíces de la ecuación cuadrática:

$$
x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

---

# Ejercicio

Escribir la ecuación de *Navier–Stokes*:

$$
\rho \frac{D\vec{V}}{Dt} = -\nabla p + \mu \nabla^2 \vec{V} + \rho \vec{g}
$$

Y una sumatoria de ejemplo:

$$
\sum_{i=1}^{4} i^2 = 1^2 + 2^2 + 3^2 + 4^2
$$

📌 Recuerda subirlo al repositorio del taller.

---

# Taller

* Se debe presentar:
  * Notebook de Python
  * Enlace al repositorio en GitHub

---

## Ejercicio 1

Cual es el número minimo de elementos de la serie $1 + 1/2 + 1/4 + 1/8$ + ...para alcanzar un error absoluto $e_{abs}$ dentro de $10^{-1}$ ?

```python
suma = 0
i = 0
while (2-suma)>= 10**-1:
    suma+= (1/2)**i
    i+=1
print(i)
```

## Ejercicio 2 (Bubble sort)

### Corrida de escritorio
$v = [3, 2, 5, 8, 4, 1]$

| i | Vector |
| -- | -- |
| 0 | $ [3, 2, 5, 8, 4, 1] $ |
| 1 | $ [2, 3, 5, 8, 4, 1] $ |
| 2 | $ [2, 3, 5, 4, 8, 1] $ |
| 3 | $ [2, 3, 5, 4, 1, 8] $ |
| 4 | $ [2, 3, 4, 5, 1, 8] $ |
| 5 | $ [2, 3, 4, 1, 5, 8] $ |
| 6 | $ [2, 3, 1, 4, 5, 8] $ |
| 7 | $ [2, 1, 3, 4, 5, 8] $ |
| 8 | $ [1, 2, 3, 4, 5, 8] $ |
| 9 | $ [1, 2, 3, 4, 5, 8] $ |

Resultado final:

$v_{sorted} = [1,2,3,4,5,8]$

Caso de Prueba:
* $v_2=[-1,0,4,5,6,7]$
* $v_3$ 100_000 número aleatorios entre -200 y 145.
``` python
a = [3, 2, 5, 8, 4, 1]
print(a)
for i in range(len(a)):
    swapped = False
    for j in range(1, len(a) - i):
        if a[j] < a[j - 1]:
            a[j], a[j - 1] = a[j - 1], a[j]
            swapped = True
            print(a)
    if not swapped:
        break

print(a)
```

# Algoritmo 3



| n | fib(n) |
| -- | -- |
| 0 | 0 |
| 1 | 1 |
| 2 | 1 |
| 3 | 2 |
| 4 | 3 |
| 5 | 5 |
| 6 | 8 |
| 7 | 13 |
| ---|---| 
| $n = 11 $ | ? |
| $n = 84 $ | ? |
| $n = 1531 $ | ? |
---
## Graficar

* El valor de la serie $fib(n)$
* El valor del cociente

$\phi \rightarrow \frac{fib(n)} {fib(n-1)} \approx 1.618 $ número áureo


| n | $\phi \rightarrow \frac{fib(n)} {fib(n-1)}$ |
| -- | -- |
| 2 | $1/1=1$ |
| 3 | $2/1=2$ |
| 4 | $3/2=1.5$ |
| 5 | $5/3=1.66667$ |
| 6 | $8/5=1.6$ |
| 7 | $13/8=1.625$ |
| 8 | $21/13=1.615$ |
| $\infty $ | $ \frac{1 + \sqrt{5}} {2} \approx 1.618$ (número áureo) |

``` python
n= 11

if n == 0:
    print(0) 
else:
    x=0
    y=1
    for i in range (1, n-1):
        z = x+y
        x = y
        y = z
    print(y)
    print(y/x)
```