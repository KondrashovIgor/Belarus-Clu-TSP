# Belarus Clu-TSP: Clustered Traveling Salesman Problem Solver

This repository contains a Jupyter Notebook implementation of a **heuristic algorithm** designed to solve a **Clustered Traveling Salesman Problem (Clu-TSP)** inspired by real-world logistics challenges in Belarus. The solution was developed as part of a coursework or research project focused on combinatorial optimization in logistics.

---

## 📌 Problem Overview

The **Clustered TSP (Clu-TSP)** is a variant of the classic Traveling Salesman Problem with the following characteristics:

- Cities (or nodes) are grouped into **disjoint clusters**.
- The salesman must **visit all cities in a cluster consecutively** before moving to another cluster.
- The objective is to find the shortest possible route that satisfies the clustering constraint.

In this specific case, the problem models **logistic delivery routes across regions (clusters) of Belarus**, where deliveries within a region must be completed before moving on to the next.

---

## 🧠 Algorithm Summary

The notebook implements a **custom greedy constructive heuristic** that:

1. **Groups locations by region** (clusters predetermined or inferred from data).
2. **Optimizes intra-cluster routes** using nearest-neighbor or similar heuristics.
3. **Determines inter-cluster visitation order** based on centroid distances or other proximity measures.
4. **Constructs a full feasible tour** respecting the Clu-TSP constraints.

> **Note**: This is a *short-term (operational-level)* heuristic algorithm intended for practical use with moderate-sized instances, not a provably optimal solver.

---

## 📁 Repository Contents

- `Срочный_алгоритм_логистика_РБ (1).ipynb`:  
  Main Jupyter Notebook containing:
  - Data loading & preprocessing (Belarus regional delivery points)
  - Cluster definition
  - Heuristic construction steps
  - Route visualization (using `matplotlib`)
  - Performance metrics (total distance, feasibility check)

> The file name translates to "Urgent Logistics Algorithm for Belarus (1).ipynb".

---

## 🛠️ Requirements

To run this notebook, you’ll need:

- Python 3.8+
- Jupyter Notebook or JupyterLab
- Required Python packages (install via `pip`):

```bash
pip install numpy pandas matplotlib scikit-learn
```

(Additional dependencies may be inferred from notebook imports.)

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/KondrashovIgor/Belarus-Clu-TSP.git
   ```
2. Navigate to the project folder:
   ```bash
   cd Belarus-Clu-TSP
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open and run `Срочный_алгоритм_логистика_РБ (1).ipynb`.

> Ensure input data (e.g., coordinates of delivery points, cluster labels) is available in the expected format. The notebook may assume hardcoded data or local CSV files.

---

## 📊 Output

After execution, the notebook will:
- Display the constructed route as a 2D plot (with clusters color-coded)
- Print total tour length
- Show sequence of visited nodes grouped by cluster

---

## 📚 References & Context

This work relates to:
- **Clustered TSP** literature (e.g., Chisman, 1975; Guttmann-Beck et al., 2000)
- **Logistics optimization** in national or regional distribution networks
- **Heuristic design** for NP-hard routing problems

---

## 📝 License

Unless otherwise specified, this code is for **educational and research purposes only**.  
Check the repository’s `LICENSE` file (if present) for usage rights.

---

## 🙋 Contact

For questions or collaboration, contact the author via GitHub:  
[@KondrashovIgor](https://github.com/KondrashovIgor)

---

> *Optimizing Belarusian logistics, one cluster at a time.* 🇧🇾
