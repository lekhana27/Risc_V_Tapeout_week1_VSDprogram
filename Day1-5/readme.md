📅 Day 1 – Introduction To RTL Verilog Design And Synthesis

📘 Introduction to Verilog RTL Design and Synthesis

I learned about the basic flow of RTL design and simulation. A simulator like iverilog is used to check if the RTL design meets the specifications by applying test vectors through a testbench (TB). The TB provides input stimuli and monitors outputs to validate functionality.

The design is written in Verilog, and the results are observed using waveform viewers like gtkwave. For synthesis, tools like Yosys are used along with Sky130 PDKs, which provide standard cell libraries. These libraries contain Verilog models of standard cells used for logic synthesis.

📘 Labs using iverilog and gtkwave

In this lab, I learned how to write simple Verilog testbenches, simulate them using iverilog, and visualize signal waveforms in gtkwave. This helps in debugging and verifying RTL designs by observing the behavior of signals over time.

📘 Introduction to Yosys and Logic synthesis

Yosys is an open-source tool for logic synthesis. It takes RTL Verilog code and maps it to a gate-level representation using standard cell libraries (like Sky130). This process transforms high-level RTL into circuits that can be implemented on silicon.

📘 Labs using Yosys and Sky130 PDKs

In this lab, I practiced synthesizing RTL designs with Yosys using the Sky130 process design kits (PDKs). These PDKs provide standard cells that represent physical hardware. The synthesis flow showed how RTL gets converted into gate-level netlists ready for implementation.

📅 Day 2 – Timing libs, hierarchical vs flat synthesis, and efficient flop coding styles

📘 Introduction to timing .libs

Timing libraries (.lib) contain detailed information about standard cells such as delay, setup, hold, and power. These libraries help synthesis tools map RTL into hardware while meeting timing constraints.

📘 Hierarchical vs Flat Synthesis

Hierarchical synthesis preserves module boundaries, making designs easier to debug and reuse.

Flat synthesis combines all modules into a single netlist, enabling better optimization but harder to manage.
I learned when to use each approach depending on design complexity and optimization needs.

📘 Various Flop Coding Styles and Optimization

Different ways of coding flip-flops in Verilog can lead to different synthesis results. I explored reset types (async/sync), enable signals, and efficient flop coding practices that reduce area and improve timing.

📅 Day 3 – Combinational and Sequential Optimizations


📘 Introduction to Optimizations

Optimizations in synthesis improve design performance, reduce area, and minimize power. Tools automatically restructure logic while ensuring functionality remains the same.

📘 Combinational Logic Optimizations

Techniques such as constant propagation, boolean simplification, and redundancy removal are applied to simplify combinational circuits and improve efficiency.

📘 Sequential Logic Optimizations

These optimizations improve flip-flop usage and sequential behavior, including state machine simplification, register retiming, and clock gating for power reduction.

📘 Sequential Optimizations for Unused Outputs

When outputs or registers are unused, synthesis tools remove them to save area and power. I learned how synthesis detects and eliminates such redundant logic automatically.

📅 Day 4 – GLS, Blocking vs Non-Blocking, and Synthesis–Simulation Mismatch

📘 GLS, Synthesis–Simulation Mismatch and Blocking/Non-Blocking Statements
I learned about Gate-Level Simulation (GLS), which verifies the post-synthesis netlist with actual gate delays.
This day highlighted how incorrect use of blocking (=) vs non-blocking (<=) assignments can cause functional differences between RTL simulation and synthesized hardware, leading to synthesis–simulation mismatches.

📘 Labs on GLS and Synthesis–Simulation Mismatch
Hands-on labs running gate-level simulations to observe timing effects and confirm that synthesized logic matches RTL behavior.

📘 Labs on Synth–Sim Mismatch for Blocking Statement
Practical exercise showing how using blocking assignments in sequential logic can create unexpected outputs after synthesis, and how to correct them.

📅 Day 5 – Optimization in Synthesis

📘 If–Case Constructs
Studied Verilog if/else and case statements and their synthesis impact.
I learned the importance of complete conditions and proper defaults to avoid unintended latch inference.

📘 Labs on “Incomplete If Case”
Experimented with designs missing else branches to see how synthesis infers latches and how to fix them.

📘 Labs on “Incomplete Overlapping Case”
Observed problems caused by overlapping or incomplete case statements, and learned how to write priority and unique cases correctly.

📘 for loop and for generate
Explored synthesizable for loops and the generate construct to create repetitive hardware structures efficiently.

📘 Labs on “for loop” and “for generate”
Implemented parameterized modules using for and generate to practice scalable RTL design.