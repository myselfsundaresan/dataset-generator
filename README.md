# 📊 Dataset Generator

A lightweight, browser-based utility designed for researchers, data scientists, and students to reconstruct raw datasets from aggregate statistics.

Often, in meta-analyses or when reviewing old papers, you only have the **summary statistics (Mean and SD)** but need raw data to test a visualization or run a non-parametric test.  
This tool helps you bridge that gap by generating **synthetic datasets** that mathematically match your target parameters.

---

## ✨ Key Features

- **Precise Statistical Matching**  
  Generates data that converges *exactly* to your input Mean and Standard Deviation.

- **Multi-Group Support**  
  Create multiple experimental or control groups (e.g., Control, Treatment A, Treatment B) simultaneously.

- **Multi-Variable Support**  
  Define multiple parameters (e.g., Age, BMI, Blood Pressure) for each group.

- **Instant Verification**  
  A built-in *Verification* panel compares target statistics against generated data in real time.

- **Export Options**  
  Download datasets as **CSV** (Excel / SPSS / R compatible) or **JSON**.

- **Click-to-Copy**  
  Copy individual columns directly to your clipboard for fast pasting into analysis tools.

---

## 🛠️ How It Works

The tool uses a normalization-based statistical algorithm to ensure accuracy:

1. **Random Sampling**  
   Generates `n` values from a standard normal distribution using the **Box–Muller transform**.

2. **Linear Transformation**  
   The data is transformed to force the sample mean and SD to exactly match user inputs:

\[
x_{new} = \left( \frac{x - \mu_{current}}{\sigma_{current}} \right) \cdot \sigma_{target} + \mu_{target}
\]

This guarantees mathematical consistency with the requested parameters.

---

## 🚀 Getting Started

This is a **pure client-side web application** — no installation required.

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/dataset-generator.git
```

### 2️⃣ Open the Tool
Simply open `datagenerator.html` in any modern web browser:
- Chrome
- Firefox
- Safari
- Microsoft Edge

---

## 📖 How to Use

1. **Configure Variables**  
   Click **+ Variable** to define what you are measuring (e.g., *Reaction Time*).

2. **Add Groups**  
   Use **+ Group** to create different study arms.

3. **Input Parameters**
   - Set sample size (`n`)
   - Enter Mean
   - Enter Standard Deviation (SD)

4. **Generate Data**  
   Click **Regenerate Dataset**.

5. **Review & Export**
   - Verify results in the *Verification* tab
   - Navigate group-wise data using tabs
   - Export the full dataset using **CSV** or **JSON**

---

## 🧪 Research Use Cases

- **Pilot Study Simulation**  
  Test statistical pipelines before collecting real data.

- **Missing Data Recovery**  
  Recreate raw datasets from published summary tables.

- **Educational Demonstrations**  
  Teach the relationship between standard deviation and data spread.

- **Software & Visualization Testing**  
  Generate large datasets to stress-test dashboards or charts.

---

## 📄 License

Distributed under the **MIT License**.  
See the `LICENSE` file for more information.

---

> 💡 *Note:* This tool generates **synthetic data** and should not be used as a substitute for real experimental data in clinical or regulatory research.
