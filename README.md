# run_analysis.R code book


#code info:

The first segment of data is used to download the data. The second segment was used to read and convert the data
into a single data frame. The next five parts do what the project requested in the same order. Part 3 takes the data from 
data.train and data.test and merges them. Part 4 simply takes the data table from part 3 and extracts the means and standard 
deviations. Part 5 uses the activity_labels.txt file and names the activities in the data set. Part 6 uses the names from
part 5 and replaces the original names in the data set with those. Finally, part 7 makes the data.tidy which is a tidy data 
set and then copies that table and makes a new file with the data.
