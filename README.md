# Scene-Classification-Images-and-Audio
Visuals and Sound extracted from Video for Scene Classification experiments



## Do images and audio complement one another in scene classification?

These dataset is made up of images from 8 different environments. 37 video sources have been processed, every 1 second an image is extracted (frame at 0.5s, 1.5s, 2.5s ... and so on) and to accompany that image, the MFCC audio statistics are also extracted from the relevant second of video. 

In this dataset, you will notice some common errors from single classifiers. For example, in the video of London, the image classifier confuses the environment with "FOREST" when a lady walks past with flowing hair. Likewise, the audio classifier gets confused by "RIVER" when we walk past a large fountain in Las Vegas due to the sounds of flowing water. Both of these errors can be fixed by a multi-modal approach, where fusion allows for the correction of errors. In our study, both of these issues were classified as "CITY" since multimodality can provide a solution for single-modal errors due to anomalous data occurring.


###Please cite this study if you use the dataset
**Look and Listen: A Multi-Modal Late Fusion Approach to Scene Classification for Autonomous Machines**
**Jordan J. Bird, Diego R. Faria, Cristiano Premebida, Aniko Ekart, and George Vogiatzis**

## Context
In this challenge, we can learn environments ("Where am I?") from either images, audio, or take a multimodal approach to fuse the data.

Multi-modal fusion often requires far fewer computing resources than temporal models, but sometimes at the cost of classification ability. Can a method of fusion overcome this? Let's find out!

## Content
Class data are given as strings in dataset.csv

Each row of the dataset contains a path to the image, as well as the MFCC data extracted from the second of video that accompany the frame.

##MFCC Extraction
(copied and pasted from the WIP paper)
we extract the the Mel-Frequency Cepstral Coefficients (MFCC) of the audio clips through a set of sliding windows 0.25s in length (ie frame size of 4K sampling points) and an additional set of overlapping windows, thus producing 8 sliding windows, 8 frames/sec. From each audio-frame, we extract 13 MFCC attributes, producing 104 attributes per 1 second clip.

These are numbered in sequence from MFCC_1

##Two Classes?
The original study deals with Class 2 (the actual environment, 8 classes) but we have included Class 1 also. Class 1 is a much easier binary classification problem of "Outdoors" and "Indoors"


## Acknowledgements

Paper currently under peer review (1st Feb 2020), check back soon for the reference!

**Please cite this study if you use the dataset**
