# CNN for sound classification
Feature extraction of sound signals along with complete CNN model fitting and evaluations.

<b>Note:</b> Uncomment the MFCC extraction block to work with your own sounds. Otherwise, I have also provided a dummy dataset i.e. <b>dataset.npy</b>.

# About dataset.npy
1. Cepstral Coefficients of dimension (178,44,13) where 178 are number of audio, 44 is the number of samples for each audio and 13 are number of Coefficients.

2. Labels of dimension (178,)

## Using Librosa for Feature Extraction
Generates 13 MFCCs (Columns), 44 Samples (Rows) for each sound signal and a Target column (Label) in addition to 13 MFCCs. (Review the dataset.csv to have an idea about shape of final data)
### REVIEW THE GRAPHS BELOW

## Quick guide
1. For each type of sound, create a directory or folder in the audio/ directory.<br>
2. To see what I mean by that, explore the audio folder in this repository. I have placed an audio as an example.<br>
3. After you are done making directories for sounds,
<br/>place this script in the directory as I have placed it in this repository.

### Following is the sequence of transitions that the signal goes through until MFCCs are generated

### Waveform
![Waveform](https://user-images.githubusercontent.com/62377713/119189223-3bbbf800-ba95-11eb-8466-3dcc76ce8e4a.PNG)
### Fourier Transform
![FFT](https://user-images.githubusercontent.com/62377713/119189293-51312200-ba95-11eb-8935-f3240ca3eec9.PNG)
### Power Spectrum
![Power Spec](https://user-images.githubusercontent.com/62377713/119189299-52fae580-ba95-11eb-86ee-e61b8a671b09.PNG)
### Spectrogram
![spec](https://user-images.githubusercontent.com/62377713/119189290-4ffff500-ba95-11eb-9aa3-ce0d1c312af1.PNG)
### Log Spectrogram
![log spec](https://user-images.githubusercontent.com/62377713/119189295-51c9b880-ba95-11eb-8a25-22ba17a0a898.PNG)
### MFCCs (Mel Frequency Cepstral Coefficients)
![MFCCs](https://user-images.githubusercontent.com/62377713/119189297-52624f00-ba95-11eb-909c-18b32687b2ee.PNG)

## Key points
1. This code rejects the audio signals having lower sample rate than 22050. <br>
2. Number of MFCCs selected are 13.
3. Hop length across the signal is 512.
4. Number of fast fourier transformation is 2048.

