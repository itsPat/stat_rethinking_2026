# Notes

Ways for *p* to produce the observation = $W,L = (4p)^W \times (4 - 4p)^L$

- We're using `4` here because it's a 4 sided globe.
- *W* is water
- *L* is land
- *p* is the proportion of water in the possibility space
    - e.g. if there's 1 water, 3 land, p is 0.25
    - e.g. if there's 3 water, 1 land, p is 0.75


The formula will depend on the generative model. For a 4 sided die, this formula works. This isn't necessarily true in all cases.

---

| Possibility | Obs 1 | Obs 2 | Obs 3 | Obs 4 | Obs 5 | Obs 6 | Obs 7 | Obs 8 | Obs 9 | Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `[○ ○ ○ ○]` | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | $0 = 0^6 \times 4^3$ |
| `[● ○ ○ ○]` | 1 | 3 | 3 | 3 | 3 | 9 | 9 | 27 | 27 | $27 = 1^6 \times 3^3$ |
| `[● ● ○ ○]` | 2 | 4 | 8 | 16 | 32 | 64 | 128 | 256 | 512 | $512 = 2^6 \times 2^3$ |
| `[● ● ● ○]` | 3 | 3 | 9 | 27 | 81 | 81 | 243 | 243 | 729 | $729 = 3^6 \times 1^3$ |
| `[● ● ● ●]` | 4 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | $0 = 4^6 \times 0^3$ |


You can calculate using the expression in the total column. However at every step (observation), to get the number of ways to arrive at that observation, you can simply take the number of ways to arrive at the previous observation and multiply it by the number of ways to arrive at the current observation.

---

# Probability

> Probability: Non-negative values that sum to one.

Suppose W=20, L=10, Then p=0.5 has

$2^W,2^L = 1,073,741,824$

ways to produce that sample.

To convert the "ways" into a probability, we divide the number of ways by the total number of ways.

![Alt Text](./slides/3.png)

In Bayesian inference, the distribution of probabilities is what we refer to as **Posterior Distribution**.

The distribution that gives you the relative possibilities of the different possibilities *after* updating on data. (Which is why we call it *posterior* distribution. There is a *prior* distribution as well, which is whatever the distribution was *before* you got new data)

---

![Alt Text](./slides/4.png)
![Alt Text](./slides/5.png)
![Alt Text](./slides/6.png)
![Alt Text](./slides/7.png)

The normalizing constant is just there to make sure everything sums up to 1. You can for the most part ignore it.

![Alt Text](./slides/8.png)
![Alt Text](./slides/9.png)
![Alt Text](./slides/10.png)
![Alt Text](./slides/11.png)
![Alt Text](./slides/12.png)
![Alt Text](./slides/13.png)
![Alt Text](./slides/14.png)

Notice how the distribution gets taller and more concentrated in an area because evidence is accumulating within that region.

![Alt Text](./slides/15.png)
![Alt Text](./slides/16.png)

![Alt Text](./slides/17.png)
![Alt Text](./slides/18.png)
![Alt Text](./slides/19.png)

Point estimates in bayesian statistics are not what we're after. The estimate *is* the distribution.

![Alt Text](./slides/20.png)

![Alt Text](./slides/21.png)

![Alt Text](./slides/22.png)

![Alt Text](./slides/23.png)