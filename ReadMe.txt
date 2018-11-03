The code for this DSGE project begins with a preprocessing step to preprocess the data before feeding it to the R code that does the Matrix Factorization step and subsequently runs the MCMC steps. These individual steps are described in further detail, below.

1. VBA Script:
______________

(i) To run the VBA script, first clear the contents of all the worksheets in the file named "filteredData_New.xlsm", except the first 3 worksheets, namely "filteredData__", "Concepts", and "data_transpose". 

(ii) Once clearing all the worksheets and leaving in the ones named in the step above, click the "View" tab on the spreadsheet, choose "Macros", and then choose "View Macros" from the drop-down tab. You'll see "Module1.tst1", highlight that and choose either "Run" to run it right away, or choose "Edit" to view it and then subsequently run it.

(iii) After it has run, copy the following worksheets into individual worksheets, which you can then name as .csv files and save for uploading to the R script that runs the Matrix Factorization and Estimation steps:
	(a) Copy the contents of the sheet "bcyc" into a file and name it "bcyc.csv"
	(b) Copy the contents of the sheet "id" into a file and name it "idx.csv"
	(c) Copy the contents of the following sheets and respectively name them as stated: "a_idx" as "a_idx.csv"; 		"b_idx" as "b_idx.csv"; "q_idx" as "q_idx.csv"; "d_idx" as "d_idx.csv"

2. R script:
____________

(i) Enter the full file paths into the placeholders inside the R-script named "matFact_N_Estimation.txt". The filenames are intuitive to connect with the descriptions given in the preceding section, under "VBA Script"

(ii) Make sure you have R version 3.3.x installed, together with an rstan package, preferrably version 2.17

(iii) Run the script, "matFact_N_Estimation.txt" to completion. Note that the last step in the MCMC sets of runs takes quite long to complete, so you might need to turn off the sleep option on your computer, so that it doesn't go off to sleep and can be left unattended to run for about 8 days continuously
