# From PD to Pareto – Efficient Credit Portfolios in Python 📈

This repository contains a small Python demo that accompanies the article:

> **"From PD to Pareto: Turning Credit Risk Models into Efficient Portfolio Decisions"**

It shows how to build an efficient frontier in **Expected Loss vs Return** space for a synthetic credit portfolio, under realistic constraints on **stress losses**, **capital usage** and **concentration**.

---

## 🧩 What this project does

- Generates a synthetic set of **credit segments** with:
  - base and stressed **PD**,
  - **LGD**,
  - **risk weights** (capital intensity),
  - **country** and **PD band** (Low/Medium/High).
- Defines a **linear program (LP)** that:
  - maximises expected return,
  - caps base and stressed expected loss,
  - enforces a capital budget,
  - enforces concentration limits (High PD and per country).
- Traces the **efficient frontier** in EL–Return space by solving the LP for different EL caps.
- Compares **random feasible portfolios** vs the efficient frontier to visualise **dominated vs efficient** positions.

---

## 📁 Repository structure

```text
from-pd-to-pareto/
├─ README.md
├─ requirements.txt
├─ src/
│  └─ pareto_optimization.py
└─ notebooks/
   └─ pareto_credit_portfolio.ipynb
