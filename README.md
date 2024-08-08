# Bangla-Voice-Based-Access-Control-for-Hall-Dining

We present a Bangla voice-based access control system. The system will take speech signal as input from  a user and cross-check with previously recorded inputs from different users. When the system finds a suitable match, it gives a decision on whether the person should be given access or not. The idea is to first extract useful features from raw speech data taken from different users. The technique that is used to extract these features is Mel-Frequency Cepstral Coefficients algorithm which involves calculating coefficients from user audio data that is unique to each user. Then these coefficients are compared with new MFCC coefficients extracted from audio data from a new user using Dynamic Time Warping (DTW) Algorithm. The comparison that yields the minimum value of all DTW comparisons is considered as the match.

Speech recognition has become an increasingly popular concept over the years because it provides an option to detect human voice and convert it into machine-readable format for further use. One of the many advantages of speech recognition is the ability to distinguish one person’s voice from another person’s voice. This feature allows us to build automated systems that can readily take a person ’ s voice as input and compare with other voice data and reach a decision. These   are generally referred to as ‘Automated Speaker Recognition’ systems. There are two stages to such systems, one is identification and the other is verification. In an identification system, the user is asked to first give an input voice data. At this stage, the user claims to be a person. In the verification system, the system tries to verify whether his claim is true.    In essence, it is a 1 to 1 match. But the system compares 1 datum to previously stored N number of data.
The total workflow of this paper is subdivided into three parts: a) Collecting voice data of different users and storing them in a database, b) Taking voice data of new user as input and performing feature extraction techniques, c) Comparing the features of previously stored voice data and new data leading to a conclusion on accessibility. While going through these proceedings, these techniques were used:

**(a)	Processing Before Extracting Features:** An end point detection algorithm is used to separate the main energy content of the signal from the rest. It sets a threshold below which it considers audio amplitude as non-voice or unvoiced data. Then it goes over the whole signal and tries to identify which regions in the raw audio data can be considered useless. It basically gives a noise removed, or silence removed signal from the raw audio data.

**(b)	Feature Extraction:** This is the heart of speech or speaker recognition systems. The silence removed signal is not of much use since a classifier cannot be used directly
 to distinguish speech signals. First, some discrete values representing the silence removed signals, or the energy to be exact need to be generated and then classifiers can be applied to them. There are many feature extraction techniques like Linear Predictive Coding (LPC), Perceptual Linear Prediction (PLP), Relative Spectral (RASTA), Discrete Wavelet Trans- form (DWT), Wavelet Packet Transform (WPT), Probabilistic Linear Discriminate Analysis (PLDA), and Mel-Frequency Cepstral Coefficient (MFCC). In this paper, Mel-Frequency Cepstral Coefficient (MFCC) is used.

**(c)	Classifiers:** The final part is to use a classifier to measure the similarity and dissimilarity between the coefficients and therefore the speech signals. For classification, various tech- niques are available like Gaussian Mixture Model (GMM),  Hidden Markov Model (HMM), Artificial Neural Network (ANN), Dynamic Time Warping (DTW), Vector Quantization (VQ) models, Support Vector Machine (SVM), and Nearest Neighbor (NN). In this paper, Dynamic Time Warping (DTW) method is used.

## Team
### Students:
- Rifah Ahmed Maisha (github - https://github.com/rifah057) 
- Zunaid Mohammad

### Supervisor:
- Dr. Abul Kalam Azad (Professor, EEE, DU)
