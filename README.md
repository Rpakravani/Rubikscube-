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

Where each face is a 3×3 matrix of color characters.

### **Rotation Logic**
Each rotation:
- Rotates the face itself clockwise  
- Cycles the surrounding edge strips  
- Preserves orientation using reversed indexing where needed  

### **File Parsing**
The constructor validates:
- Exactly 9 lines  
- Max 12 characters per line  
- Only valid cube colors  
- No blank spaces inside faces  

It then maps the 2D net into the 3D cube.

### **Move Order Calculation**
The `order(String moves)` method computes how many times a move sequence must be applied to return the cube to solved state.

---

## 📂 File Structure

/rubikscube

│── RubiksCube.java

│── IncorrectFormatException.java

│── sample_cube.txt

│── README.md


---

## 📄 Example Input File Format

A valid cube file is a 9×12 grid representing the cube net:

O O O
O O O
O O O
G G G W W W B B B Y Y Y
G G G W W W B B B Y Y Y
G G G W W W B B B Y Y Y
R R R
R R R
R R R


(Spaces represent empty areas.)

---


🔧 **Future Improvements**
- Add counter‑clockwise and double moves (F', F2, etc.)
- Add scramble generator
- Add cube solver (Layer Method or Kociemba)
- Add GUI visualization
- Add unit tests
- Add move‑notation parser with spaces and modifiers

## 🧩 How to Use

### **Compile**

### **Run**

### **Load a cube from file**
```java
RubiksCube cube = new RubiksCube("sample_cube.txt");
cube.applyMoves("FRULDB");
System.out.println(cube);




