# Genre Classification of Harmonic and Percussive Components with Deep Embeddings

This repository contains the code and resources for the study on **Music Genre Classification** using **harmonic and percussive components** extracted from separated audio signals. The project explores the impact of source separation preprocessing on genre classification performance.


## Table of Contents

- [Overview](#overview)
- [Key Features](#keyfeatures)
- [Dataset](#dataset)
 
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)


## Overview

The primary goal of this project is to investigate how music genre classification can be improved by separating audio signals into harmonic and percussive components. The classification is performed using embeddings extracted from pre-trained models and Support Vector Machine (SVM) classifiers.


### Key Features:
- **Source Separation**: Audio signals are decomposed into stems (drums, bass, vocals, others) using **Demucs v.4**.
- **Feature Extraction**: Employs pre-trained **Essentia-TensorFlow** models (VGGish, MusiCNN, EffNet) for deep embeddings.
- **Genre Classification**: Utilizes SVMs, including optimized versions, to classify genres from features.






## Dataset:
- **GTZAN Dataset**: A widely used dataset for music genre classification.
- Comprises 1,000 audio clips (10 genres, 30 seconds each).
- Extended datasets created:
  - **Percussive GTZAN**: Combines drums and bass stems.
  - **Harmonic GTZAN**: Combines vocals and others stems.


The dataset used for this project is the **GTZAN Music Genre Dataset**, which is publicly available on Kaggle. The dataset can be accessed [here](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification).

This dataset consists of 1,000 audio tracks categorized into 10 music genres. It is commonly used for music genre classification tasks.

For more information on how to use this dataset, please refer to the Kaggle page linked above.

## Methods

1. **Source Separation**:
   - Decomposed using **Demucs v.4** to produce four stems.
   
2. **Feature Extraction**:
   - Embedding models:
     - **MusiCNN**
     - **EffNet**
     - **VGGish**
   - Extract features from segments of 30-second audio clips.

3. **Genre Classification**:
   - Applied SVM classifiers (basic and optimized) to the extracted features.


## Results





## Results

<img src="results.png" width="500" height="300"/>

- The best results were achieved using **EffNet** with an optimized SVM.
- Genre classification is possible even when only harmonic or percussive components are available, with minor accuracy trade-offs.

### Accuracy Highlights:
| Model      | Dataset         | SVM      | Accuracy |
|------------|-----------------|----------|----------|
| EffNet     | Normal          | Optimized| 98%      |
| MusiCNN    | Percussive      | Optimized| 83%      |
| MusiCNN    | Harmonic        | Optimized| 83%      |



The findings demonstrate that **deep embeddings** combined with **SVMs** are effective for music genre classification. Furthermore, the use of harmonic and percussive components opens up new possibilities for specialized classification systems.


## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request. Contributions are welcome!

## License


This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
