Added a step-by-step notebook demonstrating the SlaKoNet inference workflow using a SiC POSCAR example.

This walkthrough shows how the main SlaKoNet classes and functions are connected, including:
- reading a POSCAR file,
- converting the structure into a SlaKoNet Geometry object,
- loading the pretrained SlaKoNet model,
- generating the orbital shell dictionary and k-point path,
- creating the SimpleDftb calculator,
- inspecting the Basis object and Slater–Koster parameter pairs,
- constructing H(k) and S(k),
- solving the generalized eigenvalue problem H(k)c = E(k)S(k)c,
- obtaining eigenvalues, occupations, band gap, and band structure.

The goal is to understand the internal code flow of SlaKoNet rather than treating the package as a black box.

What this notebook does not do:

This notebook does not explain or rewrite the full internal implementation of each SlaKoNet class. For example, it does not derive in detail how SimpleDftb internally solves the eigenvalue problem, how hs_matrix constructs every Slater–Koster matrix element, or how the interpolation of distance-dependent parameters is implemented inside the package.

Instead, the notebook helps track the complete code flow and shows where each major class is used. Readers can use this walkthrough as a guide to navigate the original SlaKoNet source code and then inspect individual classes and functions in detail.

Original SlaKoNet repository:
https://github.com/atomgptlab/slakonet
