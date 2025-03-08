# Transformada de LaPlace 
## Es un cambio de espacio geométrico del dominio del tiempo hacia el dominio de la frecuencia compleja, son ecuaciones transformadas con derivadas algebráicas.
## 1. Forma integral 
$$x\left(t\right)\ \Longrightarrow \ x\ \left(s\right)$$ 
$$X\ \left(s\right)\ =\int _{0^{^{ }}}^{\infty _{ }}x\left(t\right)\ \cdot \ e^{-s\cdot t}$$
$$s\ =\ \alpha \ +\ jw$$
### 1.1. Propiedades 
* linealidad

$$LC_1 f\left(t\right) + C_2 g\left(t\right) = C_1 \left(f\left(t\right)\right) + C_2 \left(g\left(t\right)\right)$$

* Desplazamiento en t

$$g(t) = f(t - \tau) u(t - \tau), \text{ entonces } G(s) = e^{-s\tau} F(s), \quad \tau \geq 0$$

* Desplazamiento en s

$$g(t) = e^{-at} f(t), \text{ entonces } G(s) = F(s + a), \quad a \geq 0$$

* Escalado en t

$$g(t) = f(kt), \text{ entonces } G(s) = \frac{1}{k} F\left(\frac{s}{k}\right)$$

## 2. Transformada escalón unitario 
> 🔑 La función escalón unitario es como un interruptor donde los únicos valores que puede tomar es 0 y 1.

$$
1(t) =
\begin{cases}
    0, & \text{para } t < 0, \\
    1, & \text{para } t > 0
\end{cases}
$$


$$\mathcal{L} \{1(t)\} = \frac{1}{s}$$

