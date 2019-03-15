# Defect-Formation-Calculation

This package is a integrated Defect Formation energy package, which contains generating tetrahedral interstitial sites and  octahedral interstitial sites, submitting `VASP` calculation job and withdraw necessary data to calculate defect formation energy.


## Generate defect structures

There are three kinds of defect system you can generate, vacancy defect, purity defect and interstitial defect. All these can be generated by [defect_maker](./defect_maker.py), and the generated structures in VASP format will be stored in a directory named by its attributes.



## submit your common calculation jobs
Here, we supply some integrated shell scripts to calculate the jobs you need.<br />
- [x] [structure_relax](./common_calculation_shell/stru_relax.sh)<br />
- [x][structures_optimization](./common_calculation_shell/stru_optimization.sh)<br />
- [x][structures_self-consistent-field](./common_calculation_shell/stru_scf.sh)<br />
- [x] [structures_band-calculation](./common_calculation_shell/stru_band.sh)<br />
- [x][structures_dos-calculation](./common_calculation_shell/stru_dos.sh)<br />
and a main [job scripts](./common_calculation_shell/job.sh) to submit your job.

We also supply some scripts to generate the input files needed in `VASP` Calculation, such as `INCAR`, `KPOINTS`, `POTCAR`, you can also use these  scripts to generate them.

So in general, Your can just begin your job from a `POSCAR` and a `job.sh`.
