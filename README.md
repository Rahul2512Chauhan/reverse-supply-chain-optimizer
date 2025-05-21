# Reverse Supply Chain Optimizer

## 📦 Project Overview

The **Reverse Supply Chain Optimizer** is an end-to-end machine learning solution designed to predict product returns, estimate return costs, optimize reverse logistics, and manage returned inventory. This pipeline helps businesses minimize losses and improve operational efficiency in handling returned products.

---

## 🧩 Project Phases

### 🔹 Phase 1: Product Return Prediction
- **Goal:** Predict the likelihood of a product being returned.
- **Model:** XGBoost Classifier
- **Output:** Return probability (0 or 1)
- **Artifacts:** `xgb_model.pkl`, `scaler.pkl`

### 🔹 Phase 2: Return Cost Estimation
- **Goal:** Estimate the cost associated with a product return.
- **Model:** XGBoost Regressor
- **Output:** Predicted return cost
- **Artifacts:** `xgb_cost_model.pkl`

### 🔹 Phase 3: Reverse Logistics Optimization
- **Goal:** Optimize the selection of return centers based on cost and distance.
- **Method:** Rule-based logic and optimization heuristics
- **Output:** Best return center location

### 🔹 Phase 4: Inventory Optimization
- **Goal:** Decide what to do with returned items (restock, refurbish, dispose).
- **Method:** Decision rules based on condition, demand, and return cost
- **Output:** Inventory action recommendation

### 🔹 Phase 5: Integrated Pipeline
- **Goal:** Provide a unified Jupyter Notebook to demonstrate full system
- **Notebook:** `05_integrated_pipeline.ipynb`
- **Features:**
  - Load models
  - Predict return
  - Estimate cost
  - Run logistics and inventory modules
  - Visualization and explanation in Markdown

---

## 🛠 Folder Structure
Reverse-Supply-Chain-Optimizer/
├── phase_1_product_return_prediction/
├── phase_2_return_cost_estimation/
├── phase_3_reverse_logistics_optimization/
├── phase_4_inventory_optimization/
├── phase_5_integration_notebook/
├── requirements.txt
└── README.md


---

## 💡 Highlights

- ✅ Built with modular architecture
- ✅ Easy to extend and scale
- ✅ All models are saved as `.pkl` for reuse
- ✅ Integration notebook demonstrates real-world flow

---

## 🚀 How to Use

1. Clone the repository (if hosted)
2. Install dependencies using `pip install -r requirements.txt`
3. Open `06_integrated_pipeline.ipynb` in Jupyter Notebook or Colab
4. Run each cell to test the full pipeline

---

## 📚 Future Improvements

- Add advanced decision trees for Phase 3 and 4
- Use a database backend for larger input batches
- Optionally deploy with a Streamlit or Voila UI
