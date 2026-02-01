

# 📘 Rigorous Mathematical Formalization of the F5 Game  
### *(KSZ Five‑Five Card Model)*

<div align="center">

<img src="icons/f5_icon.png" width="140">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
GitHub stars [(github.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fgithub.com%2FGuyKaptue%2FF5-Game-Formalization%2Fstargazers")
GitHub issues [(github.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fgithub.com%2FGuyKaptue%2FF5-Game-Formalization%2Fissues")
[`https://www.linkedin.com/in/guy-michel-kaptue-tabeu/`](https://www.linkedin.com/in/guy-michel-kaptue-tabeu/)

**A rigorous mathematical formalization of the KSZ Five‑Five Card Game, integrating probability theory, sequential game analysis, and AI‑ready structures.**

`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

<img src="icons/fivefive.png" width="300">

</div>

---

## 📑 Table of Contents

| Section | Description |
|--------|-------------|
| [Introduction](#introduction) | Overview of the F5 Game and its mathematical significance |
| [Formal Definition](#formal-definition-of-the-f5-game) | Deck, players, objectives, and special rules |
| [Mathematical Framework](#mathematical-framework) | Sets, game state, compatibility, winner determination |
| [Theorems and Proofs](#theorems-and-proofs) | Winner uniqueness, stake conservation, probability bounds |
| [Structural Properties](#structural-properties) | Determinism, imperfect information, finiteness |
| [Probabilistic Analysis](#probabilistic-analysis) | Hand distribution, Cora probability, Markov process |
| [Balancing Analysis](#balancing-analysis) | Optimal Cora multiplier, Gini coefficient, entropy |
| [Complexity Theorems](#complexity-theorems) | Game tree size, algorithmic complexity |
| [Probability Laws](#probability-laws) | Kaptue‑F5 Law, fairness, zero‑sum property |
| [Exercises](#exercises-and-applications) | Basic to advanced exercises |
| [Repository Structure](#repository-structure) | Full directory layout |
| [Citation](#citation) | BibTeX reference |
| [License](#license) | MIT License |
| [Contact](#contact) | Author information |

---

## 🃏 Introduction

The **F5 Game** is a **finite, sequential, imperfect‑information card game** played over five rounds.  
This work provides the first **complete mathematical formalization** of the KSZ Five‑Five model, combining:

- Multivariate hypergeometric distributions  
- Non‑stationary Markov processes  
- Deterministic payoff functions  
- Game‑theoretic reasoning  
- AI simulation structures  

The result is a **rigorous, reproducible, and simulation‑ready** mathematical foundation.

---

## 📐 Formal Definition of the F5 Game

- **Deck:** 32 cards (values 3–10 across four suits)  
- **Players:** 2–4  
- **Objective:** Win the fifth round with amplified Cora multiplier  
- **Special Rules:** Suit obligations, Cora system, immediate victory conditions  

Full formal definition: **`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`**

---

## 🧮 Mathematical Framework

- **Value Set:** \( V = \{3,4,\dots,10\} \)  
- **Suit Set:** \( S = \{\heartsuit, \clubsuit, \diamondsuit, \spadesuit\} \)  
- **Game State:**  
  \[
  G(t) = (H(t), r(t), c(t), s_r, P(t), \sigma, \text{direction}, d, M_0, \text{Disq}(t))
  \]
- **Compatibility:** Suit‑obligation and legal move structure  
- **Winner Determination:** Unique winner per round, Cora‑weighted final payoff  

---

## 📚 Theorems and Proofs

Highlights include:

- **Winner Uniqueness** (Theorem 4.6)  
- **Stake Conservation** (Theorem 4.10)  
- **Information‑Theoretic Bound:** \( n \leq 4 \) players  
- **Immediate Victory Probabilities:**  
  - Hand sum ≤ 21: ~1.23%  
  - Triple 7: ~0.75%  

---

## 🧱 Structural Properties

- **Deterministic** given initial distribution and choices  
- **Imperfect Information** (private hands)  
- **Finite Game Tree** (acyclic, bounded depth)  

---

## 🎲 Probabilistic Analysis

- **Expected Hand Sum:** \( \mathbb{E}[\Sigma(h)] = 32.5 \)  
- **Variance:** \( \approx 22.86 \)  
- **Cora Probability:** Hypergeometric distribution  
- **Markovian Evolution:** Non‑stationary chain across rounds  

---

## ⚖️ Balancing Analysis

- **Optimal Cora Multiplier:** \( m^* \approx 4.33 \)  
- **Gini Coefficient:** \( G_V \approx 0.202 \)  
- **Shannon Entropy:** \( H(h) \approx 17.62 \) bits  

---

## 🧩 Complexity Theorems

- **Game Tree Size:** ≤ \( 2.12 \times 10^{11} \) nodes (4 players)  
- **Simulation Complexity:** \( \mathcal{O}(5n) \)  
- **Dealing Procedure:** \( \mathcal{O}(1) \)  

---

## 📏 Probability Laws

### **Kaptue‑F5 Law**

\[
P(\Delta, W, R, H) = P(\Delta \mid W, H)\, P(W \mid R, H)\, P(R \mid H)\, P(H)
\]

- **Zero‑Sum:** \( \sum_i \delta_i = 0 \)  
- **Ex‑Ante Fairness:** \( \mathbb{E}[\delta_i] = 0 \)  

---

## 📝 Exercises and Applications

- **Basic:** Hand sum, legality checks  
- **Intermediate:** Winner determination  
- **Advanced:** Monte Carlo estimation, Markov verification  
- **Synthesis:** Full game simulation  

---

## 📁 Repository Structure

This repository contains the full LaTeX source and compiled PDF of the F5 Game formalization.

```
f5-game-formalization/
│
├── main.tex                # Main LaTeX document (entry point)
├── main.pdf                # Compiled full paper
├── preamble.tex            # Global LaTeX configuration
├── references.bib          # Bibliography
├── README.md               # Project documentation
│
├── chapters/               # All content chapters
│   ├── 00_introduction.tex
│   ├── 01_definition_context.tex
│   ├── 02_formal_definitions.tex
│   ├── 03_theorems_proofs.tex
│   ├── 04_structural_properties.tex
│   ├── 05_probabilistic_analysis.tex
│   ├── 06_balancing_analysis.tex
│   ├── 07_complexity_theorems.tex
│   ├── 08_probability_laws.tex
│   ├── 09_exercises_applications.tex
│   ├── 10_appendix.tex
│   └── conclusion.tex
│
└── icons/                  # Logos and figures
    ├── f5_icon.png
    └── fivefive.png
```

---

## 📚 Citation

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

## 📄 License

This project is licensed under the **MIT License**.  
See the full text in **LICENSE**.

---

## 📬 Contact

**Guy M. Kaptue T.**  
📧 Email: guykaptue24@gmail.com  
🌐 GitHub: [https://github.com/GuyKaptue](https://github.com/GuyKaptue)  
🔗 LinkedIn: [https://www.linkedin.com/in/guy-michel-kaptue-tabeu/](https://www.linkedin.com/in/guy-michel-kaptue-tabeu/)

---

© 2026 Guy M. Kaptue T. All rights reserved.

---
