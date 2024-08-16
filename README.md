# CODXO_Translation_App_Using_Seq2Seq_Attention_PyTorchModel

## Overview

This repository contains an English-to-Urdu translation application built using a Sequence-to-Sequence (Seq2Seq) model with Gated Recurrent Units (GRU) and Bahdanau Attention mechanism. The model is trained on a diverse dataset comprising 25,000 English-to-Urdu sentence pairs, covering various topics including general conversations, culture, politics, science, religion, literature, and more.

## Table of Contents

- [Introduction](#introduction)
- [Model Architecture](#model-architecture)
- [Attention Mechanism](#attention-mechanism)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to bridge the language gap between English and Urdu by providing a robust translation model. Leveraging the Seq2Seq architecture with Bahdanau Attention, the model effectively captures the nuances of both languages, ensuring accurate and context-aware translations.

## Model Architecture

The core of this translation model is a Seq2Seq architecture, which is composed of an Encoder and a Decoder. The Encoder processes the input sentence and compresses it into a context vector, while the Decoder generates the corresponding translation in Urdu.

### Encoder
- **GRU Layers**: The Encoder uses GRU layers to capture the temporal dependencies in the input sequence.
- **Embedding Layer**: The input tokens are first passed through an embedding layer, which converts them into dense vectors of fixed size.

### Decoder
- **GRU Layers**: Similar to the Encoder, the Decoder also utilizes GRU layers to process the context vector and generate the output sequence.
- **Attention Layer**: The Bahdanau Attention mechanism is applied between the Encoder and Decoder, allowing the model to focus on relevant parts of the input sequence while generating each word in the output.

## Attention Mechanism

The Bahdanau Attention mechanism enhances the translation by allowing the Decoder to dynamically attend to different parts of the input sequence at each step of the output generation. This mechanism is crucial for handling longer sentences and ensuring that the context is appropriately captured during translation.

## Dataset

The model is trained on a dataset of 25,000 English-to-Urdu sentence pairs. The dataset is highly diverse, covering a wide range of topics:
- **General Conversations**: Everyday dialogues and common phrases.
- **Cultural Expressions**: Sentences reflecting cultural contexts specific to Pakistan.
- **Political and Economic Terms**: Sentences related to governance, economics, and policy.
- **Scientific and Technical Terms**: Sentences from the domains of science and technology.
- **Literature and Poetry**: Sentences reflecting the rich literary tradition of Urdu.

## Installation

To set up the environment and run the model, follow these steps:

1. Clone the repository:
    ```bash
    https://github.com/HashamAkram18/CODXO_Translation_App_Using_Seq2Seq_Attention_PyTorchModel.git
    cd english-to-urdu-translation
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv E_to_U
    source venv/bin/activate
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

After setting up the environment, you can use the pre-trained model to translate English sentences into Urdu.

```python
from translation import translate_sentence

sentence = "The weather is nice today."
translation = translate_sentence(sentence)
print(translation)
```

## Training

To train the model on your own dataset, follow these steps:

1. Prepare your dataset in the required format (CSV file with English and Urdu columns).
2. Configure the training parameters in the `config.py` file.
3. Run the training script:
    ```bash
    python train.py
    ```

## Evaluation

The model can be evaluated on a test set by running the evaluation script. This script will output metrics such as BLEU score and accuracy, providing insights into the model's performance.

```bash
python evaluate.py
```

## Results

The model has achieved the following results on the test set:
- **BLEU Score**: COMMING SOON
- **Accuracy**: >98 (~Overfitting)

The results demonstrate the model's ability to handle diverse and complex translations, making it a valuable tool for both casual and professional use.

## Future Work

- **Dataset Expansion**: Expanding the dataset to include more specialized domains such as medical, legal, and technical translations.
- **Model Optimization**: Exploring more advanced architectures like Transformer-based models for further improving translation accuracy.
- **Deployment**: Deploying the model as a web service for broader accessibility.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas or report bugs.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

