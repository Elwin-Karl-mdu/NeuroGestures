# Live EMG Hand Gesture Recognition

## Overview

This project investigates real-time hand gesture recognition using electromyography (EMG), digital signal processing and machine learning.

The system will be trained using EMG signals from the Ninapro DB2 dataset and evaluated using signals collected from new individuals with a Shimmer3R EMG unit.

The main focus is to investigate how signal processing affects classification accuracy and whether a trained machine learning model can recognize hand gestures in real time using a different EMG acquisition system.

This project is conducted as part of the Advanced Signal Processing course at Mälardalen University (MDU).

## Research Questions

- How should EMG signals be processed to achieve accurate gesture recognition?
- Can a model trained on an existing dataset recognize gestures from new individuals using different hardware?
- Can the system recognize gestures accurately with sufficiently low latency?

## Dataset and Data Acquisition

The machine learning model will be trained using the [Ninapro DB2 dataset](https://ninapro.hevs.ch/instructions/DB2.html). The channels that will be used is 9 and 10 from the EMG signals.

Experimental EMG signals will be collected using a Shimmer3R EMG unit with the following planned configuration:

- Number of channels: 2
- Sampling frequency: 2000 Hz
- Surface EMG electrodes

## Methodology

### Signal Processing

- Butterworth bandpass filter
- Notch filter
- Signal segmentation
- Time-domain feature extraction

### Feature Extraction

The following time-domain features are considered:

- Mean Absolute Value (MAV)
- Root Mean Square (RMS)
- Waveform Length (WL)
- Zero Crossings (ZC)
- Slope Sign Changes (SSC)

### Machine Learning

A machine learning model will be trained to classify hand gestures based on the extracted EMG features.

### Baseline and Comparison

Two approaches will be compared to investigate the impact of signal preprocessing on classification performance:

- **Baseline:** Classification using features extracted from EMG signals without additional filtering.
- **Proposed method:** Classification using features extracted from EMG signals processed with Butterworth bandpass and notch filters.

### Real-Time Recognition

EMG signals will be acquired from the Shimmer3R, processed and classified continuously. The predicted hand gesture will be displayed on a computer using text or images.

## Evaluation

The system will be evaluated based on:

- Gesture classification accuracy
- Classification performance with and without additional filtering
- Generalization to new individuals
- Real-time recognition latency

## Hardware and Software

### Hardware

- Shimmer3R EMG unit
- Surface EMG electrodes
- Computer

### Software

- MATLAB
- Signal Processing Toolbox
- Statistics and Machine Learning Toolbox
- Instrument Control Toolbox

## Expected Results and Demonstration

- Comparison of classification performance using filtered and unfiltered EMG signals.
- Visualization of EMG signals before and after preprocessing.
- Illustration of the experimental measurement setup.
- Live demonstration of hand gesture recognition.

## References

- [Ninapro DB2 Dataset](https://ninapro.hevs.ch/instructions/DB2.html)

## Project Status

Under development.

This is a project done with Emil Ekengren and Leopold Embring
