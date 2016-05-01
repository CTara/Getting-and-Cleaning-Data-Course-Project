# Getting-and-Cleaning-Data-Course-Project
run_analysis()

The following points explain the process on how the tidy_data.txt file is obtained by running run_analysis() function

1. If data.table and reshape2 packages are unavailable, the two packages are installed. The two packages are included in the code.
2. Load activity labels and column names
3. For train and test data, only mean and standard deviation are selected in extract_features
4. Test and tain data : x_test, y_test, x_train, y_train, subject_test, subject_train files are loaded into respective variables
5. Only mean and standard deviations are selected and reassigned to X_test and X_train files
6. y_test and y_train column two are extracted into variables and are assigned header names Activity_ID and Activity_Label.
7. subject_test variable name is assigned as subject
8. Merges two data set with 
      : Column bind for subject_test, y_test,x_test into test_data and likewise subject_train, y_train and y_train      into tidy_data : : Row bind test_data and tidy_data into data and assigns column names.
9. Use melt function to convert data into molten data frame and assign to melt_data
10.Melt_data is casted into data frame and is written into a file tidy_data.txt
