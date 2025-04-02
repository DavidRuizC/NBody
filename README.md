
# 🌌 N-Body Simulation in Java

This project simulates gravitational interactions between celestial bodies in a 2D space using the **N-body problem** approach. It visualizes orbital mechanics through real-time graphics with `StdDraw`.

## 🚀 Features

- Simulates physics of gravitational attraction between multiple bodies.
- Three simulation modes:
  - `GenericUniverse`: Load custom body data from a file.
  - `CentralConfiguration`: Equal-mass bodies in circular motion.
  - `Nplus1`: One massive central body and N randomly placed satellites.
- Real-time animation using `StdDraw`.
- Modular and extensible design using OOP principles.

## 🧩 Structure Overview

- `Main.java`: Entry point, parses arguments, initializes the universe and starts simulation.
- `Universe.java`: Abstract class that defines shared logic for simulation (force calculation, position updates).
- `NBodySimulator.java`: Manages animation loop and drawing logic.
- `Body.java`: Represents a body with mass, position, and velocity. Can compute force exerted by another body.
- `Vector.java`: Immutable class for vector operations (math, scaling, magnitude).
- `GenericUniverse.java`: Reads initial state from file.
- `CentralConfiguration.java`: Arranges bodies in a symmetric configuration.
- `Nplus1.java`: One central heavy body and several lighter orbiters.
- `StdDraw.java`: Graphics library used to visualize the simulation.

## ▶️ How to Run

### 1. Compile the project:

```bash
javac *.java
```

### 2. Run the simulation

#### GenericUniverse (from file):
```bash
java Main 25000 10 trace generic data.txt
```

#### Central Configuration (N bodies in orbit):
```bash
java Main 25000 10 trace central_configuration 5
```

#### N+1 Configuration (one massive + N others):
```bash
java Main 25000 10 trace nplus1 50
```

**Arguments:**
```
<dt> <pauseTime> <trace> <universeType> <extra>
```
- `dt`: time step per frame
- `pauseTime`: delay in ms between frames
- `trace`: "trace" to enable motion trace, else "no"
- `universeType`: generic, central_configuration, nplus1
- `extra`: file name or number of bodies

## 🧪 Sample Output

Visual output in a canvas window:
- White dots representing bodies.
- Optional motion trail (trace mode).
- Orbital dynamics with gravity effects.

## 🛠 Example Input File (for GenericUniverse)

```
3
1.5e11
1.0e11 2.0e11 0 10000 5.0e24
-1.0e11 -2.0e11 0 -10000 5.0e24
0 0 0 0 1.0e30
```

## 🧠 Concepts Used

- Newtonian mechanics
- Object-Oriented Programming
- Vector arithmetic
- Simulation and visualization

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
