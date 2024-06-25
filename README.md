# Auto Essay Scoring

Project designed to automatically score essays on a scale from 1 to 6 using a fine-tuned DeBERTa v3 base model. This repository provides the necessary code and resources to train the model using the PEFT (Parameter-Efficient Fine-Tuning) method, specifically with LoRA (Low-Rank Adaptation). The dataset used for training is sourced from Kaggle.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model](#model)
- [Fine-Tuning](#fine-tuning)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to provide an automated essay scoring system that assigns a score between 1 and 6 to input essays. The system leverages the DeBERTa v3 base model, which is fine-tuned using the PEFT approach with LoRA.

## Dataset

The dataset used for training the model is sourced from Kaggle. It contains a collection of essays with corresponding scores ranging from 1 to 6.

## Model

The DeBERTa (Decoding-enhanced BERT with disentangled attention) v3 base model is used as the base model for this project. DeBERTa is known for its state-of-the-art performance on various natural language understanding tasks.

- Model link: [DeBERTa v3 base dataset on Kaggle](https://www.kaggle.com/datasets/jonathanchan/deberta-v3-base)

## Fine-Tuning

We fine-tune the DeBERTa v3 base model using the PEFT method with LoRA. LoRA allows for efficient adaptation of pre-trained models to specific tasks with minimal additional parameters.

## Installation

To get started with the Auto Essay Scoring project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/auto-essay-scoring.git
    cd auto-essay-scoring
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Preparing the Data:**

    Download the dataset from Kaggle and place it in the `data` directory:
    ```bash
    mkdir data
    # Place the downloaded dataset files in the data directory
    ```

2. **Training the Model:**

    To train the model using the provided scripts, run:
    ```bash
    python train.py --config configs/train_config.json
    ```

3. **Scoring Essays:**

    Once the model is trained, you can score new essays using:
    ```bash
    python score.py --input essay.txt
    ```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue if you have any suggestions or improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to customize this `README.md` file as per your requirements. If you have any questions or need further assistance, please open an issue or contact the repository maintainers.
