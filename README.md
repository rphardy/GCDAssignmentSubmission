# Getting and Cleaning Data Assignment Submission

This Readme describes the analysis run_analysis.R, which performs the following on the UCI HAR dataset:

1) Sets the working directory, downloads the zipped data, unzips it.

2) (Section 1): From the unzipped .txt files, reads in 6 files and merges them into one complete dataset: 
  testing set subject data,
  testing set activity data,
  testing set outcome data,
  training set subject data,
  training set activity data,
  training set outcome data.

3) (Section 2): Names all variables with descriptive names, specified in features.txt, and extracts the information on the mean and standard deviation, by keeping these features only. It extracts only the measurements that have both mean and s.d. explicitly: i.e. the measures that end in mean() and s.d(). Measures with a mean, but no standard deviation are excluded: i.e those that end in meanFreq() are excluded. 

4) (Section 3): Ascribes descriptive names to the values in the activity variable, using names provided in activity_labels.txt

5) (Section 4): - From the data set in step 4, writes a second, independent tidy data set with the average of each variable for each activity and each subject and reads this back in to R to check it.

See codebook, run_analysis.R and tidied_data.txt

To read in tidied_data and store as a dataframe to check, copy, paste and update:

check <- read.table("INSERTYOURDIRECTORY/tidied_data.txt",header=TRUE) 
