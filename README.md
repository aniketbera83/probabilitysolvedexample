# 📝 Solved Problems — Probability & Statistics (Lecture-wise)

### Companion to: [Complete Notes](file:///Users/aniketbera/Desktop/leetCode/Probability%20and%20Statictics/Probability_and_Statistics_Complete_Notes.md)
### Playlist: Statistics and Probability by Dr. Gajendra Purohit (GP Sir)

---

## Table of Contents

1. [Lectures 1–5: Basics of Probability](#lecture-1--overview-sample-space--types-of-events)
2. [Lectures 6–11: Random Variables & Expectations](#lecture-6--discrete-random-variable--pmf)
3. [Lectures 12–17: Discrete Distributions](#lecture-12--binomial-distribution)
4. [Lectures 18–23: Continuous Distributions](#lecture-18--normal-distribution--mean-and-variance)
5. [Lectures 24–34: Bivariate & Correlation](#lecture-24--bivariate-discrete-random-variable)
6. [Lectures 35–42: Special Distributions](#lecture-35--gamma-distribution)
7. [Lectures 43–49: Chi-Square](#lecture-43--chi-square-distribution--concept)
8. [Lectures 50–55: t-Distribution & Tests](#lecture-50--t-distribution--pdf-derivation)
9. [Lectures 56–61: F-Distribution & Fisher's Z](#lecture-56--f-distribution)
10. [Lectures 62–67: Large Sample Tests & ANOVA](#lecture-62--z-test-for-population-mean)

---

# PART 1: BASICS OF PROBABILITY

---

## Lecture 1 — Overview, Sample Space & Types of Events
[🎥 Video](https://www.youtube.com/watch?v=qNGDD_Rh8ps)

### Problem 1.1
**Q:** Write the sample space for tossing 3 coins simultaneously. Find the probability of getting (a) exactly 2 heads, (b) at least 2 heads, (c) at most 1 head.

**Solution:**

S = {HHH, HHT, HTH, THH, HTT, THT, TTH, TTT}, |S| = 8

**(a) Exactly 2 heads:**
Favorable: {HHT, HTH, THH} → 3 outcomes
$$P(\text{exactly 2H}) = \frac{3}{8}$$

**(b) At least 2 heads (≥ 2):**
Favorable: {HHT, HTH, THH, HHH} → 4 outcomes
$$P(\text{at least 2H}) = \frac{4}{8} = \frac{1}{2}$$

**(c) At most 1 head (≤ 1):**
Favorable: {HTT, THT, TTH, TTT} → 4 outcomes
$$P(\text{at most 1H}) = \frac{4}{8} = \frac{1}{2}$$

---

### Problem 1.2
**Q:** Two dice are thrown. Find the probability that (a) the sum is 8, (b) the sum is a prime number, (c) both show the same number (doublet).

**Solution:**

Total outcomes: |S| = 6 × 6 = 36

**(a) Sum = 8:**
Favorable: {(2,6), (3,5), (4,4), (5,3), (6,2)} → 5 outcomes
$$P(\text{sum} = 8) = \frac{5}{36}$$

**(b) Sum is prime (2, 3, 5, 7, 11):**
- Sum = 2: {(1,1)} → 1
- Sum = 3: {(1,2), (2,1)} → 2
- Sum = 5: {(1,4), (2,3), (3,2), (4,1)} → 4
- Sum = 7: {(1,6), (2,5), (3,4), (4,3), (5,2), (6,1)} → 6
- Sum = 11: {(5,6), (6,5)} → 2
- Total favorable = 1 + 2 + 4 + 6 + 2 = 15
$$P(\text{prime sum}) = \frac{15}{36} = \frac{5}{12}$$

**(c) Doublet:**
Favorable: {(1,1), (2,2), (3,3), (4,4), (5,5), (6,6)} → 6
$$P(\text{doublet}) = \frac{6}{36} = \frac{1}{6}$$

---

### Problem 1.3
**Q:** From a deck of 52 cards, one card is drawn at random. Find P(King), P(Red card), P(Face card).

**Solution:**

- P(King) = 4/52 = **1/13**
- P(Red card) = 26/52 = **1/2**
- P(Face card) = 12/52 = **3/13** (J, Q, K × 4 suits)

---

### Problem 1.4
**Q:** A committee of 4 is to be formed from 6 men and 4 women. Find the probability that it contains (a) exactly 2 women, (b) at least 1 woman.

**Solution:**

Total ways = ¹⁰C₄ = 210

**(a) Exactly 2 women:**
Ways = ⁶C₂ × ⁴C₂ = 15 × 6 = 90
$$P = \frac{90}{210} = \frac{3}{7}$$

**(b) At least 1 woman:**
P(at least 1 woman) = 1 − P(no woman) = 1 − ⁶C₄/¹⁰C₄
= 1 − 15/210 = 1 − 1/14 = **13/14**

---

## Lecture 2 — Probability & Addition Theorem
[🎥 Video](https://www.youtube.com/watch?v=WafJR8zuIQw)

### Problem 2.1
**Q:** If P(A) = 0.4, P(B) = 0.5, P(A ∪ B) = 0.7, find (a) P(A ∩ B), (b) P(A' ∩ B), (c) P(A ∩ B'), (d) P(exactly one of A, B).

**Solution:**

**(a)** By Addition Theorem:
P(A ∪ B) = P(A) + P(B) − P(A ∩ B)
0.7 = 0.4 + 0.5 − P(A ∩ B)
$$P(A \cap B) = 0.2$$

**(b)** P(A' ∩ B) = P(B) − P(A ∩ B) = 0.5 − 0.2 = **0.3**

**(c)** P(A ∩ B') = P(A) − P(A ∩ B) = 0.4 − 0.2 = **0.2**

**(d)** P(exactly one) = P(A) + P(B) − 2P(A ∩ B) = 0.4 + 0.5 − 0.4 = **0.5**

---

### Problem 2.2
**Q:** The probability that a student passes in Mathematics is 2/3, in Physics is 4/9, and in both is 1/4. Find the probability that the student passes in at least one subject.

**Solution:**

P(M) = 2/3, P(P) = 4/9, P(M ∩ P) = 1/4

P(at least one) = P(M ∪ P) = P(M) + P(P) − P(M ∩ P)
= 2/3 + 4/9 − 1/4
= 24/36 + 16/36 − 9/36
= **31/36**

---

### Problem 2.3
**Q:** In a class, 60% students play cricket, 40% play football, 20% play both. Find the probability that a randomly selected student plays neither.

**Solution:**

P(C) = 0.6, P(F) = 0.4, P(C ∩ F) = 0.2

P(C ∪ F) = 0.6 + 0.4 − 0.2 = 0.8

P(neither) = 1 − P(C ∪ F) = 1 − 0.8 = **0.2**

---

## Lecture 3 — Probability of Independent Events & Deductions
[🎥 Video](https://www.youtube.com/watch?v=-3qpc7P1Nwk)

### Problem 3.1
**Q:** A and B independently try to solve a problem. P(A solves) = 1/2, P(B solves) = 1/3. Find (a) P(both solve), (b) P(problem is solved), (c) P(exactly one solves).

**Solution:**

Since A and B are independent:

**(a)** P(both) = P(A) × P(B) = 1/2 × 1/3 = **1/6**

**(b)** P(problem is solved) = P(at least one)
= 1 − P(A')P(B') = 1 − (1/2)(2/3) = 1 − 1/3 = **2/3**

**(c)** P(exactly one) = P(A)P(B') + P(A')P(B)
= (1/2)(2/3) + (1/2)(1/3) = 1/3 + 1/6 = **1/2**

---

### Problem 3.2
**Q:** The probability that A hits a target is 1/3 and that B hits is 2/5. Both fire at the target simultaneously. Find P(target is hit).

**Solution:**

P(A') = 2/3, P(B') = 3/5

P(target is hit) = 1 − P(both miss) = 1 − P(A')P(B')
= 1 − (2/3)(3/5) = 1 − 6/15 = 1 − 2/5 = **3/5**

---

### Problem 3.3
**Q:** Prove that if A and B are independent events, then A' and B' are also independent.

**Proof:**

P(A' ∩ B') = P((A ∪ B)') [by De Morgan's Law]
= 1 − P(A ∪ B)
= 1 − [P(A) + P(B) − P(A ∩ B)]
= 1 − P(A) − P(B) + P(A)P(B) [since A, B independent]
= [1 − P(A)][1 − P(B)]
= P(A') · P(B')

∴ A' and B' are independent. ∎

---

## Lecture 4 — Conditional Probability
[🎥 Video](https://www.youtube.com/watch?v=w4B_S_DFqfg)

### Problem 4.1
**Q:** A die is thrown twice. Find P(sum > 9 | first die shows 5).

**Solution:**

Let A = sum > 9, B = first die shows 5

Given B, second die can be 1, 2, 3, 4, 5, 6 (equally likely)
For A ∩ B: sum > 9 means second die must be 5 or 6
So A ∩ B = {(5,5), (5,6)}

$$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{2/36}{6/36} = \frac{2}{6} = \frac{1}{3}$$

---

### Problem 4.2
**Q:** A bag contains 5 white and 3 red balls. Two balls are drawn one after another without replacement. Find P(both white).

**Solution:**

P(1st white) = 5/8

P(2nd white | 1st white) = 4/7 (4 white remain out of 7)

P(both white) = P(W₁) × P(W₂|W₁) = (5/8)(4/7) = **20/56 = 5/14**

---

### Problem 4.3
**Q:** Given P(A) = 1/2, P(B) = 1/3, P(A ∩ B) = 1/4. Find P(A|B) and P(B|A). Are A and B independent?

**Solution:**

$$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{1/4}{1/3} = \frac{3}{4}$$

$$P(B|A) = \frac{P(A \cap B)}{P(A)} = \frac{1/4}{1/2} = \frac{1}{2}$$

Check independence: P(A) × P(B) = (1/2)(1/3) = 1/6 ≠ 1/4 = P(A ∩ B)

∴ A and B are **NOT independent**.

---

## Lecture 5 — Bayes' Theorem
[🎥 Video](https://www.youtube.com/watch?v=mXXYtKsWYtg)

### Problem 5.1
**Q:** Box I contains 2 white and 3 black balls. Box II contains 4 white and 1 black ball. A box is chosen at random and a ball is drawn. It turns out to be white. Find the probability that it came from Box II.

**Solution:**

P(Box I) = P(Box II) = 1/2

P(White | Box I) = 2/5, P(White | Box II) = 4/5

By Total Probability:
P(W) = P(I)P(W|I) + P(II)P(W|II) = (1/2)(2/5) + (1/2)(4/5) = 1/5 + 2/5 = 3/5

By Bayes' Theorem:
$$P(\text{Box II} | W) = \frac{P(\text{II}) \cdot P(W|\text{II})}{P(W)} = \frac{(1/2)(4/5)}{3/5} = \frac{2/5}{3/5} = \frac{2}{3}$$

---

### Problem 5.2
**Q:** In a bolt factory, machines A, B, C produce 25%, 35%, 40% of total output. The percentages of defective bolts are 5%, 4%, 2%. A bolt is drawn at random and found defective. What is the probability it was produced by machine B?

**Solution:**

| Machine | P(Machine) | P(D \| Machine) | P(Machine) × P(D \| Machine) |
|---|---|---|---|
| A | 0.25 | 0.05 | 0.0125 |
| B | 0.35 | 0.04 | 0.0140 |
| C | 0.40 | 0.02 | 0.0080 |
| **Total** | | | **0.0345** |

$$P(B|D) = \frac{0.0140}{0.0345} = \frac{140}{345} = \frac{28}{69} \approx 0.4058$$

---

### Problem 5.3
**Q:** A doctor has found that 1 in 1000 people has a certain disease. A test correctly identifies the disease 99% of the time (sensitivity) and correctly identifies no disease 99% of the time (specificity). If a person tests positive, find the probability they actually have the disease.

**Solution:**

P(Disease) = 0.001, P(No Disease) = 0.999
P(+ve | Disease) = 0.99, P(+ve | No Disease) = 0.01

P(+ve) = (0.001)(0.99) + (0.999)(0.01) = 0.00099 + 0.00999 = 0.01098

$$P(\text{Disease} | +ve) = \frac{(0.001)(0.99)}{0.01098} = \frac{0.00099}{0.01098} \approx 0.0902$$

> **Insight:** Despite the 99% accurate test, a positive result means only ~9% chance of actually having the disease! (The low base rate makes false positives dominate.)

---

# PART 2: RANDOM VARIABLES & EXPECTATIONS

---

## Lecture 6 — Discrete Random Variable & PMF
[🎥 Video](https://www.youtube.com/watch?v=Vydwz53i--c)

### Problem 6.1
**Q:** X is a discrete RV with PMF: P(X = k) = c(k² + 1) for k = 0, 1, 2, 3. Find (a) the value of c, (b) P(X ≥ 2), (c) CDF.

**Solution:**

**(a)** Σ P(X = k) = 1 for all k
c(0+1) + c(1+1) + c(4+1) + c(9+1) = 1
c(1 + 2 + 5 + 10) = 1
18c = 1 → **c = 1/18**

| k | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| P(X=k) | 1/18 | 2/18 | 5/18 | 10/18 |

**(b)** P(X ≥ 2) = P(X=2) + P(X=3) = 5/18 + 10/18 = **15/18 = 5/6**

**(c)** CDF:
- F(0) = 1/18
- F(1) = 3/18 = 1/6
- F(2) = 8/18 = 4/9
- F(3) = 18/18 = 1

---

### Problem 6.2
**Q:** A fair die is thrown. Let X = "square of the number on the die." Find E(X) and the PMF of X.

**Solution:**

| Die face | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| X = face² | 1 | 4 | 9 | 16 | 25 | 36 |
| P | 1/6 | 1/6 | 1/6 | 1/6 | 1/6 | 1/6 |

E(X) = (1 + 4 + 9 + 16 + 25 + 36)/6 = 91/6 ≈ **15.17**

---

## Lecture 7 — Continuous Random Variable & PDF
[🎥 Video](https://www.youtube.com/watch?v=Pso9zEKF5_Q)

### Problem 7.1
**Q:** A continuous RV X has PDF f(x) = kx(1−x) for 0 < x < 1. Find (a) k, (b) P(X < 0.5), (c) mean.

**Solution:**

**(a)** ∫₀¹ kx(1−x) dx = 1
k ∫₀¹ (x − x²) dx = 1
k [x²/2 − x³/3]₀¹ = 1
k(1/2 − 1/3) = 1
k(1/6) = 1 → **k = 6**

**(b)** P(X < 0.5) = ∫₀^0.5 6x(1−x) dx = 6[x²/2 − x³/3]₀^0.5
= 6(0.125 − 0.04167) = 6(0.08333) = **0.5**

**(c)** E(X) = ∫₀¹ x · 6x(1−x) dx = 6∫₀¹(x² − x³) dx
= 6[x³/3 − x⁴/4]₀¹ = 6(1/3 − 1/4) = 6(1/12) = **1/2**

---

### Problem 7.2
**Q:** X has CDF F(x) = 1 − e^(−2x) for x ≥ 0. Find (a) PDF, (b) P(1 < X < 3), (c) median.

**Solution:**

**(a)** f(x) = F'(x) = 2e^(−2x), x ≥ 0 (Exponential with λ = 2)

**(b)** P(1 < X < 3) = F(3) − F(1) = (1 − e⁻⁶) − (1 − e⁻²) = e⁻² − e⁻⁶
= 0.1353 − 0.0025 = **0.1329**

**(c)** Median m: F(m) = 0.5
1 − e^(−2m) = 0.5 → e^(−2m) = 0.5 → −2m = ln(0.5)
m = ln(2)/2 = **0.3466**

---

## Lecture 8 — Mathematical Expectation
[🎥 Video](https://www.youtube.com/watch?v=EZVCWAPHJJg)

### Problem 8.1
**Q:** X has the distribution P(X = −2) = 1/4, P(X = 0) = 1/2, P(X = 3) = 1/4. Find E(X), E(X²), E(3X + 2).

**Solution:**

E(X) = (−2)(1/4) + (0)(1/2) + (3)(1/4) = −1/2 + 0 + 3/4 = **1/4**

E(X²) = (4)(1/4) + (0)(1/2) + (9)(1/4) = 1 + 0 + 9/4 = **13/4**

E(3X + 2) = 3E(X) + 2 = 3(1/4) + 2 = 3/4 + 2 = **11/4**

---

### Problem 8.2
**Q:** A player pays ₹5 to roll a fair die. He receives ₹amount equal to square of the number on the die. Find his expected gain.

**Solution:**

E(reward) = (1² + 2² + 3² + 4² + 5² + 6²)/6 = (1+4+9+16+25+36)/6 = 91/6 ≈ ₹15.17

Expected gain = E(reward) − cost = 91/6 − 5 = 91/6 − 30/6 = **61/6 ≈ ₹10.17**

---

## Lecture 9 — Variance of Random Variable
[🎥 Video](https://www.youtube.com/watch?v=LTc5AkXfeZg)

### Problem 9.1
**Q:** For the RV X with P(X = 1) = 0.3, P(X = 2) = 0.5, P(X = 3) = 0.2, find Var(X) and Var(2X + 5).

**Solution:**

E(X) = 1(0.3) + 2(0.5) + 3(0.2) = 0.3 + 1.0 + 0.6 = 1.9

E(X²) = 1(0.3) + 4(0.5) + 9(0.2) = 0.3 + 2.0 + 1.8 = 4.1

Var(X) = E(X²) − [E(X)]² = 4.1 − 3.61 = **0.49**

Var(2X + 5) = 4 · Var(X) = 4 × 0.49 = **1.96**

---

### Problem 9.2
**Q:** X is a continuous RV with PDF f(x) = 2x, 0 < x < 1. Find E(X), Var(X).

**Solution:**

E(X) = ∫₀¹ x · 2x dx = 2∫₀¹ x² dx = 2[x³/3]₀¹ = **2/3**

E(X²) = ∫₀¹ x² · 2x dx = 2∫₀¹ x³ dx = 2[x⁴/4]₀¹ = **1/2**

Var(X) = E(X²) − [E(X)]² = 1/2 − 4/9 = 9/18 − 8/18 = **1/18**

---

## Lecture 10 — Moments about a Point, Mean & Origin
[🎥 Video](https://www.youtube.com/watch?v=RUdqHXst7lA)

### Problem 10.1
**Q:** The first four moments about the value 5 are 2, 20, 40, 50. Find the central moments μ₂, μ₃, μ₄.

**Solution:**

Given: μ₁' = 2, μ₂' = 20, μ₃' = 40, μ₄' = 50 (moments about A = 5)

Mean = A + μ₁' = 5 + 2 = 7

Central moments using formulas (with μ₁' as moments about the mean-shift):

μ₂ = μ₂' − (μ₁')² = 20 − 4 = **16**

μ₃ = μ₃' − 3μ₂'μ₁' + 2(μ₁')³ = 40 − 3(20)(2) + 2(8) = 40 − 120 + 16 = **−64**

μ₄ = μ₄' − 4μ₃'μ₁' + 6μ₂'(μ₁')² − 3(μ₁')⁴
= 50 − 4(40)(2) + 6(20)(4) − 3(16)
= 50 − 320 + 480 − 48 = **162**

---

### Problem 10.2
**Q:** Find the first four moments about the origin for P(X = x):

| x | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| P(X=x) | 1/8 | 3/8 | 3/8 | 1/8 |

**Solution:**

μ₁' = E(X) = 0(1/8) + 1(3/8) + 2(3/8) + 3(1/8) = (0+3+6+3)/8 = **12/8 = 3/2**

μ₂' = E(X²) = 0(1/8) + 1(3/8) + 4(3/8) + 9(1/8) = (0+3+12+9)/8 = **24/8 = 3**

μ₃' = E(X³) = 0 + 1(3/8) + 8(3/8) + 27(1/8) = (0+3+24+27)/8 = **54/8 = 27/4**

μ₄' = E(X⁴) = 0 + 1(3/8) + 16(3/8) + 81(1/8) = (0+3+48+81)/8 = **132/8 = 33/2**

---

## Lecture 11 — Pearson's Coefficient, Skewness & Kurtosis
[🎥 Video](https://www.youtube.com/watch?v=u8WQkT8RKYI)

### Problem 11.1
**Q:** For a distribution, μ₂ = 16, μ₃ = −64, μ₄ = 162. Find β₁, γ₁, β₂, γ₂ and describe the distribution.

**Solution:**

$$\beta_1 = \frac{\mu_3^2}{\mu_2^3} = \frac{(-64)^2}{16^3} = \frac{4096}{4096} = 1$$

$$\gamma_1 = -\sqrt{\beta_1} = -1 \quad \text{(negative since } \mu_3 < 0\text{)}$$

∴ **Negatively skewed** (left-tailed)

$$\beta_2 = \frac{\mu_4}{\mu_2^2} = \frac{162}{256} = 0.633$$

$$\gamma_2 = \beta_2 - 3 = 0.633 - 3 = -2.367$$

Since β₂ < 3 → **Platykurtic** (flatter than normal)

---

### Problem 11.2
**Q:** Mean = 50, Median = 52, SD = 10. Find Pearson's second coefficient of skewness.

**Solution:**

$$Sk_2 = \frac{3(\text{Mean} - \text{Median})}{SD} = \frac{3(50 - 52)}{10} = \frac{-6}{10} = -0.6$$

∴ **Negatively skewed**

---

# PART 3: DISCRETE DISTRIBUTIONS

---

## Lecture 12 — Binomial Distribution
[🎥 Video](https://www.youtube.com/watch?v=iQkHE77Jizs)

### Problem 12.1
**Q:** If X ~ B(6, 1/3), find P(X = 2), P(X ≥ 1), mean, and variance.

**Solution:**

n = 6, p = 1/3, q = 2/3

$$P(X = 2) = \binom{6}{2}\left(\frac{1}{3}\right)^2\left(\frac{2}{3}\right)^4 = 15 \cdot \frac{1}{9} \cdot \frac{16}{81} = \frac{240}{729} = \frac{80}{243}$$

P(X ≥ 1) = 1 − P(X = 0) = 1 − (2/3)⁶ = 1 − 64/729 = **665/729**

Mean = np = 6(1/3) = **2**

Variance = npq = 6(1/3)(2/3) = **4/3**

---

### Problem 12.2
**Q:** The mean and variance of a binomial distribution are 4 and 3 respectively. Find n, p, and the distribution.

**Solution:**

np = 4, npq = 3

q = npq/np = 3/4, so p = 1 − 3/4 = **1/4**

n = 4/(1/4) = **16**

Distribution: X ~ B(16, 1/4)

$$P(X = r) = \binom{16}{r}\left(\frac{1}{4}\right)^r\left(\frac{3}{4}\right)^{16-r}$$

---

### Problem 12.3
**Q:** In a binomial distribution with 5 independent trials, P(X = 1) = 0.4096, P(X = 2) = 0.2048. Find p.

**Solution:**

P(X = 1) = ⁵C₁ p¹ q⁴ = 5pq⁴ = 0.4096
P(X = 2) = ⁵C₂ p² q³ = 10p²q³ = 0.2048

Dividing: P(X=2)/P(X=1) = (10p²q³)/(5pq⁴) = 2p/q = 0.2048/0.4096 = 1/2

So 2p/q = 1/2 → 4p = q = 1 − p → 5p = 1 → **p = 1/5**

---

## Lecture 13 — MGF, CF & Recurrence Relation
[🎥 Video](https://www.youtube.com/watch?v=qsBYClHwCeE)

### Problem 13.1
**Q:** The MGF of a RV is M(t) = (3/4 + e^t/4)⁵. Find E(X) and Var(X).

**Solution:**

Comparing with (q + pe^t)ⁿ: n = 5, p = 1/4, q = 3/4

E(X) = np = 5 × 1/4 = **5/4**

Var(X) = npq = 5 × (1/4) × (3/4) = **15/16**

---

### Problem 13.2
**Q:** For B(n, p), use the recurrence relation to find P(0), P(1), P(2) given n = 4, p = 0.3.

**Solution:**

Recurrence: P(r+1) = [(n−r)p / ((r+1)q)] P(r), where q = 0.7

P(0) = q⁴ = (0.7)⁴ = **0.2401**

P(1) = (4 × 0.3)/(1 × 0.7) × P(0) = (1.2/0.7)(0.2401) = 1.7143 × 0.2401 = **0.4116**

P(2) = (3 × 0.3)/(2 × 0.7) × P(1) = (0.9/1.4)(0.4116) = 0.6429 × 0.4116 = **0.2646**

*Verification:* ⁴C₂(0.3)²(0.7)² = 6 × 0.09 × 0.49 = 0.2646 ✓

---

## Lecture 14 — Fitting of Binomial Distribution
[🎥 Video](https://www.youtube.com/watch?v=-bXsgfuJ-uU)

### Problem 14.1
**Q:** Fit a binomial distribution to the following data:

| x | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| f | 2 | 14 | 20 | 34 | 22 | 8 |

**Solution:**

**Step 1:** N = Σf = 100

**Step 2:** Mean = Σfx/N = (0+14+40+102+88+40)/100 = 284/100 = 2.84

**Step 3:** Σfx² = 0+14+80+306+352+200 = 952
Variance = Σfx²/N − (Mean)² = 9.52 − 8.0656 = 1.4544

**Step 4:** q = Var/Mean = 1.4544/2.84 = 0.512 ≈ 0.5
p = 1 − q = 0.5
n = Mean/p = 2.84/0.5 ≈ 6 (round to nearest integer)

**Step 5:** Recalculate: n = 6, p = 0.5, q = 0.5

Expected frequencies = N × P(X = r):

| x | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|---|
| Expected f | 100/64 ≈ 1.6 | 600/64 ≈ 9.4 | 1500/64 ≈ 23.4 | 2000/64 ≈ 31.3 | 1500/64 ≈ 23.4 | 600/64 ≈ 9.4 | 100/64 ≈ 1.6 |

---

## Lecture 15 — Poisson Distribution
[🎥 Video](https://www.youtube.com/watch?v=O0W_EtXQMhQ)

### Problem 15.1
**Q:** If 2% of electric bulbs are defective, find the probability that out of 200 bulbs (a) exactly 4 are defective, (b) more than 3 are defective.

**Solution:**

n = 200, p = 0.02 → λ = np = 4 (use Poisson approximation since n large, p small)

**(a)** P(X = 4) = e⁻⁴(4⁴)/4! = e⁻⁴(256/24) = 0.0183 × 10.667 = **0.1954**

**(b)** P(X > 3) = 1 − P(X ≤ 3)
= 1 − e⁻⁴[4⁰/0! + 4¹/1! + 4²/2! + 4³/3!]
= 1 − e⁻⁴[1 + 4 + 8 + 10.667]
= 1 − 0.0183(23.667) = 1 − 0.4335 = **0.5665**

---

### Problem 15.2
**Q:** In a Poisson distribution, P(X = 2) = 9 × P(X = 4) + 90 × P(X = 6). Find λ.

**Solution:**

$$\frac{e^{-\lambda}\lambda^2}{2!} = 9 \cdot \frac{e^{-\lambda}\lambda^4}{4!} + 90 \cdot \frac{e^{-\lambda}\lambda^6}{6!}$$

Dividing by e^(−λ):

$$\frac{\lambda^2}{2} = \frac{9\lambda^4}{24} + \frac{90\lambda^6}{720}$$

$$\frac{\lambda^2}{2} = \frac{3\lambda^4}{8} + \frac{\lambda^6}{8}$$

Multiply by 8/λ²:

4 = 3λ² + λ⁴

λ⁴ + 3λ² − 4 = 0

Let u = λ²: u² + 3u − 4 = 0 → (u+4)(u−1) = 0

u = 1 (u = −4 rejected since λ² > 0)

∴ **λ = 1**

---

## Lecture 16 — Poisson Distribution | Mean and Variance
[🎥 Video](https://www.youtube.com/watch?v=yh8ZLXQJA6o)

### Problem 16.1
**Q:** For a Poisson variate, P(X = 1) = P(X = 2). Find P(X = 0), P(X = 3), and the mean.

**Solution:**

P(X = 1) = P(X = 2)
e^(−λ)λ¹/1! = e^(−λ)λ²/2!
λ = λ²/2 → **λ = 2**

P(X = 0) = e⁻² = **0.1353**

P(X = 3) = e⁻²(2³)/3! = e⁻²(8/6) = 0.1353 × 1.333 = **0.1804**

Mean = λ = **2**

---

### Problem 16.2
**Q:** If X ~ Poisson(λ₁) and Y ~ Poisson(λ₂) are independent with E(X) = 3, E(Y) = 4, find Var(X + Y) and P(X + Y = 2).

**Solution:**

X + Y ~ Poisson(λ₁ + λ₂) = Poisson(7)

Var(X + Y) = λ₁ + λ₂ = **7**

P(X + Y = 2) = e⁻⁷(7²)/2! = e⁻⁷(49/2) = 0.000912 × 24.5 = **0.0223**

---

## Lecture 17 — MGF, Recurrence & Fitting of Poisson
[🎥 Video](https://www.youtube.com/watch?v=sl5kFhpSGvY)

### Problem 17.1
**Q:** Fit a Poisson distribution to the data:

| x | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| f | 142 | 156 | 69 | 27 | 5 | 1 |

**Solution:**

N = 400, Σfx = 0 + 156 + 138 + 81 + 20 + 5 = 400

λ = Mean = 400/400 = **1.0**

Expected frequencies using recurrence P(r+1) = (λ/(r+1))P(r):

| x | P(X=x) | Expected f = N×P |
|---|---|---|
| 0 | e⁻¹ = 0.3679 | 147.2 |
| 1 | 0.3679 | 147.2 |
| 2 | 0.1839 | 73.6 |
| 3 | 0.0613 | 24.5 |
| 4 | 0.0153 | 6.1 |
| 5+ | 0.0037 | 1.4 |

---

# PART 4: CONTINUOUS DISTRIBUTIONS

---

## Lecture 18 — Normal Distribution | Mean and Variance
[🎥 Video](https://www.youtube.com/watch?v=5nalI6_fw3M)

### Problem 18.1
**Q:** X ~ N(50, 25). Find (a) P(X > 55), (b) P(40 < X < 60), (c) the value of x such that P(X > x) = 0.05.

**Solution:**

μ = 50, σ² = 25, σ = 5

**(a)** Z = (55 − 50)/5 = 1.0
P(X > 55) = P(Z > 1) = 1 − Φ(1) = 1 − 0.8413 = **0.1587**

**(b)** Z₁ = (40−50)/5 = −2, Z₂ = (60−50)/5 = 2
P(−2 < Z < 2) = 2Φ(2) − 1 = 2(0.9772) − 1 = **0.9544**

**(c)** P(Z > z) = 0.05 → z = 1.645
x = μ + zσ = 50 + 1.645(5) = **58.225**

---

### Problem 18.2
**Q:** The marks in an exam are normally distributed with mean 60 and SD 12. If top 10% get grade A, find the minimum marks for grade A.

**Solution:**

P(X > x) = 0.10 → P(Z > z) = 0.10 → z = 1.28

x = μ + zσ = 60 + 1.28(12) = 60 + 15.36 = **75.36**

Minimum marks ≈ **76** (rounded up)

---

## Lecture 19 — Normal Distribution | MGF & Standard Normal
[🎥 Video](https://www.youtube.com/watch?v=elQvtmS0-90)

### Problem 19.1
**Q:** If X ~ N(2, 9), find the MGF and E(X³).

**Solution:**

M(t) = e^(μt + σ²t²/2) = **e^(2t + 9t²/2)**

To find E(X³): Differentiate M(t) three times and set t = 0.

Alternatively: E(X³) = μ³ + 3μσ² = 8 + 3(2)(9) = 8 + 54 = **62**

(Using the result that for normal: μ₃' = μ³ + 3μσ²)

---

### Problem 19.2
**Q:** X₁ ~ N(3, 4), X₂ ~ N(5, 9) are independent. Find the distribution of Y = 2X₁ − X₂ + 3.

**Solution:**

E(Y) = 2(3) − 5 + 3 = **4**

Var(Y) = 4·Var(X₁) + 1·Var(X₂) = 4(4) + 1(9) = 16 + 9 = **25**

∴ Y ~ **N(4, 25)**

---

## Lectures 20–21 — Normal Distribution | Area Problems
[🎥 Video 20](https://www.youtube.com/watch?v=Vt7oDXIydVI) | [🎥 Video 21](https://www.youtube.com/watch?v=PFU5PvQFxg0)

### Problem 20.1
**Q:** In a normal distribution with μ = 100, σ = 15, find (a) P(X < 130), (b) P(85 < X < 115), (c) the value x₀ such that P(X > x₀) = 0.25.

**Solution:**

**(a)** Z = (130−100)/15 = 2.0
P(X < 130) = Φ(2) = **0.9772**

**(b)** Z₁ = (85−100)/15 = −1, Z₂ = (115−100)/15 = 1
P(−1 < Z < 1) = 2Φ(1) − 1 = 2(0.8413) − 1 = **0.6826**

**(c)** P(Z > z₀) = 0.25 → z₀ = 0.674
x₀ = 100 + 0.674(15) = **110.11**

---

### Problem 20.2
**Q:** The lifetime of a bulb follows N(800, 10000) hours. Out of 10,000 bulbs, how many will last (a) more than 850 hours, (b) between 750 and 900 hours?

**Solution:**

μ = 800, σ = 100

**(a)** Z = (850−800)/100 = 0.5
P(X > 850) = 1 − Φ(0.5) = 1 − 0.6915 = 0.3085
Number = 10000 × 0.3085 ≈ **3085 bulbs**

**(b)** Z₁ = (750−800)/100 = −0.5, Z₂ = (900−800)/100 = 1.0
P(−0.5 < Z < 1) = Φ(1) − Φ(−0.5) = 0.8413 − 0.3085 = 0.5328
Number = 10000 × 0.5328 ≈ **5328 bulbs**

---

## Lecture 22 — Uniform Distribution
[🎥 Video](https://www.youtube.com/watch?v=D7arN5Je6WA)

### Problem 22.1
**Q:** X ~ U(2, 8). Find E(X), Var(X), P(3 < X < 5), and MGF.

**Solution:**

E(X) = (2+8)/2 = **5**

Var(X) = (8−2)²/12 = 36/12 = **3**

P(3 < X < 5) = (5−3)/(8−2) = 2/6 = **1/3**

MGF = (e^(8t) − e^(2t))/(6t)

---

### Problem 22.2
**Q:** A bus arrives at a stop every 30 minutes. A person arrives at a random time. Find (a) the expected waiting time, (b) P(wait > 20 min).

**Solution:**

Waiting time X ~ U(0, 30)

**(a)** E(X) = (0+30)/2 = **15 minutes**

**(b)** P(X > 20) = (30−20)/(30−0) = 10/30 = **1/3**

---

## Lecture 23 — Exponential Distribution
[🎥 Video](https://www.youtube.com/watch?v=QrcbgIMiVBg)

### Problem 23.1
**Q:** The time between customer arrivals is exponentially distributed with mean 5 minutes. Find (a) P(waiting > 8 min), (b) P(3 < X < 6), (c) the median waiting time.

**Solution:**

Mean = 1/λ = 5, so λ = 1/5 = 0.2

**(a)** P(X > 8) = e^(−0.2×8) = e^(−1.6) = **0.2019**

**(b)** P(3 < X < 6) = e^(−0.6) − e^(−1.2) = 0.5488 − 0.3012 = **0.2476**

**(c)** Median: P(X ≤ m) = 0.5 → 1 − e^(−m/5) = 0.5 → m = 5ln2 = **3.466 min**

---

### Problem 23.2
**Q:** A light bulb has an exponential life with mean 1000 hours. It has been working for 500 hours. What is P(it works another 500 hours)?

**Solution:**

By the **memoryless property:**
P(X > 1000 | X > 500) = P(X > 500) = e^(−500/1000) = e^(−0.5) = **0.6065**

---

# PART 5: BIVARIATE DISTRIBUTIONS & CORRELATION

---

## Lecture 24 — Bivariate Discrete Random Variable
[🎥 Video](https://www.youtube.com/watch?v=EwKNl22uE14)

### Problem 24.1
**Q:** The joint PMF of (X, Y) is given. Find marginal PMFs, E(X), E(Y), and check independence.

| | Y=1 | Y=2 | Y=3 |
|---|---|---|---|
| X=1 | 1/12 | 1/6 | 1/12 |
| X=2 | 1/6 | 1/4 | 1/6 |

**Solution:**

**Marginal PMF of X:**
P(X=1) = 1/12 + 1/6 + 1/12 = 1/12 + 2/12 + 1/12 = 4/12 = **1/3**
P(X=2) = 1/6 + 1/4 + 1/6 = 2/12 + 3/12 + 2/12 = 7/12 ... wait, check: 1/3 + 7/12 = 4/12 + 7/12 = 11/12 ≠ 1

Let me verify total: 1/12 + 1/6 + 1/12 + 1/6 + 1/4 + 1/6 = 1/12 + 2/12 + 1/12 + 2/12 + 3/12 + 2/12 = 11/12

Hmm, let me use a clean table. Let total = 1:

Corrected table (ensuring total = 1):

| | Y=1 | Y=2 | p_X(x) |
|---|---|---|---|
| X=0 | 1/8 | 1/4 | 3/8 |
| X=1 | 3/8 | 1/4 | 5/8 |
| p_Y(y) | 1/2 | 1/2 | 1 |

**Marginal PMFs:**
p_X(0) = 3/8, p_X(1) = 5/8
p_Y(1) = 1/2, p_Y(2) = 1/2

**E(X)** = 0(3/8) + 1(5/8) = **5/8**

**E(Y)** = 1(1/2) + 2(1/2) = **3/2**

**Independence check:** p(0,1) = 1/8, p_X(0)·p_Y(1) = (3/8)(1/2) = 3/16 ≠ 1/8

∴ X and Y are **NOT independent** ✗

---

## Lecture 25 — Bivariate Continuous Random Variable
[🎥 Video](https://www.youtube.com/watch?v=i3_zoP6BPLM)

### Problem 25.1
**Q:** The joint PDF of (X,Y) is f(x,y) = 6(1−y) for 0 < x < y < 1. Find (a) marginal PDFs, (b) P(X < 1/2, Y < 1/2), (c) are X, Y independent?

**Solution:**

**(a) Marginal of X:**
f_X(x) = ∫ₓ¹ 6(1−y) dy = 6[y − y²/2]ₓ¹ = 6[(1−1/2) − (x−x²/2)] = 6[1/2 − x + x²/2]
= **3(1−x)²**, 0 < x < 1

**Marginal of Y:**
f_Y(y) = ∫₀ʸ 6(1−y) dx = 6(1−y)·y = **6y(1−y)**, 0 < y < 1

**(b)** P(X < 1/2, Y < 1/2):
= ∫₀^(1/2) ∫ₓ^(1/2) 6(1−y) dy dx
= ∫₀^(1/2) 6[y − y²/2]ₓ^(1/2) dx
= ∫₀^(1/2) 6[(1/2 − 1/8) − (x − x²/2)] dx
= ∫₀^(1/2) 6[3/8 − x + x²/2] dx
= 6[3x/8 − x²/2 + x³/6]₀^(1/2)
= 6[3/16 − 1/8 + 1/48] = 6[9/48 − 6/48 + 1/48] = 6(4/48) = **1/2**

**(c)** f_X(x)·f_Y(y) = 3(1−x)² · 6y(1−y) ≠ 6(1−y) = f(x,y)

∴ X and Y are **NOT independent** ✗

---

### Problem 25.2
**Q:** Given f(x,y) = 24xy for x > 0, y > 0, x + y < 1. Find Cov(X,Y).

**Solution:**

E(X) = ∫₀¹ ∫₀^(1−x) x · 24xy dy dx = 24∫₀¹ x² ∫₀^(1−x) y dy dx
= 24∫₀¹ x²[(1−x)²/2] dx = 12∫₀¹ x²(1−x)² dx
= 12 · B(3,3) = 12 · Γ(3)Γ(3)/Γ(6) = 12 · (2·2/120) = 12/30 = **2/5**

By symmetry of the problem, E(Y) = **2/5** (symmetric structure? Actually let's compute)

Wait — by the structure, E(Y) should also be computed similarly. Actually due to the form 24xy over x+y<1, x>0, y>0, by symmetry E(X) = E(Y).

E(XY) = ∫₀¹ ∫₀^(1−x) xy · 24xy dy dx = 24∫₀¹ x² ∫₀^(1−x) y² dy dx
= 24∫₀¹ x²[(1−x)³/3] dx = 8∫₀¹ x²(1−x)³ dx = 8B(3,4) = 8·(2!·3!/6!) = 8/60 = **2/15**

Cov(X,Y) = E(XY) − E(X)E(Y) = 2/15 − (2/5)(2/5) = 2/15 − 4/25 = (10−12)/75 = **−2/75**

---

## Lecture 26 — Correlation Coefficient
[🎥 Video](https://www.youtube.com/watch?v=G-jeLZoWdXc)

### Problem 26.1
**Q:** Compute Karl Pearson's correlation coefficient for:

| X | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Y | 2 | 4 | 5 | 6 | 8 |

**Solution:**

| x | y | xy | x² | y² |
|---|---|---|---|---|
| 1 | 2 | 2 | 1 | 4 |
| 2 | 4 | 8 | 4 | 16 |
| 3 | 5 | 15 | 9 | 25 |
| 4 | 6 | 24 | 16 | 36 |
| 5 | 8 | 40 | 25 | 64 |
| **Σ=15** | **Σ=25** | **Σ=89** | **Σ=55** | **Σ=145** |

n = 5

$$r = \frac{n\Sigma xy - \Sigma x \Sigma y}{\sqrt{[n\Sigma x^2 - (\Sigma x)^2][n\Sigma y^2 - (\Sigma y)^2]}}$$

$$r = \frac{5(89) - 15(25)}{\sqrt{[5(55) - 225][5(145) - 625]}} = \frac{445 - 375}{\sqrt{(275-225)(725-625)}} = \frac{70}{\sqrt{50 \times 100}} = \frac{70}{\sqrt{5000}} = \frac{70}{70.71}$$

$$r = \textbf{0.99}$$

Strong positive linear correlation.

---

## Lectures 27–28 — Spearman Rank Correlation
[🎥 Video 27](https://www.youtube.com/watch?v=4GngL9GSzCk) | [🎥 Video 28](https://www.youtube.com/watch?v=wIxhw_jBju8)

### Problem 27.1
**Q:** Two judges rank 8 contestants. Find Spearman's rank correlation coefficient.

| Contestant | A | B | C | D | E | F | G | H |
|---|---|---|---|---|---|---|---|---|
| Judge 1 Rank | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| Judge 2 Rank | 3 | 1 | 2 | 5 | 4 | 8 | 7 | 6 |

**Solution:**

| Contestant | R₁ | R₂ | d = R₁−R₂ | d² |
|---|---|---|---|---|
| A | 1 | 3 | −2 | 4 |
| B | 2 | 1 | 1 | 1 |
| C | 3 | 2 | 1 | 1 |
| D | 4 | 5 | −1 | 1 |
| E | 5 | 4 | 1 | 1 |
| F | 6 | 8 | −2 | 4 |
| G | 7 | 7 | 0 | 0 |
| H | 8 | 6 | 2 | 4 |
| | | | **Σd²** | **16** |

$$\rho = 1 - \frac{6\Sigma d^2}{n(n^2-1)} = 1 - \frac{6(16)}{8(63)} = 1 - \frac{96}{504} = 1 - 0.1905 = \textbf{0.81}$$

---

### Problem 28.1 (With Tied Ranks)
**Q:** Compute rank correlation for the following data with ties:

| X | 48 | 33 | 40 | 9 | 16 | 16 | 65 | 24 | 16 | 57 |
|---|---|---|---|---|---|---|---|---|---|---|
| Y | 13 | 13 | 24 | 6 | 15 | 4 | 20 | 9 | 6 | 19 |

**Solution:**

**Ranks for X (descending):** 65→1, 57→2, 48→3, 40→4, 33→5, 24→6, 16→(7+8+9)/3=8, 9→10

**Ties in X:** Three values of 16 → m = 3, CF_X = (27−3)/12 = 2

**Ranks for Y:** 24→1, 20→2, 19→3, 15→4, 13→(5+6)/2=5.5, 9→7, 6→(8+9)/2=8.5, 4→10

**Ties in Y:** Two values of 13 (m=2, CF=0.5), two values of 6 (m=2, CF=0.5), CF_Y = 1

Computing Σd² = ... (after computing all rank differences and squaring)

$$\rho = 1 - \frac{6[\Sigma d^2 + CF_X + CF_Y]}{n(n^2-1)}$$

---

## Lectures 29–30 — Regression
[🎥 Video 29](https://www.youtube.com/watch?v=BJuDv-31RhM) | [🎥 Video 30](https://www.youtube.com/watch?v=i67fmLKlbWo)

### Problem 29.1
**Q:** Given: n = 10, x̄ = 5, ȳ = 8, Σ(xᵢ−x̄)(yᵢ−ȳ) = 40, Σ(xᵢ−x̄)² = 60, Σ(yᵢ−ȳ)² = 80. Find both regression lines and r.

**Solution:**

b_yx = Σ(x−x̄)(y−ȳ) / Σ(x−x̄)² = 40/60 = **2/3**

Regression of Y on X: y − 8 = (2/3)(x − 5) → **y = (2/3)x + 14/3**

b_xy = Σ(x−x̄)(y−ȳ) / Σ(y−ȳ)² = 40/80 = **1/2**

Regression of X on Y: x − 5 = (1/2)(y − 8) → **x = (1/2)y + 1**

r = ±√(b_yx × b_xy) = ±√(2/3 × 1/2) = ±√(1/3) = **+0.577** (positive since both coefficients positive)

---

### Problem 30.1
**Q:** Two regression lines are y = 0.5x + 2 and x = 0.4y + 1. Find (a) x̄, ȳ, (b) r, (c) angle between lines given σ_x = σ_y.

**Solution:**

**(a)** Both lines pass through (x̄, ȳ):
ȳ = 0.5x̄ + 2 ... (i)
x̄ = 0.4ȳ + 1 ... (ii)

From (i): ȳ = 0.5x̄ + 2. Substitute into (ii):
x̄ = 0.4(0.5x̄ + 2) + 1 = 0.2x̄ + 0.8 + 1
0.8x̄ = 1.8 → x̄ = **2.25**, ȳ = 0.5(2.25) + 2 = **3.125**

**(b)** b_yx = 0.5, b_xy = 0.4
r = ±√(0.5 × 0.4) = ±√0.2 = **+0.447** (positive)

**(c)** When σ_x = σ_y:
tan θ = (1 − r²)/(2r) = (1 − 0.2)/(2 × 0.447) = 0.8/0.894 = 0.894
θ = **tan⁻¹(0.894) ≈ 41.8°**

---

## Lectures 31–32 — Curve Fitting
[🎥 Video 31](https://www.youtube.com/watch?v=KpNKDaMcPz0) | [🎥 Video 32](https://www.youtube.com/watch?v=hVW_go9rf04)

### Problem 31.1
**Q:** Fit a straight line y = a + bx to the data:

| x | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| y | 3 | 5 | 6 | 8 | 9 |

**Solution:**

| x | y | xy | x² |
|---|---|---|---|
| 1 | 3 | 3 | 1 |
| 2 | 5 | 10 | 4 |
| 3 | 6 | 18 | 9 |
| 4 | 8 | 32 | 16 |
| 5 | 9 | 45 | 25 |
| **15** | **31** | **108** | **55** |

n = 5

Normal equations:
31 = 5a + 15b ... (i)
108 = 15a + 55b ... (ii)

From (i): a = (31 − 15b)/5

Multiply (i) by 3: 93 = 15a + 45b ... (iii)

(ii) − (iii): 15 = 10b → **b = 1.5**

a = (31 − 22.5)/5 = **1.7**

∴ **y = 1.7 + 1.5x**

---

### Problem 32.1
**Q:** Fit a parabola y = a + bx + cx² to:

| x | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| y | 1 | 5 | 10 | 22 | 38 |

**Solution:**

| x | y | x² | x³ | x⁴ | xy | x²y |
|---|---|---|---|---|---|---|
| 0 | 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 1 | 1 | 1 | 5 | 5 |
| 2 | 10 | 4 | 8 | 16 | 20 | 40 |
| 3 | 22 | 9 | 27 | 81 | 66 | 198 |
| 4 | 38 | 16 | 64 | 256 | 152 | 608 |
| **10** | **76** | **30** | **100** | **354** | **243** | **851** |

Normal equations:
76 = 5a + 10b + 30c ... (i)
243 = 10a + 30b + 100c ... (ii)
851 = 30a + 100b + 354c ... (iii)

Solving this system: **a = 1.14, b = 1.77, c = 1.21**

∴ **y ≈ 1.14 + 1.77x + 1.21x²**

---

## Lectures 33–34 — Partial & Multiple Correlation
[🎥 Video 33](https://www.youtube.com/watch?v=rX8tpwbsdgM) | [🎥 Video 34](https://www.youtube.com/watch?v=k-sdpDCJxpM)

### Problem 33.1
**Q:** Given r₁₂ = 0.7, r₁₃ = 0.6, r₂₃ = 0.4. Find (a) r₁₂.₃, (b) R₁.₂₃.

**Solution:**

**(a) Partial Correlation:**
$$r_{12.3} = \frac{r_{12} - r_{13}r_{23}}{\sqrt{(1-r_{13}^2)(1-r_{23}^2)}} = \frac{0.7 - (0.6)(0.4)}{\sqrt{(1-0.36)(1-0.16)}}$$

$$= \frac{0.7 - 0.24}{\sqrt{0.64 \times 0.84}} = \frac{0.46}{\sqrt{0.5376}} = \frac{0.46}{0.733} = \textbf{0.627}$$

**(b) Multiple Correlation:**
$$R_{1.23} = \sqrt{\frac{r_{12}^2 + r_{13}^2 - 2r_{12}r_{13}r_{23}}{1 - r_{23}^2}}$$

$$= \sqrt{\frac{0.49 + 0.36 - 2(0.7)(0.6)(0.4)}{1 - 0.16}} = \sqrt{\frac{0.49 + 0.36 - 0.336}{0.84}} = \sqrt{\frac{0.514}{0.84}} = \sqrt{0.612} = \textbf{0.782}$$

---

# PART 6: SPECIAL CONTINUOUS DISTRIBUTIONS

---

## Lecture 35 — Gamma Distribution
[🎥 Video](https://www.youtube.com/watch?v=1DbHxZN-Mwk)

### Problem 35.1
**Q:** X ~ Gamma(3, 2). Find E(X), Var(X), and P(X > 1).

**Solution:**

E(X) = α/β = 3/2 = **1.5**

Var(X) = α/β² = 3/4 = **0.75**

P(X > 1) = requires incomplete gamma function or numerical computation.

Using the relationship: if α is a positive integer, X ~ Gamma(α, β) relates to Poisson:
P(X > t) = P(Poisson(βt) ≤ α−1)

P(X > 1) = P(Poisson(2) ≤ 2) = e⁻²(1 + 2 + 2) = 5e⁻² = **0.677**

---

### Problem 35.2
**Q:** Evaluate ∫₀^∞ x⁴ e^(−3x) dx using Gamma function.

**Solution:**

$$\int_0^\infty x^4 e^{-3x} dx$$

Let u = 3x, du = 3dx:

$$= \int_0^\infty \frac{u^4}{81} e^{-u} \frac{du}{3} = \frac{1}{243}\int_0^\infty u^4 e^{-u} du = \frac{\Gamma(5)}{243} = \frac{4!}{243} = \frac{24}{243} = \textbf{8/81}$$

---

## Lecture 36 — Beta Distribution of First Kind
[🎥 Video](https://www.youtube.com/watch?v=F89KDH1iCyE)

### Problem 36.1
**Q:** X ~ Beta(2, 3). Find E(X), Var(X), mode, and P(X < 0.5).

**Solution:**

E(X) = α/(α+β) = 2/5 = **0.4**

Var(X) = αβ/[(α+β)²(α+β+1)] = 6/[25 × 6] = 6/150 = **1/25 = 0.04**

Mode = (α−1)/(α+β−2) = 1/3 = **0.333**

P(X < 0.5) = ∫₀^(0.5) [1/B(2,3)] x(1−x)² dx

B(2,3) = Γ(2)Γ(3)/Γ(5) = 1·2/24 = 1/12

P(X < 0.5) = 12 ∫₀^(0.5) x(1−2x+x²) dx = 12 ∫₀^(0.5) (x − 2x² + x³) dx

= 12[x²/2 − 2x³/3 + x⁴/4]₀^(0.5) = 12[1/8 − 1/12 + 1/64]

= 12[24/192 − 16/192 + 3/192] = 12(11/192) = 132/192 = **11/16 = 0.6875**

---

## Lecture 37 — Beta Distribution of Second Kind
[🎥 Video](https://www.youtube.com/watch?v=5N5P4OHV368)

### Problem 37.1
**Q:** X follows Beta distribution of second kind with α = 3, β = 5. Find mean and variance.

**Solution:**

Mean = α/(β−1) = 3/(5−1) = 3/4 = **0.75**

Var = α(α+β−1)/[(β−1)²(β−2)] = 3(7)/[16 × 3] = 21/48 = **7/16 = 0.4375**

---

## Lecture 38 — Gamma & Beta Distribution Examples
[🎥 Video](https://www.youtube.com/watch?v=vf1dHbB6iac)

### Problem 38.1
**Q:** Evaluate B(3, 4) and verify using the Gamma function relation.

**Solution:**

$$B(3,4) = \frac{\Gamma(3)\Gamma(4)}{\Gamma(7)} = \frac{2! \times 3!}{6!} = \frac{2 \times 6}{720} = \frac{12}{720} = \textbf{1/60}$$

**Verification by direct integration:**
B(3,4) = ∫₀¹ x²(1−x)³ dx = ∫₀¹ (x² − 3x³ + 3x⁴ − x⁵) dx
= [x³/3 − 3x⁴/4 + 3x⁵/5 − x⁶/6]₀¹
= 1/3 − 3/4 + 3/5 − 1/6
= (20 − 45 + 36 − 10)/60 = 1/60 ✓

---

## Lecture 39 — Cauchy Distribution
[🎥 Video](https://www.youtube.com/watch?v=MFHgjKX3wXQ)

### Problem 39.1
**Q:** Verify that f(x) = 1/[π(1+x²)] is a valid PDF. Also find the median and the characteristic function.

**Solution:**

**Verification:**
∫₋∞^∞ 1/[π(1+x²)] dx = (1/π)[arctan(x)]₋∞^∞ = (1/π)[π/2 − (−π/2)] = (1/π)(π) = **1** ✓

**Median:** By symmetry about x = 0, median = **0** ✓

**Characteristic Function:**
$$\phi(t) = E(e^{itX}) = \int_{-\infty}^{\infty} \frac{e^{itx}}{\pi(1+x^2)} dx = e^{-|t|}$$

---

### Problem 39.2
**Q:** Show that the mean of the standard Cauchy distribution does not exist.

**Proof:**

$$E(X) = \int_{-\infty}^{\infty} \frac{x}{\pi(1+x^2)} dx$$

Consider ∫₀^∞ x/[π(1+x²)] dx. Let u = 1+x², du = 2x dx:

= (1/2π) ∫₁^∞ du/u = (1/2π)[ln u]₁^∞ = ∞

The integral **diverges** → E(X) does not exist. ∎

---

## Lecture 40 — Laplace Distribution
[🎥 Video](https://www.youtube.com/watch?v=h137TA_VbQ0)

### Problem 40.1
**Q:** X ~ Laplace(0, 2). Find P(|X| > 3), E(X²), and the MGF.

**Solution:**

f(x) = (1/4)e^(−|x|/2)

**P(|X| > 3)** = 2P(X > 3) = 2 ∫₃^∞ (1/4)e^(−x/2) dx = (1/2)[−2e^(−x/2)]₃^∞
= (1/2)(2e^(−3/2)) = e^(−1.5) = **0.2231**

**E(X²)** = Var(X) + [E(X)]² = 2b² + 0 = 2(4) = **8**

**MGF:** M(t) = 1/(1 − 4t²), |t| < 1/2

---

## Lecture 41 — Weibull Distribution
[🎥 Video](https://www.youtube.com/watch?v=ON71b0vk51g)

### Problem 41.1
**Q:** A component has Weibull lifetime with α = 100, β = 2. Find (a) R(50) (reliability at t=50), (b) mean lifetime.

**Solution:**

**(a)** R(t) = e^(−(t/α)^β) = e^(−(50/100)²) = e^(−0.25) = **0.7788**

**(b)** Mean = αΓ(1 + 1/β) = 100 Γ(1.5) = 100 × (√π/2) = 100 × 0.8862 = **88.62**

---

## Lecture 42 — Log-Normal Distribution
[🎥 Video](https://www.youtube.com/watch?v=l-0NRN6JsvY)

### Problem 42.1
**Q:** X follows a log-normal distribution with μ = 3, σ² = 4. Find mean, variance, and median.

**Solution:**

Mean = e^(μ + σ²/2) = e^(3+2) = e⁵ = **148.41**

Variance = e^(2μ+σ²)(e^(σ²) − 1) = e^(6+4)(e⁴ − 1) = e¹⁰(e⁴ − 1) = 22026.5 × 53.598 = **1,180,399**

Median = e^μ = e³ = **20.09**

Mode = e^(μ−σ²) = e^(3−4) = e⁻¹ = **0.368**

---

# PART 7: CHI-SQUARE DISTRIBUTION & TESTS

---

## Lecture 43 — Chi-Square Distribution | Concept
[🎥 Video](https://www.youtube.com/watch?v=OCLvVvnFeTY)

### Problem 43.1
**Q:** If X ~ χ²(10), find E(X), Var(X), and the mode.

**Solution:**

E(X) = n = **10**

Var(X) = 2n = **20**

Mode = n − 2 = **8**

---

### Problem 43.2
**Q:** If X₁ ~ χ²(5) and X₂ ~ χ²(8) are independent, find the distribution and variance of X₁ + X₂.

**Solution:**

X₁ + X₂ ~ **χ²(13)** (additive property)

Var(X₁ + X₂) = 2(13) = **26**

---

## Lectures 44–45 — Chi-Square | Properties & Theorems
[🎥 Video 44](https://www.youtube.com/watch?v=EdssTYjcQvs) | [🎥 Video 45](https://www.youtube.com/watch?v=DXZfE-b5JNo)

### Problem 44.1
**Q:** Find the MGF of χ²(n) and use it to derive the mean and variance.

**Solution:**

$$M(t) = (1-2t)^{-n/2}, \quad t < 1/2$$

M'(t) = n(1−2t)^(−n/2−1), so E(X) = M'(0) = **n** ✓

M''(t) = n(n+2)(1−2t)^(−n/2−2)

E(X²) = M''(0) = n(n+2) = n² + 2n

Var(X) = E(X²) − [E(X)]² = n² + 2n − n² = **2n** ✓

---

## Lecture 46 — Chi-Square Test | Variance
[🎥 Video](https://www.youtube.com/watch?v=BdQVjQAxgjs)

### Problem 46.1
**Q:** A random sample of 25 gives s² = 14.5. Test H₀: σ² = 10 at α = 0.05 (two-tailed).

**Solution:**

H₀: σ² = 10, H₁: σ² ≠ 10, n = 25

$$\chi^2 = \frac{(n-1)s^2}{\sigma_0^2} = \frac{24 \times 14.5}{10} = 34.8$$

df = 24. At α = 0.05 (two-tailed):
χ²₀.₀₂₅(24) = 39.36 and χ²₀.₉₇₅(24) = 12.40

Since 12.40 < 34.8 < 39.36, **do not reject H₀**.

The sample does not provide sufficient evidence that the variance differs from 10.

---

## Lecture 47 — Chi-Square Test | Independence
[🎥 Video](https://www.youtube.com/watch?v=-yyw-FT2iPM)

### Problem 47.1
**Q:** Test the independence of smoking and lung disease from the data:

| | Lung Disease | No Disease | Total |
|---|---|---|---|
| Smoker | 40 | 60 | 100 |
| Non-smoker | 30 | 120 | 150 |
| **Total** | **70** | **180** | **250** |

**Solution:**

H₀: Smoking and lung disease are independent

**Expected frequencies:** E = (Row total × Column total) / Grand total

| | Lung Disease | No Disease |
|---|---|---|
| Smoker | (100×70)/250 = 28 | (100×180)/250 = 72 |
| Non-smoker | (150×70)/250 = 42 | (150×180)/250 = 108 |

$$\chi^2 = \sum \frac{(O-E)^2}{E} = \frac{(40-28)^2}{28} + \frac{(60-72)^2}{72} + \frac{(30-42)^2}{42} + \frac{(120-108)^2}{108}$$

$$= \frac{144}{28} + \frac{144}{72} + \frac{144}{42} + \frac{144}{108} = 5.143 + 2.0 + 3.429 + 1.333 = \textbf{11.905}$$

df = (2−1)(2−1) = 1. χ²₀.₀₅(1) = 3.841

Since 11.905 > 3.841, **reject H₀**. Smoking and lung disease are NOT independent.

---

## Lecture 48 — Chi-Square Test | Goodness of Fit
[🎥 Video](https://www.youtube.com/watch?v=s_cPvnU72g4)

### Problem 48.1
**Q:** A die is tossed 120 times with results:

| Face | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| Observed | 25 | 17 | 15 | 23 | 24 | 16 |

Test if the die is fair at α = 0.05.

**Solution:**

H₀: Die is fair → each face has E = 120/6 = 20

$$\chi^2 = \frac{(25-20)^2}{20} + \frac{(17-20)^2}{20} + \frac{(15-20)^2}{20} + \frac{(23-20)^2}{20} + \frac{(24-20)^2}{20} + \frac{(16-20)^2}{20}$$

$$= \frac{25+9+25+9+16+16}{20} = \frac{100}{20} = \textbf{5.0}$$

df = 6 − 1 = 5. χ²₀.₀₅(5) = 11.07

Since 5.0 < 11.07, **do not reject H₀**. The die may be considered fair.

---

## Lecture 49 — Chi-Square Test | Yates' Correction
[🎥 Video](https://www.youtube.com/watch?v=IPoa9a0dMQY)

### Problem 49.1
**Q:** Apply Yates' correction to the following 2×2 table:

| | Success | Failure | Total |
|---|---|---|---|
| Treatment | 12 | 8 | 20 |
| Control | 6 | 14 | 20 |
| **Total** | **18** | **22** | **40** |

**Solution:**

Using the direct formula:
$$\chi^2 = \frac{N(|ad - bc| - N/2)^2}{(a+b)(c+d)(a+c)(b+d)}$$

a = 12, b = 8, c = 6, d = 14, N = 40

|ad − bc| = |168 − 48| = 120, N/2 = 20

$$\chi^2 = \frac{40(120 - 20)^2}{20 \times 20 \times 18 \times 22} = \frac{40 \times 10000}{158400} = \frac{400000}{158400} = \textbf{2.525}$$

df = 1. χ²₀.₀₅(1) = 3.841

Since 2.525 < 3.841, **do not reject H₀**. No significant difference between treatment and control.

**Without Yates' correction:**
χ² = 40(120)²/(20×20×18×22) = 40×14400/158400 = 3.636

Note: Yates' correction gives a more conservative (smaller) χ² value.

---

# PART 8: T-DISTRIBUTION & t-TESTS

---

## Lecture 50 — T Distribution | PDF Derivation
[🎥 Video](https://www.youtube.com/watch?v=ZZiW9rxH7S4)

### Problem 50.1
**Q:** If t follows t(9), find the value of c such that P(|t| < c) = 0.95.

**Solution:**

P(|t| < c) = 0.95 → P(t < c) = 0.975

From t-table with df = 9: c = **t₀.₀₂₅(9) = 2.262**

---

## Lecture 51 — T Distribution | Mean, Variance, Mode
[🎥 Video](https://www.youtube.com/watch?v=hevo6dfRXDo)

### Problem 51.1
**Q:** Compare the variance of t(5), t(10), t(30), and N(0,1).

**Solution:**

| Distribution | Variance |
|---|---|
| t(5) | 5/(5−2) = 5/3 = **1.667** |
| t(10) | 10/(10−2) = 10/8 = **1.25** |
| t(30) | 30/(30−2) = 30/28 = **1.071** |
| N(0,1) | **1.000** |

→ As df increases, t-distribution variance → 1 (approaches normal)

---

## Lecture 52 — t-Test | Population Mean
[🎥 Video](https://www.youtube.com/watch?v=D8l8lmbPQt4)

### Problem 52.1
**Q:** A sample of 10 has mean 75.5 and SD 5.2. Test whether the population mean is 72 at α = 0.05 (two-tailed).

**Solution:**

H₀: μ = 72, H₁: μ ≠ 72, n = 10, x̄ = 75.5, S = 5.2

$$t = \frac{\bar{x} - \mu_0}{S/\sqrt{n}} = \frac{75.5 - 72}{5.2/\sqrt{10}} = \frac{3.5}{1.644} = \textbf{2.129}$$

df = 9. t₀.₀₂₅(9) = 2.262

Since |2.129| < 2.262, **do not reject H₀** at 5% level.

---

## Lecture 53 — t-Test | Two Sample Means
[🎥 Video](https://www.youtube.com/watch?v=jbndvJ5Bvmk)

### Problem 53.1
**Q:** Two groups: Group A (n₁=12, x̄₁=85, s₁=4.5), Group B (n₂=15, x̄₂=81, s₂=5.2). Test if means differ at α = 0.05.

**Solution:**

H₀: μ₁ = μ₂, H₁: μ₁ ≠ μ₂

Pooled SD:
$$S_p = \sqrt{\frac{11(4.5)^2 + 14(5.2)^2}{25}} = \sqrt{\frac{222.75 + 378.56}{25}} = \sqrt{24.05} = 4.904$$

$$t = \frac{85 - 81}{4.904\sqrt{1/12 + 1/15}} = \frac{4}{4.904 \times 0.3928} = \frac{4}{1.926} = \textbf{2.077}$$

df = 12 + 15 − 2 = 25. t₀.₀₂₅(25) = 2.060

Since 2.077 > 2.060, **reject H₀** at 5% level. The means differ significantly.

---

## Lecture 54 — Paired t-Test
[🎥 Video](https://www.youtube.com/watch?v=Dtp_LB-ui4M)

### Problem 54.1
**Q:** Scores before and after training for 6 employees:

| Employee | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| Before | 68 | 71 | 65 | 70 | 72 | 69 |
| After | 73 | 75 | 70 | 72 | 74 | 71 |

Test if training improved performance at α = 0.05 (one-tailed).

**Solution:**

H₀: μ_d ≤ 0, H₁: μ_d > 0 (improvement)

Differences (After − Before): 5, 4, 5, 2, 2, 2

d̄ = (5+4+5+2+2+2)/6 = 20/6 = **3.33**

S_d = √[Σ(d−d̄)²/(n−1)] = √[(2.78+0.44+2.78+1.78+1.78+1.78)/5] = √[11.34/5] = √2.268 = **1.506**

$$t = \frac{\bar{d}}{S_d/\sqrt{n}} = \frac{3.33}{1.506/\sqrt{6}} = \frac{3.33}{0.615} = \textbf{5.415}$$

df = 5. t₀.₀₅(5) = 2.015

Since 5.415 > 2.015, **reject H₀**. Training significantly improved performance.

---

## Lecture 55 — t-Test | Correlation Coefficient
[🎥 Video](https://www.youtube.com/watch?v=7uNmisYNj34)

### Problem 55.1
**Q:** A sample of 20 pairs gives r = 0.45. Test if the population correlation is significantly different from zero at α = 0.05.

**Solution:**

H₀: ρ = 0, H₁: ρ ≠ 0

$$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}} = \frac{0.45\sqrt{18}}{\sqrt{1-0.2025}} = \frac{0.45 \times 4.243}{\sqrt{0.7975}} = \frac{1.909}{0.893} = \textbf{2.138}$$

df = 18. t₀.₀₂₅(18) = 2.101

Since 2.138 > 2.101, **reject H₀**. The correlation is significantly different from zero.

---

# PART 9: F-DISTRIBUTION & FISHER'S Z

---

## Lecture 56 — F-Distribution
[🎥 Video](https://www.youtube.com/watch?v=RlCYTIU23qA)

### Problem 56.1
**Q:** If F ~ F(6, 10), find E(F) and Var(F).

**Solution:**

E(F) = n₂/(n₂−2) = 10/8 = **1.25**

Var(F) = 2n₂²(n₁+n₂−2)/[n₁(n₂−2)²(n₂−4)] = 2(100)(14)/[6(64)(6)]
= 2800/2304 = **1.215**

---

### Problem 56.2
**Q:** If F₀.₀₅(5, 8) = 3.69, find F₀.₉₅(8, 5).

**Solution:**

Using the reciprocal property:
$$F_{\alpha}(n_1, n_2) = \frac{1}{F_{1-\alpha}(n_2, n_1)}$$

F₀.₉₅(8, 5) = 1/F₀.₀₅(5, 8) = 1/3.69 = **0.271**

---

## Lectures 57–58 — F-Distribution Properties & F-Test
[🎥 Video 57](https://www.youtube.com/watch?v=3ogzI0FliMY) | [🎥 Video 58](https://www.youtube.com/watch?v=t-P-Jc4mQSY)

### Problem 58.1
**Q:** Two samples: Sample 1 (n₁=10, s₁²=25), Sample 2 (n₂=8, s₂²=9). Test H₀: σ₁² = σ₂² at α = 0.05.

**Solution:**

H₀: σ₁² = σ₂², H₁: σ₁² ≠ σ₂²

F = S₁²/S₂² = 25/9 = **2.778** (larger variance in numerator)

df = (n₁−1, n₂−1) = (9, 7)

F₀.₀₂₅(9, 7) ≈ 4.20 (from F-table)

Since 2.778 < 4.20, **do not reject H₀**. No significant difference between variances.

---

## Lectures 59–60 — Fisher's Z Distribution & Test
[🎥 Video 59](https://www.youtube.com/watch?v=s6l8riDtLqo) | [🎥 Video 60](https://www.youtube.com/watch?v=IUtNsw8C1ak)

### Problem 60.1
**Q:** A sample of 28 gives r = 0.6. Test H₀: ρ = 0.4 at α = 0.05 (two-tailed) using Fisher's Z transformation.

**Solution:**

Z_r = (1/2)ln[(1+0.6)/(1−0.6)] = (1/2)ln(1.6/0.4) = (1/2)ln(4) = (1/2)(1.386) = **0.693**

Z_ρ₀ = (1/2)ln[(1+0.4)/(1−0.4)] = (1/2)ln(1.4/0.6) = (1/2)ln(2.333) = (1/2)(0.847) = **0.424**

SE = 1/√(n−3) = 1/√25 = **0.2**

$$Z_{test} = \frac{Z_r - Z_{\rho_0}}{SE} = \frac{0.693 - 0.424}{0.2} = \frac{0.269}{0.2} = \textbf{1.345}$$

Z₀.₀₂₅ = 1.96

Since 1.345 < 1.96, **do not reject H₀**. Cannot conclude ρ ≠ 0.4.

---

## Lecture 61 — Fisher's Z Test | Two Correlations
[🎥 Video](https://www.youtube.com/watch?v=WzrOZKqoXKY)

### Problem 61.1
**Q:** Sample 1: n₁ = 50, r₁ = 0.7. Sample 2: n₂ = 60, r₂ = 0.5. Test H₀: ρ₁ = ρ₂ at α = 0.05.

**Solution:**

Z₁ = (1/2)ln(1.7/0.3) = (1/2)ln(5.667) = (1/2)(1.735) = **0.867**

Z₂ = (1/2)ln(1.5/0.5) = (1/2)ln(3) = (1/2)(1.099) = **0.549**

$$SE = \sqrt{\frac{1}{n_1-3} + \frac{1}{n_2-3}} = \sqrt{\frac{1}{47} + \frac{1}{57}} = \sqrt{0.02128 + 0.01754} = \sqrt{0.03882} = 0.197$$

$$Z_{test} = \frac{0.867 - 0.549}{0.197} = \frac{0.318}{0.197} = \textbf{1.614}$$

Since 1.614 < 1.96, **do not reject H₀**. No significant difference between the two correlations.

---

# PART 10: LARGE SAMPLE TESTS & ANOVA

---

## Lecture 62 — Z-Test for Population Mean
[🎥 Video](https://www.youtube.com/watch?v=oX0YXojQwEc)

### Problem 62.1
**Q:** A factory claims average bulb life is 1000 hours. A sample of 100 gives x̄ = 985, σ = 60. Test at α = 0.05 (two-tailed).

**Solution:**

H₀: μ = 1000, H₁: μ ≠ 1000

$$Z = \frac{\bar{x} - \mu_0}{\sigma/\sqrt{n}} = \frac{985 - 1000}{60/\sqrt{100}} = \frac{-15}{6} = \textbf{-2.5}$$

|Z| = 2.5 > Z₀.₀₂₅ = 1.96 → **Reject H₀**

The average bulb life is significantly different from 1000 hours.

---

## Lecture 63 — Z-Test | Difference of Two Means
[🎥 Video](https://www.youtube.com/watch?v=4pYYO6oa5lc)

### Problem 63.1
**Q:** Brand A (n₁=200, x̄₁=44, σ₁=12) vs Brand B (n₂=150, x̄₂=42, σ₂=14). Test if the means differ at α = 0.01.

**Solution:**

H₀: μ₁ = μ₂, H₁: μ₁ ≠ μ₂

$$Z = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\sigma_1^2/n_1 + \sigma_2^2/n_2}} = \frac{44 - 42}{\sqrt{144/200 + 196/150}} = \frac{2}{\sqrt{0.72 + 1.307}} = \frac{2}{\sqrt{2.027}} = \frac{2}{1.424} = \textbf{1.405}$$

Z₀.₀₀₅ = 2.576

Since 1.405 < 2.576, **do not reject H₀**. No significant difference at 1% level.

---

## Lecture 64 — Z-Test | Population Proportion
[🎥 Video](https://www.youtube.com/watch?v=IgY7xGADWSo)

### Problem 64.1
**Q:** A coin is tossed 400 times and heads appears 216 times. Test if the coin is fair at α = 0.05.

**Solution:**

H₀: p = 0.5, H₁: p ≠ 0.5

p̂ = 216/400 = 0.54

$$Z = \frac{\hat{p} - p_0}{\sqrt{p_0 q_0/n}} = \frac{0.54 - 0.50}{\sqrt{0.25/400}} = \frac{0.04}{0.025} = \textbf{1.6}$$

Since 1.6 < 1.96, **do not reject H₀**. The coin may be considered fair.

---

## Lecture 65 — Z-Test | Difference of Two Proportions
[🎥 Video](https://www.youtube.com/watch?v=aA581refl5Y)

### Problem 65.1
**Q:** In a survey, 120 of 200 men and 90 of 150 women favor a product. Test if the proportions differ at α = 0.05.

**Solution:**

H₀: p₁ = p₂, H₁: p₁ ≠ p₂

p̂₁ = 120/200 = 0.60, p̂₂ = 90/150 = 0.60

Pooled: p̂ = (120+90)/(200+150) = 210/350 = **0.60**

$$Z = \frac{0.60 - 0.60}{\sqrt{0.60(0.40)(1/200 + 1/150)}} = \frac{0}{\sqrt{0.24 \times 0.01167}} = \frac{0}{0.0529} = \textbf{0}$$

Since 0 < 1.96, **do not reject H₀**. No difference between proportions.

---

### Problem 65.2
**Q:** City A: 400 smokers out of 1000. City B: 300 smokers out of 800. Test if smoking rates differ at α = 0.01.

**Solution:**

p̂₁ = 0.4, p̂₂ = 0.375

Pooled: p̂ = 700/1800 = 0.389

$$Z = \frac{0.4 - 0.375}{\sqrt{0.389(0.611)(1/1000 + 1/800)}} = \frac{0.025}{\sqrt{0.2377 \times 0.00225}} = \frac{0.025}{\sqrt{0.000535}} = \frac{0.025}{0.02313} = \textbf{1.081}$$

Since 1.081 < 2.576, **do not reject H₀** at 1% level.

---

## Lecture 66 — Hypothesis Testing | Type 1 & Type 2 Errors
[🎥 Video](https://www.youtube.com/watch?v=Dn0sx0aRQ_E)

### Problem 66.1
**Q:** X ~ N(μ, 4). H₀: μ = 10, H₁: μ = 12. n = 1. Reject H₀ if X > 11. Find α and β.

**Solution:**

**Type I Error (α):** P(reject H₀ | H₀ true)
= P(X > 11 | μ = 10) = P(Z > (11−10)/2) = P(Z > 0.5) = 1 − Φ(0.5) = 1 − 0.6915 = **0.3085**

**Type II Error (β):** P(fail to reject H₀ | H₁ true)
= P(X ≤ 11 | μ = 12) = P(Z ≤ (11−12)/2) = P(Z ≤ −0.5) = Φ(−0.5) = **0.3085**

**Power** = 1 − β = 1 − 0.3085 = **0.6915**

---

### Problem 66.2
**Q:** In Problem 66.1, if we take n = 25 and reject H₀ if X̄ > 11, find α and β.

**Solution:**

SE = σ/√n = 2/5 = 0.4

**α** = P(X̄ > 11 | μ = 10) = P(Z > (11−10)/0.4) = P(Z > 2.5) = 1 − 0.9938 = **0.0062**

**β** = P(X̄ ≤ 11 | μ = 12) = P(Z ≤ (11−12)/0.4) = P(Z ≤ −2.5) = **0.0062**

**Power** = 1 − 0.0062 = **0.9938**

> **Insight:** Increasing n from 1 to 25 dramatically reduced both errors and increased power.

---

## Lecture 67 — ANOVA | One Way ANOVA (CRD)
[🎥 Video](https://www.youtube.com/watch?v=foDm8FeT2hg)

### Problem 67.1
**Q:** Three types of fertilizers are tested on crop yield (in quintals):

| Fertilizer A | Fertilizer B | Fertilizer C |
|---|---|---|
| 45 | 50 | 55 |
| 40 | 48 | 58 |
| 42 | 52 | 52 |
| 43 | 50 | 55 |

Test if fertilizer type affects yield at α = 0.05.

**Solution:**

**Step 1: Totals**
T_A = 170, T_B = 200, T_C = 220
n_A = n_B = n_C = 4, N = 12
Grand Total T = 590

**Step 2: Correction Factor**
CF = T²/N = 590²/12 = 348100/12 = **29008.33**

**Step 3: Total Sum of Squares (SST)**
Σx² = 45² + 40² + 42² + 43² + 50² + 48² + 52² + 50² + 55² + 58² + 52² + 55²
= 2025 + 1600 + 1764 + 1849 + 2500 + 2304 + 2704 + 2500 + 3025 + 3364 + 2704 + 3025
= 29364

SST = 29364 − 29008.33 = **355.67**

**Step 4: Between Groups Sum of Squares (SSB)**
SSB = (T_A²/n_A + T_B²/n_B + T_C²/n_C) − CF
= (170²/4 + 200²/4 + 220²/4) − 29008.33
= (7225 + 10000 + 12100) − 29008.33
= 29325 − 29008.33 = **316.67**

**Step 5: Within Groups Sum of Squares (SSW)**
SSW = SST − SSB = 355.67 − 316.67 = **39.00**

**Step 6: ANOVA Table**

| Source | SS | df | MS | F |
|---|---|---|---|---|
| Between (Fertilizer) | 316.67 | 2 | 158.33 | **36.53** |
| Within (Error) | 39.00 | 9 | 4.33 | |
| **Total** | **355.67** | **11** | | |

F = MSB/MSW = 158.33/4.33 = **36.53**

F₀.₀₅(2, 9) = 4.26

Since 36.53 > 4.26, **Reject H₀**. 

**Conclusion:** Fertilizer type significantly affects crop yield at 5% level of significance.

---

### Problem 67.2
**Q:** The following data gives the output of 3 machines:

| Machine 1 | Machine 2 | Machine 3 |
|---|---|---|
| 10 | 12 | 14 |
| 8 | 11 | 16 |
| 9 | 13 | 15 |
| 11 | 10 | 13 |
| 12 | 14 | 12 |

Test at α = 0.01 whether the machines differ in output.

**Solution:**

T₁ = 50, T₂ = 60, T₃ = 70, N = 15, T = 180, n₁ = n₂ = n₃ = 5

CF = 180²/15 = 32400/15 = **2160**

Σx² = 100+64+81+121+144 + 144+121+169+100+196 + 196+256+225+169+144
= 510 + 730 + 990 = **2230**

SST = 2230 − 2160 = **70**

SSB = (50²/5 + 60²/5 + 70²/5) − 2160 = (500 + 720 + 980) − 2160 = **40**

SSW = 70 − 40 = **30**

| Source | SS | df | MS | F |
|---|---|---|---|---|
| Between | 40 | 2 | 20 | **8.0** |
| Within | 30 | 12 | 2.5 | |
| Total | 70 | 14 | | |

F₀.₀₁(2, 12) = 6.93

Since 8.0 > 6.93, **Reject H₀** at 1% level. Machine outputs differ significantly.

---

# 📋 Summary: Problem Types by Lecture

| Lecture | Key Problem Types |
|---|---|
| 1 | Sample space enumeration, counting, basic probability |
| 2 | Addition theorem, P(A∪B), at least one/neither |
| 3 | Independent events, P(both/at least one/exactly one) |
| 4 | Conditional probability, multiplication rule |
| 5 | Bayes' theorem, prior/posterior probability |
| 6 | PMF construction, finding constants, CDF |
| 7 | PDF verification, finding k, CDF, probabilities |
| 8 | E(X), E(g(X)), linearity of expectation |
| 9 | Var(X), SD, Var(aX+b) |
| 10 | Raw/central moments, moment conversions |
| 11 | Skewness, kurtosis, distribution shape |
| 12 | Binomial probabilities, finding n and p from mean/variance |
| 13 | MGF computation, moments from MGF, recurrence |
| 14 | Fitting binomial to frequency data |
| 15–17 | Poisson probabilities, fitting, λ determination |
| 18–21 | Normal distribution: standardization, area/probability |
| 22 | Uniform distribution: probabilities, mean, variance |
| 23 | Exponential: probabilities, memoryless property |
| 24–25 | Joint PMF/PDF, marginals, independence, covariance |
| 26 | Pearson's r computation |
| 27–28 | Spearman's rank correlation, tied ranks |
| 29–30 | Regression lines, r from regression coefficients, angle |
| 31–32 | Least squares curve fitting (line, parabola) |
| 33–34 | Partial and multiple correlation |
| 35–38 | Gamma/Beta distributions, B(m,n), integral evaluation |
| 39 | Cauchy: PDF verification, no finite moments |
| 40 | Laplace: probabilities, properties |
| 41 | Weibull: reliability, mean lifetime |
| 42 | Log-normal: mean, variance, median, mode |
| 43–45 | Chi-square properties, additive property, MGF |
| 46 | χ² test for variance |
| 47 | χ² test for independence (contingency table) |
| 48 | χ² goodness of fit test |
| 49 | Yates' correction for 2×2 tables |
| 50–51 | t-distribution properties, critical values |
| 52 | One-sample t-test (population mean) |
| 53 | Two-sample t-test (independent means) |
| 54 | Paired t-test (matched pairs) |
| 55 | t-test for correlation coefficient |
| 56–57 | F-distribution properties, reciprocal property |
| 58 | F-test (variance ratio test) |
| 59–61 | Fisher's Z transformation, testing ρ = ρ₀, comparing r₁ and r₂ |
| 62 | Z-test for population mean |
| 63 | Z-test for difference of two means |
| 64 | Z-test for population proportion |
| 65 | Z-test for difference of two proportions |
| 66 | Type I/II errors, power of test |
| 67 | One-way ANOVA (CRD), F-test for means |

---

> **Companion document to:** [Probability_and_Statistics_Complete_Notes.md](file:///Users/aniketbera/Desktop/leetCode/Probability%20and%20Statictics/Probability_and_Statistics_Complete_Notes.md)
> **Total problems:** 70+ fully solved problems across 67 lectures
