# CrypWater
Source code of CrypWater and available initial trajectory
#This is a list of jupyter notebook codes that can be used to do water-density analysis using MD trajectories of proteins.
To implement the code:
1. Make sure MDAnalysis and Torch is available in your python environment
2. Make sure the initial trajectory you used is the unaligned protein trajectory with water-oxygens
The first step of water density calculation is to copy water box to six directions, which can be done with the 'copy_water_box_to_6_directions' script.
With the copied protein-water_oxygen pdbs, the user have to combine them into a new trajectory with VMD and then RMS-align the trajectory.
Now, with this aligned_copied-water-oxygen_protein trajectory, we can start the water density calculation with 'water_density_calculation' script.
With the calculated water density maps, the resulted .dx files can be loaded by chimerax, VMD or pymol
Next, the user can use the 'Gaussian_Mixture_Model_Flexible_Residue_Identification' for convex-residue identification
Then the residues have to be selected out of the cluster result based on observations from MD trajectory, basically the region of clusters that covers the cryptic site region
Afterwards, the 'CrypWater_Volume_calculation' script can be used for cryptic site volume calculation.

There is also a 'convex-region' script that can be used to generate convex-hull files readable by ChimeraX or Pymol
