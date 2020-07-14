# ComputerArch-Prj1
## Part A

In part A, we write three simple assembly programs to implement three functions in `example.c`. 
Based on ensuring correctness, we especially focus on the functional equivalence with the example C functions. 
By selecting and placing labels in the assembly code appropriately, the code is also very readable.
## Part B

In part B, we modify the `HCL` file of the Y86's sequential design to add a new instruction --- `iaddl`. 
The following is the roadmap to finish this part:

- Clarify the computation process of `iadd` and write it down at the beginning in `seq-full.hcl`.
- Add dependency relations of `iaddl` to all boolean signals.
- Design the datapath for `iaddl`, i.e., generate control signals for `src` and `dst`

## Part C

We achieve full scores in the benchmark testing **in just 2 hours**, 
but we **spent 2 more days** researching all the potential methods to optimize the performance even further. 
The following is our roadmap:
- Change the order of the instruction sequence to avoid data hazard and structure hazards as much as possible, which leaves *CPE = 12.96*.
- Beyond the changes on instruction order, we apply loop unrolling to reduce the number of conditional check and registers updating, which leaves *CPE = 9.83*.
- Use a binary search tree to find the precise remaining number of elements after several rounds of unrolling to achieve complete unrolling, which leaves *CPE = 8.95*.
- Modify the pipeline design in **HCL** file to achieve 100% accuracy in branch prediction for certain code pattern, which **brings CPE down to 7.79**.
