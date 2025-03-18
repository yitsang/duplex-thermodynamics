# 📌 Duplex Thermodynamics Calculator

## 🔬 Overview  
This repository provides a **Python 3-based thermodynamics calculator** for nucleic acid duplexes, including **DNA, RNA, and RNA-DNA hybrids**.  
It includes the precise handling of:

- **Perfectly matched duplexes** (DNA, RNA, and RNA-DNA hybrids)
- **Internal and terminal mismatches duplexes** (DNA only)
- **Dangling-end scenarios duplexes** (DNA and RNA)

It calculates the following **thermodynamic parameters** using **nearest-neighbor models**:

- **ΔH (Enthalpy, kcal/mol)**
- **ΔS (Entropy, cal/mol·K)**
- **ΔG (Gibbs Free Energy, kcal/mol)**

### ✅ Features  
- Supports **DNA, RNA, and RNA-DNA hybrids**
- Implements **nearest-neighbor thermodynamic models**
- Handles **internal & terminal mismatches**
- Corrects **dangling-end sequences with automated shift**
- Accepts **temperature input in Kelvin (K)**
- **Optimized for Google Colab**

---

## ⚙️ Installation  

### **📥 Clone the repository**  
```bash
git clone https://github.com/yitsang/duplex-thermodynamics.git
cd duplex-thermodynamics
```

### **📦 Install dependencies**  
```bash
pip install biopython pandas numpy
```

---

## 🚀 Running in Google Colab  

1. Open [Google Colab](https://colab.research.google.com/)  
2. Clone the repository in a Colab notebook:  
   ```python
   !git clone https://github.com/yitsang/duplex-thermodynamics.git
   %cd duplex-thermodynamics
   ```
3. Run the script:  
   ```python
   !python calculate_duplex_thermodynamics.py
   ```

---

## 🔢 Input Requirements  
- **Sequence (`seq`)**: Input as a **string** or **Biopython sequence object**.  
- **RNA Sequences**: Convert **U → T** before calculations. *(Not case-sensitive)*  
- **Temperature (`T`)**: Input in **Kelvin (K)**.  
- **Matching Duplex Calculation**: Requires **one input strand** *(complement auto-generated)*.  
- **Unmatching Duplex Calculation**: Requires **two strands**:  
  - **First strand (5' → 3')** → Main sequence  
  - **Second strand (3' → 5')** → Complementary sequence *(manual input, not auto-generated)*  

---

## 📊 Execution Steps  
1️⃣ **Run all parts sequentially** from **Part 0 to Part 5**.  
2️⃣ **Execute Part 5** to start the calculation:  
   ```python
   # 🔹 Run the calculator
   if __name__ == "__main__":
       run_thermodynamics_calculator()
   ```

---

## 📚 References  
This implementation is based on **nearest-neighbor thermodynamic models** from:   
📖 SantaLucia et al. (1996), Biochemistry 35, 3555–3562 for DNA_nn5 table

📖 **Biopython `Bio.SeqUtils.MeltingTemp` module**: Used for reference calculations and thermodynamic modeling. More details at [Bio.SeqUtils.MeltingTemp](https://biopython.org/docs/1.75/api/Bio.SeqUtils.MeltingTemp.html).  
 
---

## 📜 License  
This project is open-source and available under the **MIT License**.  

---

## 🤝 Contributing  
Feel free to **open issues** or **submit pull requests** to improve this tool! 😊   



