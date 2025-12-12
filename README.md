# 🎨 Interactive Cubic Bézier Curve – Spring Physics Simulation (Web)

This project is an interactive visualization of a **cubic Bézier curve** that behaves like a flexible rope.  
The animation responds to mouse movement, and the curve updates in real-time using a **spring–damping physics model**.

Everything is implemented **from scratch**, including:

- Cubic Bézier curve math  
- Tangent calculation  
- Spring physics  
- Real-time canvas rendering  
- Mouse-based interaction  

---

## 🚀 Features

### ✔️ Manual Bézier Curve Implementation
The curve is computed using the standard cubic Bézier formula:

B(t) = (1 - t)^3 P0
+ 3(1 - t)^2 t P1
+ 3(1 - t) t^2 P2
+ t^3 P3

---

### ✔️ Tangent Visualization
Directional tangent lines are rendered using the derivative:

B'(t) = 3(1 - t)^2 (P1 - P0)
+ 6(1 - t) t (P2 - P1)
+ 3 t^2 (P3 - P2)

---

### ✔️ Spring-Damper Motion
The inner control points move naturally using:



a = -k(x - target) - damping * v

---

### ✔️ Smooth 60 FPS Canvas Rendering
The entire simulation is updated using `requestAnimationFrame`.

---

## 🛠️ Technologies Used

- **HTML5 Canvas**

---

## 📁 Project Structure



Bezier-spring/
│
├── index.html # HTML + CSS + JS (single page)
└── README.md # Documentation


*(Your entire project runs from one HTML file.)*

---

## 🔧 How to Run

Simply open:



index.html


No server or build tools required.

---

## 🌀 Interaction Controls

- **Drag** the orange control points to reshape the curve  
- **Move your mouse** to influence the rope motion  
- Tangent lines update dynamically as the curve moves  

---

## 🎥 Recording Instructions (for assignment submission)

1. Open `index.html` in your browser  
2. Use a screen recorder:  
   - Windows → `Win + G` (Xbox Game Bar)  
   - macOS → `Cmd + Shift + 5`  
3. Record 20–30 seconds showing:  
   - dragging the control points  
   - rope-like motion  
   - tangent lines updating  

---

## 📌 Notes

- No libraries or frameworks were used  
- All math + physics code is custom built  
- Spring stiffness, damping, and sampling step can be tuned easily  
- The project is extendable (gravity, wind, multi-segment ropes, etc.)

---

## 🧑‍💻 Author

Created as part of an assignment on **graphics programming, Bézier math, and real-time physics simulation**.
