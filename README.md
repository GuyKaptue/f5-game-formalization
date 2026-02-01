

<div align="center">


<img src="icons/f5_icon.png" width="140">

# Rigorous Mathematical Formalization of the F5 Game (KSZ Five-Five Card Model)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/GuyKaptue/F5-Game-Formalization.svg)](https://github.com/GuyKaptue/F5-Game-Formalization/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/GuyKaptue/F5-Game-Formalization.svg)](https://github.com/GuyKaptue/F5-Game-Formalization/issues)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/guy-michel-kaptue-tabeu/)

> **A rigorous mathematical formalization of the KSZ Five-Five Card Game, integrating probability theory, sequential game analysis, and AI simulation-ready frameworks.**

[![Read PDF](https://img.shields.io/badge/📄-Read_Full_Paper-blue?style=for-the-badge)](main.pdf)


<img src="icons/fivefive.png" width="300">
</div>

---

## Table of Contents

| Section                                                               | Description                                                                         |
| --------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [Introduction](#introduction)                                         | Overview of the F5 Game and its mathematical significance                           |
| [Formal Definition of the F5 Game](#formal-definition-of-the-f5-game) | Deck, players, objectives, and special rules                                        |
| [Mathematical Framework](#mathematical-framework)                     | Fundamental sets, game state, compatibility, and winner determination               |
| [Theorems and Proofs](#theorems-and-proofs)                           | Key results including winner uniqueness, stake conservation, and probability bounds |
| [Structural Properties](#structural-properties)                       | Determinism, imperfect information, finiteness                                      |
| [Probabilistic Analysis](#probabilistic-analysis)                     | Hand sum distribution, Cora probability, Markovian process                          |
| [Balancing Analysis](#balancing-analysis)                             | Optimal Cora multiplier, Gini coefficient, Shannon entropy                          |
| [Complexity Theorems](#complexity-theorems)                           | Game tree size, algorithmic complexity, dealing procedure                           |
| [Probability Laws](#probability-laws)                                 | Kaptue-F5 Law, zero-sum property, ex-ante fairness                                  |
| [Exercises and Applications](#exercises-and-applications)             | Basic, intermediate, advanced, and synthesis exercises                              |
| [Conclusion](#conclusion)                                             | Summary, AI applications, and stochastic modeling insights                          |
| [Files in This Repository](#files-in-this-repository)                 | Repository structure, PDF, LaTeX sources, figures, and simulations                  |
| [Citation](#citation)                                                 | BibTeX reference for scholarly use                                                  |
| [License](#license)                                                   | MIT License                                                                         |
| [Contact](#contact)                                                   | Author contact information                                                          |

---

## Introduction

The **F5 Game** is a **finite, sequential game of imperfect information**, where players manage a hand of five cards over five rounds. It introduces the **Kaptue-F5 Law**, a hierarchical probabilistic framework combining:

* Multivariate hypergeometric distributions
* Non-stationary Markov processes
* Deterministic payoff functions

This formalization transforms oral rules into a **mathematically rigorous, AI-ready model**.

---

## Formal Definition of the F5 Game

* **Deck:** 32 cards (values 3–10, four suits)
* **Players:** 2–4 participants
* **Objective:** Win the fifth round with amplified Cora multiplier
* **Special Rules:** Suit obligations, Cora system, immediate victory (hand sum ≤ 21 or triple 7)

Full definition: [main.pdf](main.pdf)

---

## Mathematical Framework

* **Fundamental Sets:** ( V = {3, 4, \dots, 10} ), ( S = {\heartsuit, \clubsuit, \diamondsuit, \spadesuit} )
* **Game State:** ( G(t) = (H(t), r(t), c(t), s_r, P(t), \sigma, \text{direction}, d, M_0, \text{Disq}(t)) )
* **Compatibility & Playability:** Suit obligations, legal moves
* **Winner Determination:** Unique winner per round, final gains multiplied by Cora

---

## Theorems and Proofs

* **Winner Uniqueness (Theorem 4.6)**
* **Stake Conservation (Theorem 4.10)**
* **Information-Theoretic Bound:** ( n \leq 4 ) players (Theorem 4.2)
* **Probability of Immediate Victory:**

  * Hand sum ≤ 21: ( P \approx 1.23% )
  * Triple 7: ( P \approx 0.75% )

---

## Structural Properties

* **Determinism:** Conditional on initial distribution and player choices
* **Imperfect Information:** Players know only their hand and played cards
* **Finiteness:** Game tree is finite and acyclic

---

## Probabilistic Analysis

* **Hand Sum Distribution:** ( \mathbb{E}[\Sigma(h)] = 32.5 ), ( \text{Var}[\Sigma(h)] \approx 22.86 )
* **Cora Probability:** Hypergeometric distribution for value-3 cards
* **Markovian Process:** Rounds evolve as non-stationary Markov chain

---

## Balancing Analysis

* **Optimal Cora Multiplier:** ( m^* \approx 4.33 ) (attractiveness factor ( k = 1.5 ))
* **Gini Coefficient:** ( G_V \approx 0.202 ) (moderate inequality)
* **Shannon Entropy:** ( H(h) \approx 17.62 ) bits (high strategic diversity)

---

## Complexity Theorems

* **Game Tree Size:** ≤ ( 2.12 \times 10^{11} ) nodes (4 players)
* **Algorithmic Complexity:** ( \mathcal{O}(5n) ) for full simulation
* **Dealing Procedure:** ( \mathcal{O}(1) )

---

## Probability Laws

**Kaptue-F5 Law:**

[
P(\Delta, W, R, H) = P(\Delta \mid W, H) \cdot P(W \mid R, H) \cdot P(R \mid H) \cdot P(H)
]

* **Zero-Sum Property:** ( \sum_{i=1}^n \delta_i = 0 )
* **Ex-Ante Fairness:** ( \mathbb{E}[\delta_i] = 0 )

---

## Exercises and Applications

* **Basic:** Sum calculation, legality verification
* **Intermediate:** Winner determination, gain calculation
* **Advanced:** Monte Carlo estimation, Markov property verification
* **Synthesis:** Full game simulation and strategic analysis

---

## Conclusion

The F5 Game is a **rich mathematical object**, suitable for:

* AI training
* Probabilistic simulations
* Game-theoretic research

The **Kaptue-F5 Law** provides a **unified framework** for strategy evaluation and stochastic modeling.

---

## Files in This Repository

| File                 | Description                                  |
| -------------------- | -------------------------------------------- |
| [main.pdf](main.pdf) | Full paper (v4.0, January 2026)              |

---

## Citation

```bibtex
@misc{kaptue2026f5,
  author = {Guy M. Kaptue T.},
  title = {Rigorous Mathematical Formalization of the F5 Game (KSZ Five-Five Card Model)},
  year = {2026},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/GuyKaptue/F5-Game-Formalization}}
}
```

---

## License

This repository is licensed under the [MIT License](LICENSE).

---

## Contact

**Guy M. Kaptue T.**
[Email](mailto:guy.kaptue@email.com) | [GitHub](https://github.com/GuyKaptue) | [LinkedIn](https://www.linkedin.com/in/guy-michel-kaptue-tabeu/)

---

© 2026 Guy M. Kaptue T. All rights reserved.

---
