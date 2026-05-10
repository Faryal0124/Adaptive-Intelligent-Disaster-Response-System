
# 🚑 AIDRA — Adaptive Intelligent Disaster Response Agent

> A hybrid AI-powered disaster rescue system integrating Search Algorithms, CSP, Machine Learning, and Fuzzy Logic for intelligent emergency response.

# 📌 Overview

AIDRA (Adaptive Intelligent Disaster Response Agent) is an AI-based disaster management system designed to simulate intelligent rescue operations in a dynamic disaster environment.

The system operates on a **6×6 disaster grid** containing:
- Victims
- Hospitals
- Dangerous zones
- Road blockages
- Rescue teams
- Ambulances

AIDRA intelligently:
- Prioritizes victims
- Allocates rescue resources
- Plans optimal rescue routes
- Predicts survival probability
- Handles uncertainty using fuzzy logic
- Dynamically replans paths during aftershocks

---

# 🎯 Objectives

The project demonstrates practical implementation of major Artificial Intelligence concepts including:

- Search Algorithms
- Constraint Satisfaction Problems (CSP)
- Machine Learning
- Fuzzy Logic
- Dynamic Replanning
- Intelligent Decision Making

---

# 🧠 AI Techniques Used

| AI Component | Technique Implemented |
|-------------|----------------------|
| Route Planning | BFS, A*, Greedy BFS, Hill Climbing |
| Resource Allocation | CSP + MRV Heuristic |
| Survival Prediction | kNN + Gaussian Naive Bayes |
| Uncertainty Handling | Fuzzy Logic |
| Dynamic Adaptation | Real-time A* Replanning |
| Visualization |  Matplotlib |

---

# ⚡ Key Features

## ✅ Intelligent Route Planning
Implements and compares multiple search algorithms:
- Breadth First Search (BFS)
- A* Search
- Greedy Best First Search
- Hill Climbing

---

## ✅ CSP-Based Resource Allocation
Uses Constraint Satisfaction Problem techniques to assign:
- 5 victims
- 2 ambulances
- 1 rescue team

### Hard Constraint
Each ambulance can carry:

> **MAXIMUM 1 critical patient**

The MRV (Minimum Remaining Values) heuristic is used for faster allocation.

---

## ✅ Machine Learning Survival Prediction

Predicts whether a victim is:
- Likely to survive
- At high risk

### Features Used
- Number of dangerous cells on path
- Distance to nearest hospital
- Severity score
- Estimated response time

### ML Models
- k-Nearest Neighbors (k=5)
- Gaussian Naive Bayes

### Dataset
- 550+ generated disaster rescue samples
- 80/20 train-test split

---

## ✅ Fuzzy Logic Decision System

Handles uncertainty in disaster environments.

### Risk Levels
- LOW
- MEDIUM
- HIGH

### Blockage Probability Calculation
Based on:
- Aftershock impact (40%)
- Fire spread risk (60%)

---

## ✅ Dynamic Replanning

If roads become blocked during rescue:
- Current route is invalidated
- A* search is re-executed
- New optimal route is generated in real-time


---

# 🏆 Results

| Metric | Result |
|-------|--------|
| Victims Saved | 5/5 (100%) |
| Critical Constraint | Satisfied |
| A* Cost Improvement | 18 cost units saved |
| MRV Speed Improvement | 2.6× faster |
| Naive Bayes Accuracy | 85% |
| Naive Bayes F1 Score | 0.86 |
| CSP Backtracking | 0 |
| Dynamic Replanning | Successful |

---

# 📊 KPIs Generated

The system automatically generates performance analytics including:

1. Victim Save Rate
2. BFS vs A* Cost Comparison
3. Danger Exposure Analysis
4. ML Model Performance Metrics
5. CSP Backtracking Comparison
6. Survival Probability per Victim
7. Rescue Efficiency Dashboard

Generated output:
```bash
aidra_kpi_dashboard.png
```

---



# 📁 Project Structure

```bash
AIDRA/
│
├── main.py
├── agent.py
├── search.py
├── simulation.py
├── grid.py
├── visualize.py
├── disaster_rescue_dataset.csv
│
└── README.md
```

---

# 📂 File Descriptions

| File | Purpose |
|------|---------|
| `main.py` | Main entry point |
| `agent.py` | AI agent, CSP, ML, fuzzy logic |
| `search.py` | Search algorithm implementations |
| `simulation.py` | Rescue simulation engine |
| `grid.py` | Disaster environment generation |
| `visualize.py` | KPI graphs and charts |
| `disaster_rescue_dataset.csv` | ML training dataset |

---

# ⚙️ Installation

## Prerequisites

Install required Python libraries:

```bash
pip install numpy scikit-learn matplotlib
```

---


## Run Terminal Version

```bash
python main.py
```

---

# 🔍 Search Algorithms Explained

## Breadth First Search (BFS)
- Finds shortest path in steps
- Ignores danger levels
- Guarantees shortest unweighted route

---

## A* Search
- Uses:
  - Path cost
  - Heuristic distance
- Avoids dangerous zones
- Produces optimal weighted path

---

## Greedy Best First Search
- Uses heuristic only
- Faster but not always optimal

---

## Hill Climbing
- Local search strategy
- Can get stuck in local optima

---

# 🧩 CSP with MRV Heuristic

The CSP system allocates victims while satisfying constraints.

### Standard Backtracking
- Assigns sequentially
- Slower search

### MRV Heuristic
- Selects least-loaded ambulance first
- Reduces search complexity
- Achieved:
```bash
2.6× faster execution
```

---

# 🤖 Machine Learning Details

## Models Compared

| Model | Accuracy | F1 Score |
|------|----------|----------|
| kNN | 78% | 0.78 |
| Naive Bayes | 85% | 0.86 |

---

## Why Naive Bayes Performed Better
- Better handling of probabilistic relationships
- More stable on generated disaster data
- Faster prediction time

---

# 🌫️ Fuzzy Logic System

The fuzzy module estimates:
- Route risk
- Probability of blockage

### Example
```text
Danger Ratio → HIGH Risk
Aftershock + Fire → 72% blockage probability
```

---

# 🔄 Dynamic Replanning Example

```text
Event: Road blocked at (2,1)
Reason: Aftershock detected
Action: Replanning A* route from current position
```

---

# ✅ CCP Requirements Fulfilled

| Requirement | Status |
|-------------|--------|
| 4 Search Algorithms | ✅ |
| CSP + Heuristic | ✅ |
| 2 ML Models | ✅ |
| Fuzzy Logic | ✅ |
| Dynamic Replanning | ✅ |
| Decision Logging | ✅ |
| KPI Visualization | ✅ |

---

# 🛠️ Technologies Used

- Python 3.8+
- scikit-learn
- NumPy
- Matplotlib
- Tkinter

---

# 👥 Team Contributions

| Team Member | Responsibilities |
|-------------|-----------------|
| Member 1 | Search algorithms, CSP, GUI, simulation |
| Member 2 | ML models, dataset generation, fuzzy logic, visualization |

---

# 📚 Academic Purpose

This project was developed as part of:

### Course:
**Artificial Intelligence (AIC-201)**

### Project Type:
Course Completion Project (CCP)

---

# 📜 License

This project is developed strictly for:

> Educational and Academic Purposes Only

---

# ⭐ Future Improvements

Possible future enhancements:
- Real-world map integration
- Deep Learning survival prediction
- Multi-agent coordination
- Reinforcement Learning optimization
- Web-based dashboard



