# HAR: Weight Lifting Exercises
## Codebook

### Acknowledgements

Without kind contribution of the data set of the following research, this Course Project would have been impossible.

**Groupware@LES - Projects - Weight Lifting Exercises**  
Site: <http://groupware.les.inf.puc-rio.br/har>  
Working Paper: <http://groupware.les.inf.puc-rio.br/work.jsf?p1=11201>  
  
*Velloso, E.; Bulling, A.; Gellersen, H.; Ugulino, W.; Fuks, H. Qualitative Activity Recognition of Weight Lifting Exercises. Proceedings of 4th International Conference in Cooperation with SIGCHI (Augmented Human '13) . Stuttgart, Germany: ACM SIGCHI, 2013.*

### Overview

This Codebook is split into 3 parts:

- Overview of index.HTML
- Study Design
- Variables involved

### Overview of included HTML File

This HTML file contains the prediction algorithm used to produce the results. The main objective is to predict the manner in which the participants would do the exercises. This is particularly important in this research; you would want to know how many participants would do well in a training exercise, to assess the effectiveness of the training.

The only training done here is a Unilateral Dumbbell Biceps Curl. More details can be found in the Study Design, on how research is done on this particular exercise.

The HTML file contained in this repositiory is compiled; you can simply open it and look at the results.

### Study Design

*Description of study design may also be found on the site itself. This part is extracted for convenience to the readers of the repository.*

This human activity recognition research has traditionally focused on discriminating between different activities, i.e. to predict "which" activity was performed at a specific point in time (like with the Daily Living Activities dataset above). The approach we propose for the Weight Lifting Exercises dataset is to investigate "how (well)" an activity was performed by the wearer. The "how (well)" investigation has only received little attention so far, even though it potentially provides useful information for a large variety of applications,such as sports training.

In this work (refer to the working paper) we first define quality of execution and investigate three aspects that pertain to qualitative activity recognition: the problem of specifying correct execution, the automatic and robust detection of execution mistakes, and how to provide feedback on the quality of execution to the user. We tried out an on-body sensing approach (dataset here), but also an "ambient sensing approach" (by using Microsoft Kinect - dataset still unavailable)

Six young health participants were asked to perform one set of 10 repetitions of the Unilateral Dumbbell Biceps Curl in five different fashions: exactly according to the specification (Class A), throwing the elbows to the front (Class B), lifting the dumbbell only halfway (Class C), lowering the dumbbell only halfway (Class D) and throwing the hips to the front (Class E).

Class A corresponds to the specified execution of the exercise, while the other 4 classes correspond to common mistakes. Participants were supervised by an experienced weight lifter to make sure the execution complied to the manner they were supposed to simulate. The exercises were performed by six male participants aged between 20-28 years, with little weight lifting experience. We made sure that all participants could easily simulate the mistakes in a safe and controlled manner by using a relatively light dumbbell (1.25kg).

### Features

The sensors mainly depended on 3 types of readings to gain the data:

- Accelerometer (accel)
- Gyroscope (gyros)
- Magnetic Meter (magnet)

The sensors are attached to the arm, forearm, dumbbell, and waist (belt) of the experimental subject. These locations are reproduced fully as part of the covariate name used in this data set.

The eight features used in the data set, as follows, generated a total of 96 derived feature sets of sensor data.

- mean
- variance
- standard deviation
- max
- min
- amplitude
- kurtosis
- skewness

This case, I removed all these derived feature sets, as the objective is to use the original data to predict the type of activity the human is doing.

### Variables Included

Presence of NAs hold no predictive power. Columns with 70% or more NA obsevations will be removed, and near zero covariates will be removed as well. The following variables are the result of the clean up of the data set.

**Naming Variables**
  
X (Observation No.)  
user\_name  
raw\_timestamp\_part\_1  
raw\_timestamp\_part\_2  
cvtd\_timestamp  
new\_window  
num\_window  

**Sensor Variables**
  
roll\_belt  
pitch\_belt  
yaw\_belt  
total\_accel\_belt  
gyros\_belt\_x  
gyros\_belt\_y  
gyros\_belt\_z  
accel\_belt\_x  
accel\_belt\_y  
accel\_belt\_z  
magnet\_belt\_x  
magnet\_belt\_y  
magnet\_belt\_z  
roll\_arm  
pitch\_arm  
yaw\_arm  
total\_accel\_arm  
gyros\_arm\_x  
gyros\_arm\_y  
gyros\_arm\_z  
accel\_arm\_x  
accel\_arm\_y  
accel\_arm\_z  
magnet\_arm\_x  
magnet\_arm\_y  
magnet\_arm\_z  
roll\_dumbbell  
pitch\_dumbbell  
yaw\_dumbbell  
total\_accel\_dumbbell  
gyros\_dumbbell\_x  
gyros\_dumbbell\_y  
gyros\_dumbbell\_z  
accel\_dumbbell\_x  
accel\_dumbbell\_y  
accel\_dumbbell\_z  
magnet\_dumbbell\_x  
magnet\_dumbbell\_y  
magnet\_dumbbell\_z  
roll\_forearm  
pitch\_forearm  
yaw\_forearm  
total\_accel\_forearm  
gyros\_forearm\_x  
gyros\_forearm\_y  
gyros\_forearm\_z  
accel\_forearm\_x  
accel\_forearm\_y  
accel\_forearm\_z  
magnet\_forearm\_x  
magnet\_forearm\_y  
magnet\_forearm\_z  
classe
