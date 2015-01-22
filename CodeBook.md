---
title: "CodeBook.md"
author: "Ray Jones"
date: "January 22, 2015"
output: html_document
---

## Introduction

For all variables except subject and activity, the values in the file are the means of the normalized values extracted from the UCI HAR data sets averaged across subject / activity. For the original definitions of the raw data variables see the relevant descriptions presented at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones - the description included below has been modified from that included in this data set.

## Feature Selection 

The features originally selected for the database come from the accelerometer and gyroscope 3-axial raw signals tacc.xyz and tgyro.xyz. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tbodyacc.xyz and tgravityacc.xyz) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tbodyaccjerk.xyzand tbodygyrojerk.xyz). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tbodyaccmag, tgravityaccmag, tbodyaccjerkmag, tbodygyromag, tbodygyrojerkmag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fbodyacc.xyz, fbodyaccjerk.xyz, fbodygyro.xyz, fbodyaccjerkmag, ffodygyromag, fbodygyrojerkmag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern - ‘.xyz’ is used to denote 3-axial signals in the X, Y and Z directions.

* tbodyacc.xyz
* tgravityacc.xyz
* tbodyaccjerk.xyz
* tbodygyro.xyz
* tbodygyrojerk.xyz
* tbodyaccmag
* tgravityaccmag
* tbodyaccjerkmag
* tbodygyromag
* tbodygyrojerkmag
* fbodyacc.xyz
* fbodyaccjerk.xyz
* fbodygyro.xyz
* fbodyaccmag
* fbodyaccjerkmag
* fbodygyromag
* fbodygyrojerkmag

The variables estimated from these signals are: 

* .mean: Mean value
* .std: Standard deviation

As discussed above, the values in the run_analysis.R output file are then the means of these normalized values extracted from the UCI HAR data sets averaged across subject / activity. 

## Codebook
```
subject                  : int
    subject ID code
		1..30

activity                 : chr
	activity identifier
		laying
		sitting
		standing
		walking
		walking.downstairs
		walking.upstairs

tbodyacc.mean.x          : num
	mean normalized value
		-1.00..1.00

tbodyacc.mean.y          : num
	mean normalized value
		-1.00..1.00

tbodyacc.mean.z          : num
	mean normalized value
		-1.00..1.00

tbodyacc.std.x           : num
	mean normalized value
		-1.00..1.00

tbodyacc.std.y           : num
	mean normalized value
		-1.00..1.00

tbodyacc.std.z           : num
	mean normalized value
		-1.00..1.00

tgravityacc.mean.x       : num
	mean normalized value
		-1.00..1.00

tgravityacc.mean.y       : num
	mean normalized value
		-1.00..1.00

tgravityacc.mean.z       : num
	mean normalized value
		-1.00..1.00

tgravityacc.std.x        : num
	mean normalized value
		-1.00..1.00

tgravityacc.std.y        : num
	mean normalized value
		-1.00..1.00

tgravityacc.std.z        : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.mean.x      : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.mean.y      : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.mean.z      : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.std.x       : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.std.y       : num
	mean normalized value
		-1.00..1.00

tbodyaccjerk.std.z       : num
	mean normalized value
		-1.00..1.00

tbodygyro.mean.x         : num
	mean normalized value
		-1.00..1.00

tbodygyro.mean.y         : num
	mean normalized value
		-1.00..1.00

tbodygyro.mean.z         : num
	mean normalized value
		-1.00..1.00

tbodygyro.std.x          : num
	mean normalized value
		-1.00..1.00

tbodygyro.std.y          : num
	mean normalized value
		-1.00..1.00

tbodygyro.std.z          : num
	mean normalized value
		-1.00..1.00

tbodygyrojerk.mean.x     : num
	mean normalized value
		-1.00..1.00

tbodygyrojerk.mean.y     : num
	mean normalized value
		-1.00..1.00

tbodygyrojerk.mean.z     : num  
	mean normalized value
		-1.00..1.00

tbodygyrojerk.std.x      : num  
	mean normalized value
		-1.00..1.00

tbodygyrojerk.std.y      : num  
	mean normalized value
		-1.00..1.00

tbodygyrojerk.std.z      : num 
	mean normalized value
		-1.00..1.00

tbodyaccmag.mean         : num 
	mean normalized value
		-1.00..1.00

tbodyaccmag.std          : num 
	mean normalized value
		-1.00..1.00

tgravityaccmag.mean      : num 
	mean normalized value
		-1.00..1.00

tgravityaccmag.std       : num 
	mean normalized value
		-1.00..1.00

tbodyaccjerkmag.mean     : num 
	mean normalized value
		-1.00..1.00

tbodyaccjerkmag.std      : num 
	mean normalized value
		-1.00..1.00

tbodygyromag.mean        : num 
	mean normalized value
		-1.00..1.00

tbodygyromag.std         : num 
	mean normalized value
		-1.00..1.00

tbodygyrojerkmag.mean    : num 
	mean normalized value
		-1.00..1.00

tbodygyrojerkmag.std     : num 
	mean normalized value
		-1.00..1.00

fbodyacc.mean.x          : num 
	mean normalized value
		-1.00..1.00

fbodyacc.mean.y          : num 
	mean normalized value
		-1.00..1.00

fbodyacc.mean.z          : num 
	mean normalized value
		-1.00..1.00

fbodyacc.std.x           : num 
	mean normalized value
		-1.00..1.00

fbodyacc.std.y           : num 
	mean normalized value
		-1.00..1.00

fbodyacc.std.z           : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.mean.x      : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.mean.y      : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.mean.z      : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.std.x       : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.std.y       : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerk.std.z       : num 
	mean normalized value
		-1.00..1.00

fbodygyro.mean.x         : num 
	mean normalized value
		-1.00..1.00

fbodygyro.mean.y         : num 
	mean normalized value
		-1.00..1.00

fbodygyro.mean.z         : num 
	mean normalized value
		-1.00..1.00

fbodygyro.std.x          : num 
	mean normalized value
		-1.00..1.00

fbodygyro.std.y          : num 
	mean normalized value
		-1.00..1.00

fbodygyro.std.z          : num 
	mean normalized value
		-1.00..1.00

fbodyaccmag.mean         : num 
	mean normalized value
		-1.00..1.00

fbodyaccmag.std          : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerkmag.mean 	 : num 
	mean normalized value
		-1.00..1.00

fbodyaccjerkmag.std  	 : num 
	mean normalized value
		-1.00..1.00

fbodygyromag.mean    	 : num 
	mean normalized value
		-1.00..1.00

fbodygyromag.std     	 : num 
	mean normalized value
		-1.00..1.00

fbodygyrojerkmag.mean	 : num 
	mean normalized value
		-1.00..1.00

fbodygyrojerkmag.std 	 : num 
	mean normalized value
		-1.00..1.00

```
