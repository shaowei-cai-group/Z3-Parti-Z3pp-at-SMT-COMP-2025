# Z3-Parti-Z3++ at SMT-COMP 2025

We intend to participate in the forthcoming SMT-COMP 2025 by submitting **Z3-Parti-Z3++** for **the Parallel Track** categories.

**Z3-Parti-Z3++** is a **wrapper** tool from Z3 and intend for **QF_RDL, QF_IDL, QF_LRA, QF_LIA, QF_NRA, and QF_NIA**. The authors of **Z3-Parti-Z3++** are **Mengyu Zhao and Shaowei Cai**.

The system description is named `Z3_Parti_Z3pp_at_SMT_COMP_2025.pdf`.

As per the submission rule, we are providing the pseudo-random 32-bit unsigned number **998244353**.

Zenodo DOI: [TBD]

## Variable-level Partitioning for Distributed SMT Solving

Z3-Parti-Z3++ is the practical implementations of our innovative concept of **Var**iable-level **Parti**tioning, which is applied to the Arithmetic theories. This technique is introduced for the first time in our recently published paper at CAV 2024, titled *Distributed SMT Solving Based on Dynamic Variable-level Partitioning*.

Within Arithmetic theories, each time VarParti picks a variable and partitions the problem by dividing the feasible domain of the variable, leading to sub-problems, which can be further simplified via constraint propagation.

Our proposed variable-level partitioning permits robust, comprehensive partitioning. Regardless of the Boolean structure of any given instance, our partitioning algorithm can keep partitioning to the last moment of the solving process.

Building on our CAV 2024 work on variable-level partitioning, **Z3-Parti-Z3++** has evolved from a parallel solver into a fully **distributed** engine that scales smoothly from a handful of cores to hundreds of nodes.
The new implementation adopts a two-tier **leader–coordinator–worker** hierarchy that cleanly separates distributed scheduling from parallel solving.

Detailed information on the original parallel framework appears in our paper ``Distributed SMT Solving Based on Dynamic Variable-level Partitioning''.
We have provided our solver, evaluation scripts, and related experimental results in \href{https://github.com/shaowei-cai-group/AriParti}{GitHub-AriParti}.

In our future work, a comprehensive description of the additional mechanisms introduced in the distributed version will be presented.


## How to Build and Test

Download solver binary files in Zenodo.

Test in the instance:
```bash
python3 solver/run_AriParti.py path_to_test_case.smt2
```
