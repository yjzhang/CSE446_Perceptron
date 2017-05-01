CSE446 17SP HW3
===============

### 1. Perceptron (30 points)

First, get the Perceptron working with the kernel $k_p^1(u,v) = u \cdot v + 1$.

Implement the function `dot_kf`, and implement the methods for `Perceptron`.

Run Perceptron for a single pass over the validation set with this kernel, and plot the average loss $\bar{L}$ as a function of the number of steps $T$, where

$$\bar{L} = \frac{1}{T}\sum_{j=1}^T\mathbbm{1}(\hat y^{(t)} \neq y^{(t)})$$

 where $\hat{y}^t$ is the label that Perceptron predicts for datapoint $t$ as it runs, and $\mathbbm{1}$ is an indicator function, which is 1 if its condition is true and 0 otherwise. Record the average loss every 100 steps, e.g. [100, 200, 300, ...].

Run the perceptron in the `if __name__ == '__main__'` block at the bottom of the code.

### 2. Polynomial kernel (30 points)

For a positive integer $d$, the polynomial kernel $k_p^d(u,v) = (u \cdot v + 1)^d$ maps $X$ into a feature space of all polynomials of degree up to $d$.

Implement the function `poly_kernel`.

For the set $d = [1,3,5,7,10,15,20]$, run Perceptron for a single pass over the validation set with $k_p^d$, and plot the average loss over the validation set $\bar{L}(1000)$ as a function of $d$. What value of $d$ produces the lowest loss?

### 3. Exponential kernel (30 points)

For $\sigma > 0$, the Exponential kernel $k_E^\sigma(u,v) = e^{-\frac{\|u-v\|}{2\sigma^2}}$ is a map to all polynomials of $x$, where $\sigma$ is a tuning constant that roughly corresponds to the "window size" of the exponential. Tuning on the validation set has produced a value of $\sigma = 10$.

Implement the function `exp_kernel`.

For the $d$ you chose in the previous step, run Perceptron with both $k_p^d$ and $k_E^{10}$ for a single pass over the testing set. For each of these two kernels, plot the average loss $\bar{L}(T)$ as a function of the number of steps. As above, report the average loss for every 100 steps.
