# memory-labs

> Exploratory C programs and notes focused on how memory is laid out, allocated, and randomized at runtime.

---

## 🎯 Purpose
This repo is a collection of **small labs** that break down memory behavior in Linux:
- Stack vs heap growth
- .data / .bss segments
- `mmap` regions and file-backed mappings
- Address Space Layout Randomization (ASLR) and Position Independent Executables (PIE)
- Observing memory layouts with `/proc/[pid]/maps` and gdb

---

## 📂 Structure
- `labs/` — numbered labs (`lab01_stack`, `lab02_heap`, …)  
- `docs/` — markdown explainers, ASCII diagrams, screenshots of gdb runs  
- `tools/` — small Python/Bash helpers for inspecting `/proc` and ELF headers  

---

## 🧪 Example labs
- `lab01_stack/stack_demo.c` → local variables + frame pointer inspection  
- `lab02_heap/heap_growth.c` → malloc/free behavior, brk pointer movement  
- `lab03_aslr/aslr_check.c` → observe randomized base addresses  

---

## 🚀 Getting started
```bash
git clone https://github.com/OneMartiniTuringRE/memory-labs.git
cd memory-labs/labs/lab01_stack
gcc -O0 -g stack_demo.c -o stack_demo
./stack_demo
