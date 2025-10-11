

# 🌀 Fibonacci Sequence Generator

A simple and interactive **Streamlit app** that generates the **Fibonacci sequence** based on the number of terms entered by the user.

---

## 🚀 Features

* 📈 Generates Fibonacci sequence up to **N** terms
* ⚙️ Simple and intuitive **Streamlit UI**
* 🖥️ Instant display of results
* 🧮 Lightweight and beginner-friendly example for Streamlit apps

---

## 🧰 Tech Stack

* **Python 3.x**
* **Streamlit**

---

## 📦 Installation

1. **Clone this repository**

   ```bash
   git clone https://github.com/yourusername/fibonacci-streamlit.git
   cd fibonacci-streamlit
   ```

2. **Create and activate a virtual environment** *(optional but recommended)*

   ```bash
   python -m venv venv
   source venv/bin/activate     # On Linux/Mac
   venv\Scripts\activate        # On Windows
   ```

3. **Install dependencies**

   ```bash
   pip install streamlit
   ```

---

## ▶️ Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

Then open your browser and navigate to:

```
http://localhost:8501
```

---

## 📜 Code Overview

```python
import streamlit as st

def fibonacci(n):
    fib_sequence = []
    a, b = 0, 1
    for _ in range(n):
        fib_sequence.append(a)
        a, b = b, a + b
    return fib_sequence

st.title("Fibonacci Sequence Generator")

n_terms = st.number_input(
    "Enter the number of terms you want in the Fibonacci sequence:",
    min_value=1,
    value=10,
    step=1
)

if st.button("Generate Sequence"):
    fib_sequence = fibonacci(n_terms)
    st.write(f"First {n_terms} terms of Fibonacci sequence:")
    st.write(fib_sequence)
```

---

## 🧠 Example Output

**Input:** 7
**Output:** `[0, 1, 1, 2, 3, 5, 8]`

---

## 🧩 Future Enhancements

* Add option to **plot Fibonacci numbers** as a chart
* Display the **ratio (Golden ratio)** convergence
* Allow **CSV export** of the sequence

---

## 👨‍💻 Author

**Satvik Dubey**
💼 AI DevSecOps Engineer

