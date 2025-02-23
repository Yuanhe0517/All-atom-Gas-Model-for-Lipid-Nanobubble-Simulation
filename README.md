# All-atom-Gas-Model-for-Lipid-Nanobubble-Simulation

# AA-LNB.py

`AA-LNB.py` is a modified version of `insane.py` [1] by Yuan He, Yuxuan Wang, Xiu Li, and Xubo Lin. It can generate the input conformation for lipid nanobubble simulations.

## Generating Lipid Nanobubble Simulation Systems

The following commands were used to generate lipid nanobubble simulation systems with different gas cores:

```sh

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol N2:0.06 -sold 0.27 -salt 0.15 -a 1.2 -gas N2 -o N2-LNB.gro -gden 250 -excl 0.5

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol H2:0.06 -sold 0.27 -salt 0.15 -a 1.2 -gas H2 -o H2-LNB.gro -gden 18 -excl 0.5

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol O2:0.06 -sold 0.27 -salt 0.15 -a 1.2 -gas O2 -o O2-LNB.gro -gden 290 -excl 0.5

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol CO:0.06 -sold 0.27 -salt 0.15 -a 1.2 -gas CO -o CO-LNB.gro -gden 220 -excl 0.5

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol CO2:1.3 -sold 0.26 -salt 0.15 -a 1.2 -gas CO2 -o CO2-LNB.gro -gden 520 -excl 0.5

AA-LNB.py -r 3 -d 1 -x 20 -y 20 -z 20 -u POPC -sol TIP3:100 -sol SO2:0.4 -sold 0.26 -salt 0.15 -a 1.2 -gas SO2 -o SO2-LNB.gro -gden 570 -excl 0.5
```

## Parameter Explanation

-r Radius of the gas sphere (nm)

-d Distance between periodic images (nm)

-x X dimension or first lattice vector of the system (nm)

-y Y dimension or first lattice vector of the system (nm)

-z Z dimension or first lattice vector of the system (nm)

-u Lipid type and relative abundance (NAME[:#])

-sol Solvent type and relative abundance (NAME[:#])

-sold Solvent diameter (nm)

-salt Salt concentration (NaCl, mol/L)

-a Area per lipid (nm²)

-gas Gas type and relative abundance (NAME[:#])

-gden Gas density (kg/m³)

-excl Exclusion range (nm) for solvent addition relative to the membrane surface

-o Output GRO file: Membrane with Protein

## References:

[1] Wassenaar, T. A.; Ingólfsson, H. I.; Bockmann, R. A.; Tieleman, D. P.; Marrink, S. J. Computational
lipidomics with insane: a versatile tool for generating custom membranes for molecular simulations. J. Chem.
Theory Comput. 2015, 11, 2144-2155.
