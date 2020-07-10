# run_analysis.R code info and code book

#code book:

features <- read.csv('./UCI HAR Dataset/features.txt', header = FALSE, sep = ' ')

features <- as.character(features[,2])

data.train.x <- read.table('./UCI HAR Dataset/train/X_train.txt')

data.train.activity <- read.csv('./UCI HAR Dataset/train/y_train.txt', header = FALSE, sep = ' ')

data.train.subject <- read.csv('./UCI HAR Dataset/train/subject_train.txt',header = FALSE, sep = ' ')

data.train <-  data.frame(data.train.subject, data.train.activity, data.train.x)
names(data.train) <- c(c('subject', 'activity'), features)

data.test.x <- read.table('./UCI HAR Dataset/test/X_test.txt')

data.test.activity <- read.csv('./UCI HAR Dataset/test/y_test.txt', header = FALSE, sep = ' ')

data.test.subject <- read.csv('./UCI HAR Dataset/test/subject_test.txt', header = FALSE, sep = ' ')

data.test <-  data.frame(data.test.subject, data.test.activity, data.test.x)

names(data.test) <- c(c('subject', 'activity'), features)

#code info:

The first segment of data is used to download the data. The second segment was used to read and convert the data
into a single data frame. The next five parts do what the project requested in the same order. Part 3 takes the data from 
data.train and data.test and merges them. Part 4 simply takes the data table from part 3 and extracts the means and standard 
deviations. Part 5 uses the activity_labels.txt file and names the activities in the data set. Part 6 uses the names from
part 5 and replaces the original names in the data set with those. Finally, part 7 makes the data.tidy which is a tidy data 
set and then copies that table and makes a new file with the data.
