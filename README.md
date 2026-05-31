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

Original SlaKoNet repository:
https://github.com/atomgptlab/slakonet
