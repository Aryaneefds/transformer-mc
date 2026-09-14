# transformer-mc

Build a transformer from scratch in **machine code** on Ubuntu x86-64
(AMD Ryzen 5 7520U). Part of my Personal AI Coach OS major project.

## Status
- M1 (x86-64 execution model): partial
- **M2 (minimal machine-code program)**: in progress — `exit.s` + `run_bytes.py` must both return `42`

## Milestones
1. x86-64 execution model
2. Minimal machine-code program ← NOW
3. Registers, memory, calling conventions
4. Arithmetic & memory ops
5. Vector ops
6. Matrix ops
7. Embeddings
8. Attention
9. Transformer block (MVP)
10. Tiny training
11. Benchmark vs PyTorch
12. Write-up (performance, limits, lessons)

## Verify M2
```bash
gcc -nostdlib -o exit exit.s && ./exit; echo $?
python3 run_bytes.py  # prints 42
```

Tracking: `~/coach-os/05_transformer_project.md`
