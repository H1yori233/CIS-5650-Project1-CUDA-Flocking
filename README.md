# Project 1 Flocking
* Kaiqin, Kong
  * [Github](https://github.com/H1yori233)
* Tested on: Windows 11, AMD Ryzen 7 5800H @ 3.20GHz 16GB, RTX 3050 Laptop 4GB



## Boids Flocking Simulation

This project implements a CUDA-based simulation of the Boids Flocking algorithm, with various optimizations to improve performance.

![boid](./images/boid.gif)



### Performance Overview

1. **Naive Search**: O(n²) complexity, inefficient beyond ~10,000 boids.
2. **Uniform Grid (Scattered)**: O(n) complexity, ~17x faster than naive.
3. **Uniform Grid (Coherent)**: O(n) complexity, 30% faster than scattered.

### Key Results

- **Base Performance (23,333 boids)**:
  - Naive: 12.83 ms/frame
  - Scattered Grid: 0.73 ms/frame
  - Coherent Grid: 0.56 ms/frame
- **Optimization**:
  - Coherent grid improves performance by 30%.
  - Optimal block size: 256 threads.