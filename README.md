# **Agent-Based Modeling of Patient Behavior and Healthcare Access**

This project simulates patient behavior and their facility choices using **agent-based modeling** (ABM). It explores how patients with varying levels of flexibility (stubborn vs. flexible) adapt their preferences over repeated social interactions, facility constraints, and peer influence.

---

## **Table of Contents**
1. [Overview](#overview)
2. [Features](#features)
3. [Simulation Scenarios](#simulation-scenarios)
4. [Installation](#installation)
5. [Usage](#usage)

---

## **Overview**
This simulation creates a network of patients visiting one of two healthcare facilities (Facility A or B). Each patient has:
- A **personality** (flexible or stubborn).
- A preference for one of the facilities.
- Characteristics like **age**, **income**, and **health conditions**.

The goal is to analyze:
- **How preferences evolve over time** through social interactions.
- The role of **stubbornness and flexibility** in influencing convergence.
- The effects of **facility constraints** on patient choices.

---

## **Features**
1. **Dynamic Patient Behavior:**
   - Patients adjust their preferences based on social influence.
   - Flexible patients adapt more; stubborn patients resist change.
2. **Facility Attributes:**
   - Facilities have qualities like **cost**, **quality**, **reputation**, and **capacity** that affect patient preferences.
3. **Social Influence:**
   - Patients belonging to the same social group influence each other.
4. **Stubbornness Index:**
   - Quantifies the population's resistance to preference changes.
5. **Visualizations:**
   - Histograms, density plots, and pie charts visualize preference distributions, social groups, and personality types.

---

## **Simulation Scenarios**
### **Scenario 1: Basic Interaction**
- Patients interact, and flexible patients adapt based on the producer's facility.

### **Scenario 2: Stubbornness and Convergence**
- Different levels of stubbornness are tested to observe their impact on preference convergence.

### **Scenario 3: Complex Model**
- Patients have attributes like age, income, and health condition.
- Facility preferences are calculated using facility attributes and patient characteristics.
- Social and resource constraints are enforced.

---

## **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/agent-based-modeling.git
   ```
2. Install the required Python libraries:
   ```bash
   pip install numpy matplotlib seaborn pandas
   ```

---

## **Usage**
1. Open the `AgentBasedModeling.ipynb` notebook in Google Colab or Jupyter Notebook.
2. Run each cell sequentially to:
   - Generate random populations.
   - Simulate patient interactions.
   - Visualize the results.

3. Example usage in Python:
   ```python
   from simulate import simulate, compute_stubbornness_index
   
   n = 2000  # Population size
   k = 400  # Number of interactions
   
   initial_population = make_population(n)
   population, initial_stats, final_stats = simulate(n, k)
   
   stubbornness_index = compute_stubbornness_index(population, initial_population)
   print(f"Stubbornness Index: {stubbornness_index}")
   ```

---

## **Results and Visualizations**
### **Key Outputs:**
1. **Stubbornness Index:**
   - Quantifies population flexibility.
2. **Preference Convergence:**
   - Tracks the reduction in standard deviation over interactions.
3. **Impact of Social Groups:**
   - Social influence on preferences within groups.