![Escalon](https://github.com/user-attachments/assets/fa853db2-511a-489d-882b-f21a0bc9b165)

Figura 1. Escalón unitario
## 3. Transformada función rampa 
> 🔑 La función rampa es una función continua y diferenciable excepto en un punto, definida por una pendiente de 45 grados que crece linealmente.

### 3.1 Transformada de Laplace de una función escalón con rampa

### 3.2 Dada la función:

$$f(t) =
\begin{cases}
0, & t < 0 \\
At, & t \geq 0
\end{cases}$$

* Cálculo de la Transformada de Laplace

$$\mathcal{L} \{ At \} = \int_0^{\infty} At e^{-st} dt$$

* Resolviendo por integración por partes:

$$\mathcal{L} \{At\} = \int_0^{\infty} At e^{-st} dt = At \left( \frac{e^{-st}}{-s} \right) \Big|_0^\infty - \int_0^{\infty} \frac{A e^{-st}}{-s} dt$$

$$= \frac{A}{s} \int_0^{\infty} e^{-st} dt = \frac{A}{s^2}$$

![Rampa](https://github.com/user-attachments/assets/13e2acd6-6ad5-41f1-93f9-f2133e16dca7)

Figura 2. Fución rampa

# Transformada función senoidal

Las transformaciones de una función senoidal son cambios que se le aplican a la gráfica de la función en el plano cartesiano. Estas transformaciones pueden incluir desplazamientos, expansiones o compresiones.

$$f(t) =
\begin{cases}
0, & \text{para } t < 0 \\
A sen(\omega t), & \text{para } t \geq 0
\end{cases}$$

$$sen(\omega t) = \frac{1}{2j} \left( e^{j\omega t} - e^{-j\omega t} \right)$$

$$\mathcal{L} [ A sen(\omega t)] = \frac{A}{2j} \int_{0}^{\infty} \left( e^{j\omega t} - e^{-j\omega t} \right) e^{-st} dt$$

$$= \frac{A}{2j} \left( \frac{1}{s - j\omega} - \frac{1}{s + j\omega} \right)$$

$$= \frac{A \omega}{s^2 + \omega^2}$$

# Transformada de LaPlace

- **Transformada de una función:**

  $$\mathcal{L} ( f(t) ) = F(s)$$

- **Transformada de la derivada:**

  $$\mathcal{L} ( f'(t) ) = sF(s) - f(0)$$

  $$\mathcal{L} ( f''(t) ) = s^2 F(s) - s f(0) - f'(0)$$

  $$\mathcal{L} ( f^n(t) ) = s^n F(s) - s^{n-1} f(0) - \dots - s f^{n-1}(0) - f^n(0)$$

- **Transformada de la integral**

  $$\mathcal{L} \left( \int f(t) dt \right) = \frac{1}{s} F(s)$$

# Algunas demostraciones

$$F(s) = \int_{0}^{\infty} f(t) e^{-s t} dt$$

$$\mathcal{L} \{ f'(t) \} = \int_{0}^{\infty} f'(t) e^{-s t} dt$$

$$\mathcal{L} \{ f'(t) \} = uv \Big|_{0}^{\infty} - \int_{0}^{\infty} v \, du$$

$$\mathcal{L} \{ f'(t) \} = e^{-s t} f(t) \Big|_{0}^{\infty} - \int_{0}^{\infty} (-s e^{-s t} f(t)) dt$$

$$\mathcal{L} \{ f'(t) \} = -f(0) + s \int_{0}^{\infty} e^{-s t} f(t) dt$$

$$\mathcal{L} \{ f'(t) \} = -f(0) + sF(s)$$

---

**Definiciones usadas:**

$$u = e^{-s t}, \quad du = -s e^{-s t}$$  

$$v = f(t), \quad dv = f'(t)$$

# Definición de la Transformada Inversa de Laplace

En la Sección 8.1 definimos la transformación de Laplace de \( f \) por:

$$F(s) = \mathcal{L}(f) = \int_{0}^{\infty} e^{-s t} f(t) dt.$$

También diremos que \( f \) es una *transformación inversa de Laplace* de \( F \), y escribiremos:

$$f = \mathcal{L}^{-1} (F).$$

Para resolver ecuaciones diferenciales con la transformada de Laplace, debemos ser capaces de obtener \( f \) a partir de su transformación \( F \).
Hay una fórmula para hacer esto, pero **no podemos usarla directamente** porque requiere teoría de funciones de una variable compleja.  
Afortunadamente, podemos usar **la tabla de transformadas de Laplace** para encontrar transformaciones inversas necesarias.

---

## 💡 *Ejemplo 1:*  
Usa la tabla de transformadas de Laplace para encontrar:

### a.  
$$\mathcal{L}^{-1} \left( \frac{1}{s^2 - 1} \right)$$

### ✨ **Solución a** ✨  
Ajustamos \( b=1 \) en la transformación correspondiente:

$$\sinh(bt) \longleftrightarrow \frac{b}{s^2 - b^2}$$

Esto muestra que:

$$\mathcal{L}^{-1} \left( \frac{1}{s^2 - 1} \right) = \sinh t.$$

---

## 💡 *Ejemplo 2:*  
Usa la tabla de transformadas de Laplace para encontrar:

### b.  
$$\mathcal{L}^{-1} \left( \frac{s}{s^2 + 9} \right)$$

### ✨ **Solución b** ✨  
Ajustamos \( \omega=3 \) en la transformación correspondiente:

$$\cos(\omega t) \longleftrightarrow \frac{s}{s^2 + \omega^2}$$

Esto muestra que:

$$\mathcal{L}^{-1} \left( \frac{s}{s^2 + 9} \right) = \cos(3t).$$

# **Descomposición en fracciones parciales**

## 🔹 Caso 1: \( Q(s) \) tiene raíces reales distintas

Sea la función:

$$ G(s) = \frac{P(s)}{Q(s)} = \frac{P(s)}{(s + p_1)(s + p_2) \dots (s + p_n)} $$

---

## 🔹 **Forma de la descomposición en fracciones parciales**

La descomposición en fracciones parciales se expresa como:

$$ G(s) = \frac{A}{(s + p_1)} + \frac{B}{(s + p_2)} + \dots + \frac{N}{(s + p_n)} $$

---

## 🔹 **Coeficientes a determinar**
Donde \( A, B, \dots, N \) son coeficientes por determinar.

# **Descomposición en fracciones parciales**

## 🔹 **Ejercicio:**  
Obtenga la transformada inversa de:

$$ G(s) = \frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} $$

# **Descomposición en fracciones parciales**

## 🔹 Caso 2: \( Q(s) \) tiene \( n \) raíces reales repetidas  

Sea la función:

$$ G(s) = \frac{P(s)}{Q(s)} = \frac{P(s)}{(s + p)^n} $$

---

## 🔹 **Forma de la descomposición en fracciones parciales**

La descomposición en fracciones parciales se expresa como:

$$ G(s) = \frac{A}{(s + p)} + \frac{B}{(s + p)^2} + \dots + \frac{N}{(s + p)^n} $$

---

## 🔹 **Coeficientes a determinar**
Donde \( A, B, \dots, N \) son coeficientes por determinar.

# **Descomposición en fracciones parciales**

## 🔹 **Ejercicio:**  
Obtenga la transformada inversa de:

$$ G(s) = \frac{2s^2 + 6s + 5}{(s + 2)(s + 1)^2} $$

# **Descomposición en fracciones parciales**

## 🔹 Caso 3: \( Q(s) \) tiene raíces complejas conjugadas  

Sea la función:

$$ G(s) = \frac{P(s)}{Q(s)} = \frac{P(S)}{(s^2 + b_1 s + c_1)(s^2 + b_2 s + c_2) \dots (s^2 + b_n s + c_n)} $$

---

## 🔹 **Forma de la descomposición en fracciones parciales**

La descomposición en fracciones parciales se expresa como:

$$ G(s) = \frac{A s + B}{(s^2 + b_1 s + c_1)} + \frac{C s + D}{(s^2 + b_2 s + c_2)} + \dots + \frac{M s + N}{(s^2 + b_n s + c_n)} $$

---

## 🔹 **Coeficientes a determinar**
Donde \( A, B, \dots, N \) son coeficientes por determinar.

# **Descomposición en fracciones parciales**

## 🔹 **Ejercicio:**  
Obtenga la transformada inversa de:

$$ G(s) = \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} $$















