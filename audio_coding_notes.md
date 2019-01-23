# Notes from *Introduction to Digital Audio Coding and Standards*

## Chapter 1 - Introduction

* signal to noise ratio (SNR) is a decent measure of quality - the higher dB the better (90+ is good), but it doesn't account for perceptual quality
* ideally 18-20 bits for 2-5 kHz, otherwise 16 bits is ok
* coding errors
  * sampling errors - signal frequencies above half the sampling frequency are mirrored to lower frequencies causing aliasing, use a low-pass filter to remove them
  * quantization errors
    * overload errors - input signal range exceeds the range of the quantizer
	* round-off errors - always present, need to reduce it to inaudible levels
	* storage and transmission errors
* PCM is redudant, a "smart" coder allocates bits dynamically depending on the frequency content - more bits for more sensitive ranges

## Chapter 2 - Quantization

* quantization - mapping of continuous amplitude values into codes that can be represented with a finite number of bits
  * in sound context - conversion of sound from continuous signal amplitudes to discrete amplitudes
* quantization causes distortion (quantization noise), need to minimize it

### Uniform Quantization

* input amplitude range is split into equal parts
* midtread vs midrise quantizers - midtread allow -1 different codes (they pass 0 output) but yield better results
* if a value is below/above the min/max value, it will be fixed to said value - clipping
* quantization in general seems to be a complex topic, I'll be using WAVs which are already sampled and quantized

## Chapter 3 - Representation of Audio Signals

* dirac delta, fourier transform
* important properties of audio signals
  * bias <x> - average signal amplitude, generally 0 for audio
  * average power P - rate of energy in the wave
  * energy E - integral of power over time
  * standard deviation σ - average power after bias has been removed
* windowing function - multiplying a function in the time domain by this function
  * windowing to convert the function to a finite time interval introduces aliasing when using fourier transform - convolution theorem
  
## Chapter 4 - Time to Frequency Mapping Part 1: The PQMF

* frequency domain coding is generally better because you can adapt the amount of bits to encode each frequency component
* the basic technique is to split the signal into K different bands of frequencies using filter banks, signal from each band is then quantized with a limited number of bits, using less where it's less audible
* Z-transform - generalization of discrete time Fourier transform
* downsampling
  * downsampling by a factor of K - keep only every Kth sample
  * it causes aliasing
* upsampling
  * intersperse K-1 zeroes between each data point
  * it causes imaging
* perfect reconstruction filter banks - split signal into N channels using several (at least two) frequency bands, downsample by a factor of N and reverse the process to obtain an identical signal
  
## Chapter 5 - Time to Frequency Mapping Part II: The MDCT

* DFT and MDCT can both be used to create a perfect reconstruction transform coder
  * however, MDCT can be used without an increased data rate
