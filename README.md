# TASLP2019
The code for multi-channel speech enhancement which will be published in TASLP2019.
  - FCA is a method for general source separation. In fact, it can be available only for speech enhancement because of the strong initial value dependency.
  - MNMF is a general source separation method which integrate NMF-based source model into FCA.
  - MNMF-DP is a method which integrates deep speech prior into MNMF, and is for speech enhancement.
  - ILRMA and ILRMA-DP will be updated soon.

## Requirement
* Tested on Python3.6
* numpy
* pickle
* librosa
* soundfile
* progressbar2
* chainer (6.1.0 was tested) (for MNMF-DP, ILRMA-DP)
* cupy (6.1.0 was tested) (for GPU accelaration)

## Usage
```
python3 MNMF_DP.py [input_filename] --gpu [gpu_id]
```
Input is the multichannel observed signals.  
If gpu_id < 0, CPU is used, and cupy is not necessary.


<!-- ## Citation
If you use my code in a research project, please cite the following paper:

Kouhei Sekiguchi, Aditya Arie Nugraha, Yoshiaki Bando, Kazuyoshi Yoshii:  
[Fast Multichannel Source Separation Based on Jointly Diagonalizable Spatial Covariance Matrices](https://arxiv.org/abs/1903.03237),  
arXiv preprint arXiv:1903.03237, 2019 -->
