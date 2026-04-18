# Xavier Hill Roy

## GPU Computing & Systems Engineer
Master's Student at McMaster University, specializing in  GPU Acceleration, Evolutionary Computing  and Parallel Systems.

I enjoy architecting systems to run fast and optimizing existing systems.  My research focuses on porting irregular evolutionary algorithms to NVIDIA A100s, optimizing memory hierarchy to minimize warp divergence, and scaling workloads across HPC clusters.

## Tech Stack
* **Languages:** C++, CUDA C++, Python, RISC-V Assembly
* **HPC & Systems:** CUDA, OpenACC, OpenMP, MPI, Slurm, SIMD/Vectorization
* **Tools:** Nsight Compute, CMake, gRPC, Protocol Buffers, Linux/Unix
* **Hardware:** NVIDIA A100/H100, AMD EPYC, Raspberry Pi

## Current Research: Accelerating Evolution
**High-Throughput Linear Genetic Programming (LGP) on GPUs**
I am currently architecting a CUDA-based LGP engine to solve visual symbolic regression tasks.
* **Challenge:** Genetic Programming is notorious for branch divergence and irregular memory access.
* **Solution:** Designing custom memory arenas and flat-array program representations to maximize SIMT efficiency on NVIDIA H100s.


## Featured Engineering Projects

### [GPU Optimization Benchmarks](https://github.com/xavierhillroy/gpu-optimization-benchmarks)
*A collection of performance studies benchmarking serial vs. parallel implementations on data-center hardware.*
* **Core Tech:** CUDA C++, OpenACC, NVIDIA A100
* **Result:** Achieved 63.36x speedup on Prime Number Generation by optimizing nested loop structures with `collapse(2)` and parallel reductions.
* **Hardware:** Ported from AMD EPYC 7413 (CPU) to NVIDIA A100-SXM4 (GPU).

### [Toy MoE Inference Routing Benchmark](https://github.com/xavierhillroy/<repo-name>)
*A GPU microbenchmark studying routing and dispatch overhead in Mixture-of-Experts inference.*
* **Core Tech:** PyTorch, CUDA, Nsight Systems, NVTX
* **Result:** Benchmarked naive, grouped, and cached-grouped MoE dispatch under uniform and skewed routing patterns; grouping tokens by expert consistently reduced latency versus naive dispatch.
* **Profiling:** Used Nsight Systems to show that cached grouping removed online routing-plan construction overhead while expert FFN execution remained the dominant cost.

### [Parallel LGP Engine for Visual Control](https://github.com/xavierhillroy/LGP_Vision)
*A distributed evolutionary computing system for Visual Reinforcement Learning.*
* **Core Tech:** Python, HPC Clusters (Digital Research Alliance)
* **Result:** Scaled population evaluation across 64 CPU cores, reducing training time by an order of magnitude.
* **Architecture:** Implemented thread-pool execution to handle variable-length genetic programs without stalling the pipeline.

### [JPEG XL Predictor Optimization](https://github.com/xavierhillroy/libjxl-wop8)
*Algorithmic optimization of the JPEG XL lossless compression standard.*
* **Core Tech:** Genetic Algorithms, C++
* **Result:** Engineered an 8-predictor ensemble (WOP8) that improved compression ratios by 2.98% on medical and document datasets.
* **Publication:** Published in *Electronics* (2025).

## Connect With Me
I am always open to discussing GPU architecture, kernel optimization, and systems programming.

* **Email:** [hillroyx@mcmaster.ca](mailto:hillroyx@mcmaster.ca)
* **LinkedIn:** [linkedin.com/in/xavier-hill-roy](https://www.linkedin.com/in/xavier-hill-roy/)
