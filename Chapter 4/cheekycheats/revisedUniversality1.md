##  Revised proof of *H* + *S* + *CNOT* + *T* Universality Part 1

In this part of the revision I will use much of the same techniques as in the text book to show that repeated rotations by an angle $`\theta`$ that is an irrational multiple of $`4\pi`$ may be used to approximate a rotation $`\alpha \in [0, 4\pi)`$ with error bounded by $`\delta`$. To do this we will define $`\theta_k = (k\theta) \mod{4\pi}`$. 

Why the emphasis on $`4\pi`$ rather than $`2\pi`$? Because we have $`R_{\hat{n}}(\alpha) = R_{\hat{n}}(\alpha \mod{4\pi})`$ while $`R_{\hat{n}}(\alpha) = R_{\hat{n}}(\alpha \mod {2\pi})`$ only up to a global phase. Normally, the existence of a global phase factor wouldn't concern us, but in the discussion of errors in unitary approximation, global phases have a real consequence. For example,
```math
\begin{align*}
E(R_{\hat{n}}(\alpha), R_{\hat{n}}(\alpha + 2\pi)) = E(R_{\hat{n}}(\alpha), -R_{\hat{n}}(\alpha)) = 2
\end{align*}
```

Now we move on to the revision. Choose integer $`N > 4\pi/\delta`$. The pigeonhole principle implies that if we select $`N`$ elements from the range $`[0, 4\pi)`$ such that no two elements are the same, then there exist two elements in the sequence whose difference is strictly less than $`\delta`$. Since $`\theta`$ is an irrational multiple of $`4 \pi`$, $`n\theta = m\theta \mod{4\pi}`$ is not satisfied for any integer pair $`n, m`$* and therefore the sequence $`\theta_k`$ for integer $`k\in [0, N)`$ is one example of the general sequence described earlier. It follows that two integers $`i`$ and $`j`$ exist where $`i > j`$ and $`|\theta_i - \theta_j| < \delta`$. Moreover, if $`\theta_i > \theta_j`$ then $`|\theta_i - \theta_j| =  \theta_i - \theta_j \mod{4\pi} = \theta_{(i-j)}`$ so $`\theta_{(i-j)} < \delta`$. If instead $`\theta_i < \theta_j`$, then $`\theta_{(i-j)} = 4\pi - |\theta_i - \theta_j|`$ and $`\theta_{(i-j)} > 4\pi - \delta`$. In either case, there is a positive integer $`i-j`$ such that $`\theta_{l(i-j)}`$ fills up the interval $`[0, 4\pi)`$ as $`l`$ is increased and adjacent elements are $`|\theta_i - \theta_j| < \delta`$ apart.

You may now wish to review the solution to exercise 4.40 posted [here](../4.5%20universal%20quantum%20gates/4.40.md) since it is the immediate next step in the proof of universality.
