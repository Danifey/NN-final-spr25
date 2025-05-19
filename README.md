# Neural networks final spring25

## Research insights

We will be working on a CNN classification model for video in order to identify animal behaviors.

## Research Insights

From our research, working with video data has several general approaches:

### 2D Network Architectures
2D network architectures process each frame in the video as its own still image. This type of CNN cannot learn from **temporal information**—data gleaned from movement between frames over a segment of video. Temporal information is processed in a dedicated layer that aggregates outcomes from individual frames.

### 3D Network Architectures
3D network architectures are capable of learning from temporal information within a single block of nodes. These nodes include a variable for the **number of frames** in the input, representing time elapsed. This enables simultaneous processing of spatial and temporal data.

### 2+1D Network Architectures
This architecture separates spatial and temporal data processing by alternating a 2D layer (responsible for spatial data) with a single-dimensional layer (focused on temporal information). From our research, this architecture proved to be the **most effective** for behavior classification on video data (Du Tran et al.).

## Implementation Exploration

In addition to researching the architecture we wanted to use for this problem, we also found a practical guide for implementing **2+1D networks** using TensorFlow:

- TensorFlow Practical Guide: [https://www.tensorflow.org/tutorials/video/video_classification](https://www.tensorflow.org/tutorials/video/video_classification)

## Key Reference

@misc{tran2018closerlookspatiotemporalconvolutions,
      title={A Closer Look at Spatiotemporal Convolutions for Action Recognition}, 
      author={Du Tran and Heng Wang and Lorenzo Torresani and Jamie Ray and Yann LeCun and Manohar Paluri},
      year={2018},
      eprint={1711.11248},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/1711.11248},
}

[Read the full paper](https://arxiv.org/pdf/1711.11248v3)
