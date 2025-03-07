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



