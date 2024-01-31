# Deepfake-Detection
------------------

## Abstract
Abstract—With the continuous development of Generative models on face generation, how to distinguish the real and fake face has become an important problem for security. Because of the continuous improvement on the detection accuracy by facial physiological signals, video face forgery detection based on facial physiological signal analysis has received more and more attention, which has become an important research branch in the field of face forgery detection. Currently, most of the research on forgery detection based on physiological signal analysis use biometric features such as blinking patterns, head swings, heart rate signals, and lip movements. However, there hasn't been much exploration on the usage of gaze features in face forgery detection. Through the analysis of gaze directions in face videos, we have observed differences in the distribution of gaze direction pattern between the real and forged videos. Specifically, real videos tend to have more concentrated gaze distribution within a short period of time, while forged videos have more dispersed gaze distributions. In this paper, we present a novel Deepfake gaze analysis method named DFGaze, to explore spatial-temporal gaze inconsistency for video face forgery detection. Our method uses the gaze analysis model (GAM) to analyze the gaze features of face video frames, and then applies a spatial-temporal feature aggregator to realize authenticity classification based on gaze features. In order to better mine the authenticity clues in the videos, we further use the texture analysis model (TAM) and attribute analysis model (AAM) to improve the representation ability of spatial-temporal feature differences between real and forged faces. Extensive experiments show that our method can achieve state-of-the-art performance with the help of gaze analysis. The source code is available at https://github.com/ziminMIAO/DFGaze.
The framework of our proposed method.
![Uploading image.png…]()


## Install & Requirements
The code has been tested on pytorch=1.8.0 and python 3.7, please refer to `requirements.txt` for more details.
### To install the python packages
`python -m pip install -r requirements.txt`


## Dataset
1.In our experiment we use FaceForensics++, WildDeepfake,CelebDF and DFDCP datasets for evaluation.
2.Please divide the video into groups of 32 frames each and put them in the correct path as following.

├─FaceForensics++
│  ├─test
│     ├─fake
│     │  ├─video_1
│     │  ├─video_2
│     │  ├─.....
│     │  ├─video_n
│     ├─real
│     │  ├─video_1
│     │  ├─video_2
│  │  │  ├─.....
│     │  ├─video_n
├─train
│  │  ├─fake
│  │  │  ├─video_1
│  │  │  ├─video_2
│  │  │  ├─.....
│  │  │  ├─video_n
│  │  ├─real
│  │  │  ├─video_1
│  │  │  ├─video_2
│  │  │  ├─.....
│  │  │  ├─video_n



datasets
├── augment_deepfake        (2)
│   ├── fake
│   │   └── frames
│   ├── real
│   │   └── frames
│   └── val
│       ├── fake
│       └── real
├── base_deepfake           (1)
│   ├── fake
│   │   └── frames
│   ├── real
│   │   └── frames
│   └── val
│       ├── fake
│       └── real
├── both_deepfake           (3)
│   ├── fake
│   │   └── frames
│   ├── real
│   │   └── frames
│   └── val
│       ├── fake
│       └── real
├── precomputed             (4)
└── T_deepfake              (0)
    ├── manipulated_sequences
    │   ├── DeepFakeDetection
    │   ├── Deepfakes
    │   ├── Face2Face
    │   ├── FaceSwap
    │   └── NeuralTextures
    └── original_sequences
        ├── actors
        └── youtube
## Pretrained Model
we provide some [pretrained model](https://pan.baidu.com/s/16HvIPHeEm8EF2KphnCOebw) (code:lasy)based on FaceForensics++. And we also provide a [Google Drive link](https://pan.baidu.com/s/16HvIPHeEm8EF2KphnCOebw).


## Usage
**To train a model**

`python train.py`
(Please set the arguments after read the code)

## About
If our project is helpful to you, we hope you can star and fork it. If there are any questions and suggestions, please feel free to contact us.

Thanks for your support.
