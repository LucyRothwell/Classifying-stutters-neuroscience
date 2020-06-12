# The question

Can the occurence of verbal stutters be identified from neural readings?

# Overview

This repository contains code used in a neuroscience research project which aimed to classify verbal stutter events by applying machine learning to neural (EEG and fNIRS) data. It also contains the full study write up (called "Thesis paper" - abstract on page 9). Grade for project: 80% (dissertation for MSc in Psychology Research Methods, UCL).

# The data

4 participants each with 15,000 samples (0.1 second readings) of fNIRS neural readings and 15,000 (0.1 second readings) of EEG neural readings. Labelled.

Participants were males who experience child onset fluency disorder (stuttering). Participants were linked up to fNIRS and EEG neural imaging technology and recorded speaking for around 20 minutes at a time. The audio recordings allowed the stutter events to be time-labelled using Audacity software (see script below). These markings could then be used to label the stutters in the fNIRS/EEG csv files, for use in classification. 

# The code

1. **A script that labels stutter events (1 or 0) on the EEG and fNIRS readings stored in csv files.** In each participant's EEG/fNIRS csv files, there were appropximately 15,000 rows each representing a 0.1 second neural reading. Of these 15,000 rows, around 5% represented stutter events. This script takes as input, the markings from the audio file showing the start and end times of the stutters (they lasted between 0.2 and 3 seconds), and time-syncs these with the fNIRS and EEG data recordings. It then prints a column of 1s and 0s, which can be inserted into the y column "stutter" on the fNIRS/EEG csv exports, meaning each row of data (0.1 second neural reading) is now labelled as being a stutter (1) or not a stutter (0). This labelled csv is then inputted to the machine learning classifiers. This process is explained in detail in the code comments.

2. **The machine learning script** used to classifiy stutter events (using SVM, KNN, Random Forest and Logistic Regression). Explained in the code comments.

#The results

Good results but investigation of overfitting is currently underway (June 2020). To be updated shortly.
