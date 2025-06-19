# 🚀 Matrix CUDA

High-performance matrix multiplication using CUDA with GPU acceleration.

## What it does

- GPU-accelerated matrix multiplication (A × B = C)
- Compares GPU vs CPU performance
- Implements naive and tiled CUDA algorithms
- Achieves 100-700x speedup over single-threaded CPU

## Performance Results

```
Matrix Size: 1024×1024
GPU Time:    13.6 ms
CPU Time:    9925 ms
Speedup:     729x
```

## Implementation

**Naive GPU:** One thread per output element  
**Tiled GPU:** Shared memory optimization for better cache utilization  
**CPU Baseline:** Single-threaded reference implementation

## Requirements

- NVIDIA GPU with CUDA support
- CUDA Toolkit installed
- GCC compiler

## Algorithm Details

### Naive Implementation
- 1 thread = 1 output element
- Global memory access: 2×M×N×K words
- Computation-to-memory ratio: ~1/4

### Tiled Implementation
- Thread blocks compute tiles using shared memory
- Reduced global memory access: 2×M×N×K/B words
- Better computation-to-memory ratio: ~B/4

## Benchmarks

| Matrix Size | GPU Time | CPU Time | Speedup |
|------------|----------|----------|---------|
| 1024×1024  | 13.6ms   | 9.9s     | 729x    |
| 2300×2300  | 167ms    | 19.5s    | 117x    |

**Hardware:** Intel Xeon E5645 + NVIDIA GPU

## Learning Goals

- CUDA programming fundamentals
- Memory optimization techniques
- GPU vs CPU performance analysis
- Parallel algorithm design

---

🎯 **Perfect for learning GPU programming and performance optimization!**
