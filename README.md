# Delay Network-based Artificial Reverberators 
List of papers and code on delay-network-based artificial reverberation.  

This repository comes from a need to make some clarity on previous literature on delay-network-based artificial reverberators, in particular, feedback delay networks (FDN) and scattering delay networks (SDN). The goal is to keep updating this repository as we keep progressing in this field. 

## Feedback Delay Networks 
| **Reference** | **Year** | **Content Type** | **Main Contributions** | **Code** | **Notes** |
| :------------------------ | :--------------: | :------------------ | :------------------ | :-------------------------------- | :-------------------------------------------------------- | 
| S. J. Schlecht and E. A. P. Habets, “Time-varying feedback matrices in feedback delay networks and their application in artificial reverberation,” The Journal of the Acoustical Society of America, vol. 138, no. 3, pp. 1389–1398, Sept. 2015 | 2015 | Informed design | Introduce time-varying feedback matrices to modulate pole locations to break temporal patterns, and model air movement | NA | Practical considerations on time-varying FDNs in [this](https://aes2.org/publications/elibrary-page/?id=17679) paper | 
| S. J. Schlecht and E. A. P. Habets, “Feedback Delay Networks: Echo Density and Mixing Time,” IEEE/ACM Transactions on Audio, Speech, and Language Processing, vol. 25, no. 2, pp. 374–383, Feb. 2017 | 2017 | Theory and analysis | Explains the concepts of echo density and mixing time and how these are affected by the parameters of FDNs, which a focus on delay lenths | NA | NA | 
| S. J. Schlecht and E. A. P. Habets, “Accurate Reverberation Time Control in Feedback Delay Networks,” Proceedings of the International Conference on DAFx | 2017 | Attenuation fitlers optimization | Constrained nonlinear least-squares optimization problem align the attenuation filters with the target reverberation time across frequencies | NA | Requires target RT | 
| K. Prawda, V. Välimäki, and S. Schlecht, “Improved reverberation time control for feedback delay networks,” Proceedings of the International Conference on DAFx | 2019 | Attenuation filters optimization | Presents a GEQ design that incorporates an additional high-shelf filter. Proposes an optimization method based on a frequency-dependent weighting matrix | NA | Requires target RT |
| S. J. Schlecht and E. A. P. Habets, “Modal Decomposition of Feedback Delay Networks,” IEEE/ACM Transactions on Audio, Speech, and Language Processing, vol. 67, no. 20, pp. 5340–5351. 2019 | 2019 | Theory and analysis | Discusses the connection between the FDN's modal representation and its parameters. Presents a pole finding algorithm | NA | NA | 
|S. J. Schlecht and E. A. P. Habets, “Scattering in Feedback Delay Networks,” IEEE/ACM Transactions on Audio, Speech, and Language Processing, vol. 28, pp. 1915–1924 | 2020 | Informed design | Generalizes the feedback matrix to arbitrary lossless **filter** feedback matrices to increase echo density | .. | Presents the velvet feedback matrix which can create ultra-dense impulse responses at a minimal computational cost | 
| S. J. Schlecht, J. Fagerström, and V. Välimäki, “Decorrelation in Feedback Delay Networks,” IEEE/ACM Trans. Audio Speech Lang. Process., vol. 31, pp. 3478–3487 | 2023 | Theory and Analysis | Analysis of multichannel correlation induced by FDNs | - | -
| V. Välimäki, K. Prawda, and S. J. Schlecht, “Two-Stage Attenuation Filter for Artificial Reverberation,” IEEE Signal Processing Letters. | 2024 | Informed design of attenuation filters | SOTA design consisting of a first-order low-shelf filter and one-third-octave GEQ | - | Uses the [J. Liski's GEQ](https://www.dafx17.eca.ed.ac.uk/papers/DAFx17_paper_94.pdf)
| .. | .. | .. | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 

### FDNs for Spatial Audio
| S. J. Schlecht and E. A. P. Habets, “Sign-Agnostic Matrix Design for Spatial Artiﬁcial Reverberation with Feedback Delay Networks,” | 2018 | .. | .. | NA | NA | 

### Toolbox and libraris 
| **Reference** | **Description** | **Repository** |
| :------------------------ | :--------------: |  :--------------: | 
| S. J. Schlecht. "FDNTB: The feedback delay network toolbox." International Conference on Digital Audio Effects. DAFx, 2020. | The most comprehensive library on FDNs currently available. Provides a selection of special feedback matrices,  topologies, and attenuation filter. Include modal decomposition algorithm. Many examples where to start from. Written in Matlab. | [fdnToolbox](https://github.com/SebastianJiroSchlecht/fdnToolbox) | 


## Scattering Delay Networks
| **Reference** | **Year** | **Parameter Design** | **Application** | **Code** | **Notes** |
| :------------------------ | :--------------: | :------------------ | :------------------ | :-------------------------------- | :-------------------------------------------------------- | 
| De Sena, Enzo, et al. "Efficient synthesis of room acoustics via scattering delay networks." IEEE/ACM Transactions on Audio, Speech, and Language Processing 23.9: 1478-1492. | 2015 | Informed | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 
| .. | .. | .. | .. | NA | NA | 


## Early Reverbs
| **Reference** | **Year** | **Notes** |
| :------------------------ | :--------------: |  :--------------: | 
| M. R. Schroeder and B. F. Logan, “Colorless artificial reverberation,” J. Audio Eng. Soc., vol. 9, no. 3, pp. 192–197, Jul. | 1961 | Cascade of allpass filters |
| M. R. Schroeder, ``Natural-sounding artificial reverberation,'' Journal of the Audio Engineering Society, vol. 10, no. 3, pp. 219-223 | 1962 | Combination of parallel comb filters with series allpass filtes. Known as the **Schroeder reverb** |
| M. A. Gerzon, “Synthetic stereo reverberation, parts I and II,” Studio Sound, vol. 13(I), 14(II), pp. 632–635(I), 24–28(II). | 1971(I), 1972(II) | Feedback delay network - multichannel allpass reverberator | 
|  J. A. Moorer, "About this reverberation business," Computer music journal, 13-28. | 1979 | Introduces lowpass filters within comb filters to model high frequency damping. Uses a sparse FIR filter to model early reflections | 
| J. Stautner and M. Puckette, “Designing Multi-Channel Reverberators,” Computer Music Journal, vol. 6, no. 1, p. 52 | 1982 | "Consolidates" Gerzon's reverb | 
| W. G. Gardner, “A real-time multichannel room simulator,” J. Acoustical Society of America, vol. 92, no. 4, pp. 1 – 23 | 1992 | Nested allpass filters |
| W. G. Gardner, ``The virtual acoustic room,'' Master's thesis, MIT | 1992 | Diffuse reverberators for small/medium/large rooms, based on nested allpass filters |
| J.-M. Jot and A. Chaigne, “Digital delay networks for designing artificial reverberators,” in Proc. 90th Conv. Audio Eng. Soc., Paris, France, Jan. |1991 | Introduces the concept of delay-proportional attenuation filters |
| J.-M. Jot, “An analysis/synthesis approach to real-time artificial reverberation,” presented at the Proc. ICASSP, pp. 221–224 | 1992 | Explains how to design attenuation and tone corrector filters from a target RIR |
| Dattorro, J. Effect design, part 1: Reverberator and other filters. J. Audio Engineering Society, 45, 660–684. | 1997 | Tutorial-like paper with coplete design with coefficent values and practical insights |
| .. | .. | .. |


### Other resources: 

Sean Costello "[Getting started with reverb design](https://valhalladsp.com/2021/09/22/getting-started-with-reverb-design-part-2-the-foundations/)", blog post

### Acknoledgements 

This list is highly inspared by 
- Schlecht, S. J. Feedback Delay Networks in Artificial Reverberation and Reverberation Enhancement. PhD Thesis, Friedrich-Alexander-Universitaet Erlangen-Nuernberg (Germany), 2018.
- Alary, B. "Analysis and Synthesis of Directional Reverberation." PhD Thesis, Aalto University, 2021
- Valimaki, V., Parker, J. D., Savioja, L., Smith, J. O., & Abel, J. S. (2012). Fifty years of artificial reverberation. IEEE Transactions on Audio, Speech, and Language Processing, 20(5), 1421-1448.