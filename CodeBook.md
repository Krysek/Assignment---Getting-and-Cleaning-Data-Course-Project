# Code Book
The source is https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip. For creating "tidy data", only mean and standard deviation values as well as labels of actvities and features are taken over and merged from the source. Finally, the average of each variable (grouped by activity and subject) is calculted and stored in the file "tidy_data.txt".

# Description
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix ‘t’ to denote time) were captured at a constant rate of 50 Hz. and the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) – both using a low pass Butterworth filter.

The body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

A Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the ‘f’ to indicate frequency domain signals).

# Description of abbreviations of measurements
Leading t or f is based on time or frequency measurements.

* Body = related to body movement.
* Gravity = acceleration of gravity
* Acc = accelerometer measurement
* Gyro = gyroscopic measurements
* Jerk = sudden movement acceleration
* Mag = magnitude of movement

mean and std (=standard deviation) are calculated for each subject for each activity for each mean and SD measurements.

# Fields
## ID Fields
1. `subjectId` - The participant ("subject") ID
2. `activity` - The label of the activity performed when the corresponding measurements were taken. This variable covers 6 different activities:
  * `WALKING` (value 1): Subject was walking during the test.
  * `WALKING_UPSTAIRS` (value 2): subject was walking up a staircase during the test.
  * `WALKING_DOWNSTAIRS` (value 3): subject was walking down a staircase during the test.
  * `SITTING` (value 4): subject was sitting during the test.
  * `STANDING` (value 5): subject was standing during the test.
  * `LAYING` (value 6): subject was laying down during the test.

## Extracted Feature Fields
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
