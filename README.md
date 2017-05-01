CSE446 17SP HW3
===============

### 1. Perceptron (30 points)

First, get the Perceptron working with the kernel $k_p^1(u,v) = u \cdot v + 1$.

Implement the function `dot_kf`, and implement the methods for `Perceptron`.

Run Perceptron for a single pass over the validation set with this kernel, and plot the average loss as a function of the number of steps. Record the average loss every 100 steps, e.g. [100, 200, 300, ...].

Run the perceptron in the `if __name__ == '__main__':` block at the bottom of the code.

### 2. Polynomial kernel (30 points)

Implement the function `poly_kernel`.

For the set `d = [1,3,5,7,10,15,20]`, run Perceptron for a single pass over the validation set with `poly_kernel(d)`, and plot the average loss over the entire validation set as a function of `d`. What value of `d` produces the lowest loss?

### 3. Exponential kernel (30 points)

Implement the function `exp_kernel`.

For the `d` you chose in the previous step, run Perceptron with both `poly_kernel(d)` and `exp_kernel(10)` for a single pass over the testing set. For each of these two kernels, plot the average loss as a function of the number of steps. As above, report the average loss for every 100 steps.
