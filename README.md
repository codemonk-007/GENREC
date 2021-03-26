# GENREC

## Gender Recognition Algorithm

Automatic gender identification from speech is an important problem with many applications including speaker identification, speaker segmentation, and personalising human-machine interactions. Knowledge of gender can be used for normalisation of speech features, which has been shown to decrease word error rate in speech recognition. Gender identification can improve the prediction of other speaker traits such as age and emotion, either by jointly modelling gender with age (or emotion) or in a pipelined manner. Speaker verification systems also implicitly or explicitly use gender information.

## Proposed Concept 

A typical approach to identifying gender (or other speaker traits) is to compute summary statistics of the speech features (pitch or spectral), such as mean, maximum, minimum, and use these statistics as features in gender classification models. One of the major features that holds useful information of the
speech utterance is the fundamental frequency of the voice sample. The fundamental frequency or F0 is the frequency at which vocal chords vibrate to produce voice sounds. Pitch of a sound is very often used to represent the perception of fundamental frequency. Typically Fundamental Frequencies lie roughly in the range 80 to 450 Hz, with males having lower frequencies than female and children. The F0 or the fundamental frequency is not stationary but constantly changes in a sentence. Thus with this, fundamental frequency can be used to signify emphasis.

## Methodology 

1.Male average F0 Calculations: We calculate the F0 frequencies of all the male labelled samples and then take their average. This will represent the average Male F0.

2.Female average F0 Calculations: We calculate the F0 frequencies of all the female labelled samples and then take their average. This will represent the average Female F0.

3.Testing gender prediction: We use the average Male and Female F0 calculated in step 1 and test prediction of male gender by analysing closest distance between the
fundamental frequencies. The F0 calculated for the voice sample closer to avg. Male F0 will be tagged as Male and that closer to avg. Female F0 will be tagged as Female.

4.Combining Test Results: This is an auxiliary step where we combine the prediction data into a data frame.

5.Checking Accuracy: Using the combined data , we calculate the accuracy my comparing the prediction label with the initial data label.

6.Creating Frequency statistics: From the calculated fundamental frequencies we then find the summary statistics ,ie., the Mean F0, Minimum F0, Maximum F0.

Observations :

![image](https://user-images.githubusercontent.com/81297719/112602002-25990f00-8e39-11eb-9875-e6fbe3e19fe3.png)
