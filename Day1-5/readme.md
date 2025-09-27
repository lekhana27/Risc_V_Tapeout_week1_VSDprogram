# 📅 Day 1 – Introduction To RTL Verilog Design And Synthesis

## 📘 Introduction to Verilog RTL Design and Synthesis
I learned about the basic flow of RTL design and simulation. A simulator like **iverilog** checks if the RTL design meets the specifications by applying test vectors through a **testbench (TB)**.  
The TB provides input stimuli and monitors outputs to validate functionality.

The design is written in Verilog, and results are observed using waveform viewers like **gtkwave**.  
For synthesis, tools like **Yosys** are used along with **Sky130 PDKs**, which provide standard cell libraries containing Verilog models of standard cells for logic synthesis.

---

## 📘 Labs using iverilog and gtkwave
Wrote simple Verilog testbenches, simulated them with iverilog, and visualized waveforms in gtkwave to debug and verify RTL designs.

---

## 📘 Introduction to Yosys and Logic synthesis
**Yosys** is an open-source tool for logic synthesis.  
It maps RTL Verilog code to a gate-level representation using standard cell libraries (like Sky130).

---

## 📘 Labs using Yosys and Sky130 PDKs
Practiced synthesizing RTL designs with Yosys and Sky130 PDKs, observing how RTL is converted into gate-level netlists.

---

# 📅 Day 2 – Timing libs, Hierarchical vs Flat Synthesis, and Efficient Flop Coding Styles

## 📘 Introduction to timing .libs
Timing libraries (`.lib`) contain detailed information about standard cells such as delay, setup, hold, and power.  
These libraries guide synthesis tools to meet timing constraints.

---

## 📘 Hierarchical vs Flat Synthesis
- **Hierarchical synthesis** preserves module boundaries, easing debugging and reuse.  
- **Flat synthesis** combines all modules into a single netlist for better optimization but harder management.  
Learned when to use each based on complexity and optimization needs.

---

## 📘 Various Flop Coding Styles and Optimization
Explored different flip-flop coding methods—async/sync reset, enable signals—and how coding style affects area and timing.

---

# 📅 Day 3 – Combinational and Sequential Optimizations

## 📘 Introduction to Optimizations
Synthesis optimizations improve performance, reduce area, and minimize power while preserving functionality.

---

## 📘 Combinational Logic Optimizations
Techniques such as constant propagation, Boolean simplification, and redundancy removal simplify circuits.

---

## 📘 Sequential Logic Optimizations
Includes register retiming, state-machine simplification, and clock gating for power reduction.

---

## 📘 Sequential Optimizations for Unused Outputs
Synthesis removes unused outputs/registers to save area and power.

---

# 📅 Day 4 – GLS, Blocking vs Non-Blocking, and Synthesis–Simulation Mismatch

## 📘 GLS, Synthesis–Simulation Mismatch and Blocking/Non-Blocking Statements
Learned about **Gate-Level Simulation (GLS)**, which verifies the post-synthesis netlist with real gate delays.  
Incorrect use of blocking (`=`) vs non-blocking (`<=`) assignments can cause mismatches between RTL simulation and synthesized hardware.

---

## 📘 Labs on GLS and Synthesis–Simulation Mismatch
Hands-on gate-level simulations to observe timing effects and confirm synthesized logic matches RTL behavior.

---

## 📘 Labs on Synth–Sim Mismatch for Blocking Statement
Exercise showing how blocking assignments in sequential logic create unexpected outputs after synthesis and how to correct them.

---

# 📅 Day 5 – Optimization in Synthesis

## 📘 If–Case Constructs
Studied Verilog `if/else` and `case` statements and their synthesis impact.  
Learned the importance of complete conditions and proper defaults to avoid unintended latches.

---

## 📘 Labs on “Incomplete If Case”
Experimented with designs missing `else` branches to see how synthesis infers latches and how to fix them.

---

## 📘 Labs on “Incomplete Overlapping Case”
Observed issues from overlapping or incomplete `case` statements and learned to write priority/unique cases correctly.

---

## 📘 for loop and for generate
Explored synthesizable `for` loops and the `generate` construct to create repetitive hardware structures efficiently.

---

## 📘 Labs on “for loop” and “for generate”
Implemented parameterized modules using `for` and `generate` to practice scalable RTL design.
