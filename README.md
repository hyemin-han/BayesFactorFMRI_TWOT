# BayesFactorFMRI_TWOT
Refer to https://github.com/hyemin-han/BayesFactorFMRI for further details about the basic stuff. BayesFactorFMRII_TWOT will be integrated into the newer version of BayesFactorFMRI in a long term.

Modify these files to test two-group t-test:
1. run_this.py
  bayes_correction_main("mask.nii","list.csv","list2.csv",32,0)
    "mask.nii" -> the mask nii file to specify voxels to be analyzed (e.g., mask.nii created by SPM, Atlas map)
    "list.csv" -> a csv file containing the names of contrast nii files in Group 1
    "list2.csv" -> a csv file containing the names of contrast nii files in Group 2
    32 -> how many cores will be employed? Default: 32 cores. If you are going to run the code on your laptop or desktop, it shall be < 8 in the most cases.
2. list.csv and list2.csv
  Enter the names of contrast nii files (created from first-level analysis) that you want to analyze.

Then, you need to copy all nii files, the contrast nii files for two groups and mask nii file, to the folder where all Python and R code files are available (in the same folder). If you specify directories in csv files, then place responsive nii files to the designated folders.
Once all files are prepared, run "python run_this.py." Then, it will test "nii in list.csv > nii in list2.csv." If you want to compare list2 > list, then change the list files appropriately.
