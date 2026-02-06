# 🚀 A/B Testing Framework for E-Commerce
**Case Study: Croatian E-Commerce Platform Analysis**

---

## 1. Introduction: The Business Problem

### 1.1 Why A/B Testing Matters
E-commerce companies face a fundamental challenge: **How do we know if changing our website will increase revenue?**

Traditional approaches often rely on:
* **HiPPO:** Highest Paid Person's Opinion.
* **Gut Feelings:** "I think users will like this."
* **Observational Analysis:** Comparing before/after metrics (often confounded by seasonality or external events).

**A/B Testing** (Randomized Controlled Trials) provides a scientific alternative to establish **causality**. By randomly assigning users to a **Control (A)** or **Treatment (B)** group, we ensure that observed differences are attributed solely to the change itself.

### 1.2 Case Study Context: Croatian E-Commerce Platform
This project analyzes an online retailer's experiment to simplify their checkout process.
* **Timeline:** March – June 2021
* **Sample Size:** 102,000+ user sessions
* **Geography:** Zagreb, Split, Rijeka, Osijek
* **Device Split:** Mobile (60%), Desktop (35%), Tablet (5%)

---

## 2. Experimental Validation (Current Progress)
Before jumping into statistical results, we must ensure the "integrity" of the experiment. My framework in `src/validation/` checks for:
1.  **Sample Ratio Mismatch (SRM):** Is the 50/50 split actually 50/50?
2.  **User Integrity:** Checking for duplicate users across groups.
3.  **Covariate Balance:** Ensuring segments (Mobile vs Desktop) are distributed evenly.

---

## 3. Project Structure
```text
Project-DEC/
├── data/raw/               # Raw experimental data (CSV)
├── src/
│   ├── validation/         # Validation Framework & Notebook
│   └── statistical_analysis/ # Hypothesis Testing (Next Step)
└── README.md
