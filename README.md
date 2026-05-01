# 🧩 Rubik’s Cube Simulator (Java)

A full 3×3 Rubik’s Cube simulator implemented in Java.  
This project models the cube’s internal state, supports all six face rotations, loads cube states from file, applies move sequences, and checks whether the cube is solved.

This project demonstrates **matrix manipulation**, **file parsing**, **custom exceptions**, and **algorithmic rotation logic**.

---

## 🚀 Features

- **Full 3×3 cube representation** using a 6×3×3 char matrix  
- **Clockwise rotations** for all faces: `F`, `B`, `L`, `R`, `U`, `D`  
- **Apply move sequences** (e.g., `"FRULDB"`)  
- **Load cube state from a formatted text file**  
- **Validate file format and cube characters**  
- **Check if the cube is solved**  
- **Compute the order of a move sequence** (how many repetitions return to solved state)  
- **Human‑readable cube printing** in net layout  

---

## 🧠 Technical Highlights

### **Cube Representation**
The cube is stored as:

