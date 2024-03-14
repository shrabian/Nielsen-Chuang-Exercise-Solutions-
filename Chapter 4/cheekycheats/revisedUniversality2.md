##  Revised proof of *H* + *S* + *CNOT* + *T* Universality Part 2

As per the construction provided in the textbook, we have rotation operators $`R_{\hat{n}}(\theta)`$ and $`R_{\hat{m}}(\theta)`$ where $`\hat{m}`$ and $`\hat{n}`$ are non-parallel and $`\theta`$ is an irrational multiple of $`\pi`$.

From our work in exercise [4.11](../4.2%20single%20qubit%20operations/4.11.md), we can write any single qubit unitary $`U`$ as a product of rotations about non-parallel axes:
```math
U=e^{i\alpha}R_{\hat{n}}(\beta_1)R_{\hat{m}}(\gamma_1)R_{\hat{n}}(\beta_2)R_{\hat{m}}(\gamma_2)... \tag{1}
```
where the number of rotations, $`c`$, is constant with respect to the unitary being decomposed. From the result of [4.40](../4.5%20universal%20quantum%20gates/4.40.md), each rotation operator in (1) can be approximated to an arbitrary precision of $`\frac{\epsilon}{c}`$ using repeated applications of $`R_{\hat{n}}(\theta)`$ and $`R_{\hat{m}}(\theta)`$. It follows from equation 4.63 in the text book that

```math
E(U, R_{\hat{n}}(\theta)^{n_1}R_{\hat{m}}(\theta)^{n_2}R_{\hat{n}}(\theta)^{n_3}...) < \epsilon
```

That is, we may approximate any single qubit unitary using repeated applications of the $`H`$ and $`T`$ gate.