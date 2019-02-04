# Exploring use of non-negative matrix factorization for lossy audio compression

This repository stores the research and report part of my Master's thesis.

The implementation part is visible [**here**](https://github.com/argoneuscze/AudioNMF).

## Assignment

The aim of this work is to research existing methods for lossy audio compression and to apply non-negative matrix factorization (NMF) in order
to improve the compression ratio without a noticeable loss in quality. Therefore, the goals are as following:

1. Become familiar with state of the art digital audio encoding and compression methods
2. Become familiar with non-negative matrix factorization, its properties and applications in digital audio processing
3. Design and implement a proof of concept audio codec utilizing NMF for audio compression, or extend an existing codec with this functionality
4. Find a suitable method for measuring perceived audio quality
5. Measure the resulting audio quality and compare the quality and compression ratio to existing solutions

## Structure

* Abstract
* Introduction
* Audio encoding
  * Digital audio
  * State of the art
	* MDCT, STFT
* NMF
  * Motivation
  * Application
* Codec design
* Implementation
* Evaluating results
* Conclusion

## TODO

* Abstract
* Introduction
* Research
* ...


## References TL;DR

* [The theory behind MP3](http://www.mp3-tech.org/programmer/docs/mp3_theory.pdf)
* [**OPUS CELT for music compression**](https://jmvalin.ca/papers/aes135_opus_celt.pdf)
* [OPUS SILK for voice coding](https://jmvalin.ca/papers/aes135_opus_silk.pdf)
* [Application of NMF to signal-adaptive audio effects](https://pdfs.semanticscholar.org/8e14/10a054d4b1aa5e2355bbd9dd7e04686f9e1b.pdf)
* [MP3 and AAC explained](https://www.iis.fraunhofer.de/content/dam/iis/de/doc/ame/conference/AES-17-Conference_mp3-and-AAC-explained_AES17.pdf)
* [**Introduction to Digital Audio Coding and Standards**](https://www.springer.com/gp/book/9781402073571)
* [Audio Coding - Theory and Applications](https://www.springer.com/gp/book/9781441917539)
* [Non-negative Matrix Factorization Techniques - Advances in Theory and Applications](https://www.springer.com/gp/book/9783662483305)
* [**Nonnegative Matrix Factorization: A Comprehensive Review**](https://ieeexplore.ieee.org/document/6165290)
* [The Why and How of Nonnegative Matrix Factorization](https://arxiv.org/pdf/1401.5226.pdf)
* [Introduction to Nonnegative Matrix Factorization](https://arxiv.org/pdf/1703.00663.pdf)
* [**Constrained Nonnegative Matrix Factorization with Applications to Music Transcription**](https://cs.uwaterloo.ca/sites/ca.computer-science/files/uploads/files/cs-2014-27.pdf)
* [Single-channel audio source separation with NMF: divergences, constraints and algorithms](https://hal.inria.fr/hal-01631185/document)
* [Spectral Audio Signal Processing](https://ccrma.stanford.edu/~jos/sasp/sasp.html)
* [Audio compression using Modified discrete cosine transform: The MP3 coding standard](https://www.mp3-tech.org/programmer/docs/jacaba_main.pdf)
* [Source Separation Tutorial Mini-Series II: Introduction to Non-Negative Matrix Factorization](https://ccrma.stanford.edu/~njb/teaching/sstutorial/part2.pdf)
* [**Object-based Audio Coding Using Non-negative Matrix Factorization for the Spectrogram Representation**](http://www.aes.org/e-lib/browse.cfm?elib=15380)