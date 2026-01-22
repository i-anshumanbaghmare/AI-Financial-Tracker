# AI Financial Tracker 💰

*A Personal Finance Intelligence System*

## Overview

**AI Financial Tracker** is an **AI-driven personal finance intelligence system** that transforms **unstructured natural language inputs** into **structured financial data** and then applies **statistical modeling and rule-based optimization** to generate **actionable financial recommendations**.

Unlike traditional expense trackers that rely on manual form filling, this system reduces user friction by allowing users to log transactions in **natural language**, while still producing **analytics-ready, reliable data** for forecasting, optimization, and decision support.

> **Problem Statement**
> Most personal finance tools suffer from poor user adoption due to manual data entry and rigid interfaces. This project explores how lightweight NLP, structured storage, and applied statistical models can be combined to build a low-friction yet intelligent financial assistant.

---

## System Architecture (High-Level)

The system is intentionally designed as a **layered architecture**, mirroring real-world data systems:

1. **User Interaction Layer**
   Flask-based web application for input and visualization

2. **NLP Ingestion Layer**
   Rule-based NLP pipeline to convert free-text inputs into structured transactions

3. **Data Validation & Storage Layer**
   Normalized SQLite database with transaction-level integrity checks

4. **Financial Intelligence Modeling Layer**
   Statistical forecasting, probabilistic simulations, and optimization heuristics

5. **Recommendation & Decision-Support Layer**
   Budget insights, savings feasibility, debt payoff strategies, and risk-aware guidance

This separation ensures **modularity, interpretability, and maintainability**.

---

## Project Capabilities

The system functions as a **personalized financial assistant** that enables users to:

* Log expenses and income using **natural language**
* Automatically **categorize transactions** using fuzzy matching and hierarchical categories
* Track historical spending and income trends
* Generate **data-driven financial insights** using statistical and rule-based models
* Receive **transparent, explainable recommendations** rather than black-box predictions

---

## Core Features 🛠️

### 1. Natural Language Transaction Processing

* Accepts inputs like:
  *“Paid ₹1500 for groceries yesterday”*
* Extracts:

  * Amount
  * Category
  * Date
  * Description
* Supports **Indian financial context and terminology**
* Handles noisy and partial inputs with fallbacks

---

### 2. Transaction Management

* Expense and income tracking
* Automated categorization
* Historical transaction retrieval
* SQLite-backed persistence with normalized schema

---

### 3. Financial Intelligence Layer (Key Differentiator)

This layer moves the project beyond tracking into **applied financial modeling**.

#### 📈 Budget Forecasting

* Rolling moving average on monthly expenses
* Confidence intervals derived from historical variance
* Designed for stability and interpretability over overfitting

#### 💼 Investment Strategy Advisor

* Rule-based asset allocation using:

  * Risk profile (conservative / moderate / aggressive)
  * Investment horizon
* Emphasizes transparency and real-world financial reasoning

#### 🎯 Savings Goal Probability Estimation

* Monte Carlo simulations to estimate success probability
* Accounts for:

  * Return uncertainty
  * Income constraints
* Outputs **probability**, not just point estimates

#### 🏦 Debt Payoff Optimization

* Supports:

  * Avalanche (highest interest first)
  * Snowball (lowest balance first)
* Simulates month-by-month repayment
* Computes total payoff duration and interest cost

#### 🚨 Emergency Fund Advisor

* Estimates emergency fund range using expense distributions
* Adjusts recommendations based on:

  * Income stability
  * Number of dependents
* Quantifies sufficiency using probabilistic reasoning

> **Design Choice**
> Not every problem is solved using machine learning. For several components, statistical and rule-based models were intentionally chosen for **interpretability, robustness, and domain alignment**.

---

## Technical Stack ⚙️

* **Backend**: Python, Flask, Regular Expressions
* **Data Processing**: Pandas, NumPy, SciPy
* **Database**: SQLite
* **NLP**: Rule-based parsing + fuzzy matching
* **Testing**: Unit tests for parsing and models
* **Logging**: Structured logging and error handling

---

## Repository Structure 📂

```
AI_Financial_Tracker/
├── app.py                  # Flask web application
├── main.py                 # Application entry logic
├── financial_tracker.db    # SQLite database
├── config.ini              # Configuration
│
├── core/
│   ├── models.py           # Financial intelligence models
│   ├── database.py         # Database operations
│   ├── categories.py       # Category hierarchy & matching
│   ├── nlp_parser.py       # NLP transaction parsing
│   └── __init__.py
│
├── templates/
│   └── index.html          # Web interface
│
└── tests/
    ├── test_parser.py      # NLP tests
    ├── test_models.py      # Financial model tests
    └── __init__.py
```

---

## Key Modules 🔍

### `nlp_parser.py`

* Rule-based parsing of unstructured text
* Entity extraction:

  * Amount
  * Date
  * Category
* Handles multi-transaction and ambiguous inputs

### `categories.py`

* 50+ Indian-specific expense and income categories
* Hierarchical structure
* Fuzzy keyword matching for robustness

### `models.py`

* Moving-average budget forecasting
* Probabilistic savings goal modeling
* Investment allocation strategies
* Debt payoff optimization algorithms
* Emergency fund risk estimation

---

## Sample Categories

### Expense Categories

* **Food**: groceries, dhaba, kirana, panipuris, sweets
* **Transport**: auto, metro, fuel
* **Healthcare**: doctor, pharmacy, ayurveda
* **Debt**: EMI, credit card
* **Education**: tuition, coaching
* **Miscellaneous**: festivals, legal, pet care

### Income Categories

* **Employment**: salary, bonus
* **Business**: freelance, shop income
* **Investments**: dividends, mutual funds
* **Government**: refund, pension

---

## Installation 🛠️

```bash
git clone https://github.com/yourusername/AI_Financial_Tracker.git
cd AI_Financial_Tracker
python -m venv myenv
source myenv/bin/activate  # Linux/Mac
myenv\Scripts\activate     # Windows
pip install -r requirements.txt
```

Access the web interface at:

```
http://localhost:5000
```

---

## Design Principles Emphasized

* Separation of concerns
* Interpretable models over unnecessary ML
* Robust fallbacks for sparse data
* Probabilistic reasoning under uncertainty
* Real-world financial domain alignment

---

## Future Enhancements 🚀

* Voice-based transaction input
* SMS / email transaction parsing
* Banking and UPI API integration (mock/real)
* Multi-user support
* Exportable financial reports

---

## Author 👤

**Anshuman Baghamare**
B.Tech – Artificial Intelligence & Data Science
Interested in applied AI, data-driven decision systems, and intelligent assistants.

---
