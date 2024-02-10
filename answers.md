
## Intro Questions
1. You can hear most of what is said at $1500$ Hz. At $2500-3000$ its clear enough. It was a bit hard to interpret "medicine" from the female voice. 

2. I think it starts sounding pretty bad below $4000$ Hz.

3. At $8$ kHz we can capture frequencies as high as $4$ kHz. Connecting to the previous exercise, It seems that this sampling frequency is high enough to be able to understand what is being said, but still quite low. I think this is done to save some resources, especially since it's "old" telephony.

## Voiced and Unvoiced Speech Sounds
2. High pitch region: $5$ peaks in $6ms -> 833$ Hz. Low pitch region: $10$ peaks in $40ms -> 250$ Hz (Maybe it's supposed to be $~125$ Hz, which is more typical for a male).

3. Plot

4. $$X[3] = \sum_{m=1}^{N-1} x_m e^{{-j6 \pi m}/n}$$

With 8 kHz sampling rate and $N = 256$ sampling points, we have a frequency resolution of $8$ kHz $/N = 31.25$ Hz. The frequency at $X[3]$ is then $3 \cdot 31.25 = 93.75$ Hz.

5. I find the index of the maximum of the DFT to be $7$. So the fundamental is $7$ times the resolution $= 218.75$ Hz. This is within the range of voiced speech so it seems reasonable.

6. Keeping the frame length short is important for computational efficiency, but if it's too low we might not be able to find the correct fundamental frequency. In this case, the fundamental lies in the frequency bin of $31.25$ Hz around $93.75$ Hz ($97.75 \pm 15.625$). I think this is a reasonable frame length. 
7. The resulting spectrum is pointier when using a boxcar. The average magnitude of the new spectrum is also larger and it has no negative values (in log scale). This is reasonable because the Hanning window tapers the edges of the signal, removing energy.
  9. $$c(3) = (x \ast y)(3-N+1) = \sum_{l=0}^{|| x ||-1} x_l y_{l-3+N-1}^{\ast}$$
  signal.freqz computes the frequency response of the filter. Parameters are:

  numerator b = 1

  denominator a = 1 (default)

  N = 1024 (computed at 1024 frequencies)

  whole = True (computed from 0 to Nyquist frequency) 

  fs = 44100

  w = frequency points

  h2 = response

  Multiplication by $e$ simply shifts the envelope vertically. It seems to follow the magnitude of the signal spectrum better this way.

  10. ? 
  11. ?

## Formants
 
2.

## Phonemes and Allophones
1.
2.
3. A diphthong is two vowels after each other. 
4. 44
5. A phone is any distinct unit of speech sound/ a realization of speech sound. An allophone is a variation or a different pronunciation of a phoneme. It seems like it's hard to determine exactly how many allophones there are because there are so many variations of sounds (of the same phonemes).

## The Spectrogram

## Vocoder
