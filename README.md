# Classical Simulations of Quantum Circuits Using Reinforcement Learning
<!-- ROADMAP -->
## Roadmap

- [x] design and implement the MPS-based simulation enviromnet (Gym style)
- [x] design and implement the TTN-based simulation environment (Gym style)
- [x] Using RL algorithm to solve the MPS-based quantum circuits simulation problem
- [x] Using RL algorithm to solve the TTN-based quantum circuits simulation problem
- [ ] Dataset and benchmark
- [ ] Design and implement the MPS-based massive parallel simulation envrionment
- [ ] Design and implement the TTN-based massive parallel simulation envrionment


## Experimental Results
Tensor-Train/MPS tensor network  
![TT](https://user-images.githubusercontent.com/75991833/217780619-40f42213-62b8-4db5-bfa9-0c9f8d97081d.png)  
We present the ___Number of multiplications___ versus the ___Number of nodes___.   

| Tensor   Network | number of nodes | 10    | 50     | 100    | 200    | 400     | 600     | 800     | 1000    | 1500    | 2000    |  
|:----------------:|-----------------|-------|--------|--------|--------|---------|---------|---------|---------|---------|---------|  
| Tensor-Train/MPS | OE greedy       | 3.848 | 15.875 | 30.927 | 61.030 | 121.236 | 181.442 | 241.648 | 301.854 | X       | X       |  
|                  | OE dynamic      | 3.693 |--------|--------|--------|---------|---------|---------|---------|---------|---------|  
|                  | CTG greedy      | 3.693 | 15.656 | 30.705 | 60.808 | 121.014 | 181.220 | 241.426 | 301.632 | X       | X       |  
|                  | CTG kahypar     | 3.690 | 15.650 | 30.710 | 60.810 | 121.010 | 181.220 | 241.430 | 301.630 | 451.150 | 602.660 |  
|                  | RL-Hamiltonian  |       |        |        |        |         |         |         |         |         |         |  

note: (1) OE dynamic can not give a solution in a limited time for the number of nodes from 50 to 2000.  
(2) OE greedy and CTG greedy can not scale up to the number of nodes 15000 and 2000.  

Reference:

[1] Meirom, E., Maron, H., Mannor, S., & Chechik, G. Optimizing tensor network contraction using reinforcement learning. In International Conference on Machine Learning (pp. 15278-15292). ICML 2022.
