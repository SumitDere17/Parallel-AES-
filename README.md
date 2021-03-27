

## Introduction
Advanced Encryption Standard (AES) is a symmetric-key algorithm and is one of the strongest standards for electronic encryption in the world. It is widely used in software, hardware as well as in cloud applications. However, AES takes quite some time to encrypt messages especially when the number of users as well as the length of the text is quite large, which is the case in cloud enviroments.  

The paper defines 6 algorithms, namely:  
 * `GCS`  : GPU Coalescing and Slicing
 * `GCNS` : GPU Coalescing and no Slicing
 * `GNC`  : GPU no Coalescing and no Slicing
 * `CCS`  : CPU Coalescing and Slicing
 * `CCNS` : CPU Coalescing and no Slicing
 * `CNC`  : CPU no Coalescing and no Slicing  
  
All these algorithms have been implemented in this project and the results have been recorded, visualised and verified.  


## Instructions for Use
1. Clone this repository `git clone https://github.com/gurupunskill/parallel-aes.git`.
2. Change directory to `parallel-aes/src`.
    1. Change directory to `generator`.
    2. Run `g++ generate.cpp` and `./a.out`. This creates a dataset which will be used by the algorithms.
    3. Change directory to any one of the 7 implemented AES algorithm. For instance, `gcs` would hold the GCS algorithm.
    4. Run `g++ <algo-name>.cpp` and `./a.out`. You will view the corresponding times on the console.
    5. Change directory to `prop_dataset` to view the ciper texts in your text editor. 


## Software Tools, Languages and Frameworks Used
1. `C++` : C++ was the primary programming language used for implementing the algorithms.
2. `python` : The Python programming language was used to visulaise the results by plotting graphs.
3. `CUDA` : CUDA platform was used to implement the three GPU algorithms as it provides architecture for parallel computing on the GPU.
4. `OpenMP` : OpenMP platform was used to implement the three CPU algorithms as it provides architecture for parallel computing on the CPU.
5. `VSCode` : VSCode was the primary text editor used.
6. `github` : Github was used for collaboration and as a version control system.


## Results
![alt text](docs/img/Comparing-Algorithms.png)

The code was executed and tested with a uniformly random dataset of 100 files to 1000 files. Each file had random data from 30KB to 150KB generated using a pseudo random generator.  

The results are concurrent with that of those published in the paper.  

## Contributors
1. Gurupungav Narayanan 16CO128 
2. Nihal Haneef 16CO114  
