# Code Book

This R-code downloads data about "Human Activity Recognition Using Smartphones Data Set" (http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones), fetchs only mean and standard deviation values and merge this set of data with activity and feature labels. All labels are correspond to camelcase notation. At the end the result is stored in the file `tidy.txt`.


## Steps in detail
1. Download data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and stores in the subdirectory "./data/".
2. Unzip downloaded zip file in "./data".
3. Load "activity labels"
4. Load "features" and select only labels about mean and standard deviation labels
5. Adjust lables into CamelCase notation and without dashs
6. Load test data
7. Load training data
8. Merge subject data from training and test
9. Rename subject identifier column in "subjectId"
10. Merge "set data" from test and training data and select only mean and standard deviation values
11. Add column name from selected feature labels
12. Merge "activity data" from test and training data
13. Rename activity identifier column in "activityId"
14. Merge activity data and activity labels
15. Merge merged subject data, merged activity data and merged set data
16. Write merged data into file "tidy.txt"


## Fields
### ID Fields
1. `subjectId` - The participant ("subject") ID
2. `activity` - The label of the activity performed when the corresponding measurements were taken. This variable covers 6 different activities:
  * `WALKING` (value 1): Subject was walking during the test.
  * `WALKING_UPSTAIRS` (value 2): subject was walking up a staircase during the test.
  * `WALKING_DOWNSTAIRS` (value 3): subject was walking down a staircase during the test.
  * `SITTING` (value 4): subject was sitting during the test.
  * `STANDING` (value 5): subject was standing during the test.
  * `LAYING` (value 6): subject was laying down during the test.

### Extracted Feature Fields
3. `tBodyAccMeanX` (from column `1`)
4. `tBodyAccMeanY` (from column `2`)
5. `tBodyAccMeanZ` (from column `3`)
6. `tBodyAccStdX` (from column `4`)
7. `tBodyAccStdY` (from column `5`)
8. `tBodyAccStdZ` (from column `6`)
9. `tGravityAccMeanX` (from column `41`)
10. `tGravityAccMeanY` (from column `42`)
11. `tGravityAccMeanZ` (from column `43`)
12. `tGravityAccStdX` (from column `44`)
13. `tGravityAccStdY` (from column `45`)
14. `tGravityAccStdZ` (from column `46`)
15. `tBodyAccJerkMeanX` (from column `81`)
16. `tBodyAccJerkMeanY` (from column `82`)
17. `tBodyAccJerkMeanZ` (from column `83`)
18. `tBodyAccJerkStdX` (from column `84`)
19. `tBodyAccJerkStdY` (from column `85`)
20. `tBodyAccJerkStdZ` (from column `86`)
21. `tBodyGyroMeanX` (from column `121`)
22. `tBodyGyroMeanY` (from column `122`)
23. `tBodyGyroMeanZ` (from column `123`)
24. `tBodyGyroStdX` (from column `124`)
25. `tBodyGyroStdY` (from column `125`)
26. `tBodyGyroStdZ` (from column `126`)
27. `tBodyGyroJerkMeanX` (from column `161`)
28. `tBodyGyroJerkMeanY` (from column `162`)
29. `tBodyGyroJerkMeanZ` (from column `163`)
30. `tBodyGyroJerkStdX` (from column `164`)
31. `tBodyGyroJerkStdY` (from column `165`)
32. `tBodyGyroJerkStdZ` (from column `166`)
33. `tBodyAccMagMean` (from column `201`)
34. `tBodyAccMagStd` (from column `202`)
35. `tGravityAccMagMean` (from column `214`)
36. `tGravityAccMagStd` (from column `215`)
37. `tBodyAccJerkMagMean` (from column `227`)
38. `tBodyAccJerkMagStd` (from column `228`)
39. `tBodyGyroMagMean` (from column `240`)
40. `tBodyGyroMagStd` (from column `241`)
41. `tBodyGyroJerkMagMean` (from column `253`)
42. `tBodyGyroJerkMagStd` (from column `254`)
43. `fBodyAccMeanX` (from column `266`)
44. `fBodyAccMeanY` (from column `267`)
45. `fBodyAccMeanZ` (from column `268`)
46. `fBodyAccStdX` (from column `269`)
47. `fBodyAccStdY` (from column `270`)
48. `fBodyAccStdZ` (from column `271`)
49. `fBodyAccMeanFreqX` (from column `294`)
50. `fBodyAccMeanFreqY` (from column `295`)
51. `fBodyAccMeanFreqZ` (from column `296`)
52. `fBodyAccJerkMeanX` (from column `345`)
53. `fBodyAccJerkMeanY` (from column `346`)
54. `fBodyAccJerkMeanZ` (from column `347`)
55. `fBodyAccJerkStdX` (from column `348`)
56. `fBodyAccJerkStdY` (from column `349`)
57. `fBodyAccJerkStdZ` (from column `350`)
58. `fBodyAccJerkMeanFreqX` (from column `373`)
59. `fBodyAccJerkMeanFreqY` (from column `374`)
60. `fBodyAccJerkMeanFreqZ` (from column `375`)
61. `fBodyGyroMeanX` (from column `424`)
62. `fBodyGyroMeanY` (from column `425`)
63. `fBodyGyroMeanZ` (from column `426`)
64. `fBodyGyroStdX` (from column `427`)
65. `fBodyGyroStdY` (from column `428`)
66. `fBodyGyroStdZ` (from column `429`)
67. `fBodyGyroMeanFreqX` (from column `452`)
68. `fBodyGyroMeanFreqY` (from column `453`)
69. `fBodyGyroMeanFreqZ` (from column `454`)
70. `fBodyAccMagMean` (from column `503`)
71. `fBodyAccMagStd` (from column `504`)
72. `fBodyAccMagMeanFreq` (from column `513`)
73. `fBodyBodyAccJerkMagMean` (from column `516`)
74. `fBodyBodyAccJerkMagStd` (from column `517`)
75. `fBodyBodyAccJerkMagMeanFreq` (from column `526`)
76. `fBodyBodyGyroMagMean` (from column `529`)
77. `fBodyBodyGyroMagStd` (from column `530`)
78. `fBodyBodyGyroMagMeanFreq` (from column `539`)
79. `fBodyBodyGyroJerkMagMean` (from column `542`)
80. `fBodyBodyGyroJerkMagStd` (from column `543`)
81. `fBodyBodyGyroJerkMagMeanFreq` (from column `552`)
