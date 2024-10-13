# SkimLit: Skimming Medical Literature Using Deep Learning

SkimLit is a deep learning project aimed at simplifying the understanding of medical research literature. It automatically classifies sentences from medical abstracts into specific categories like **Introduction**, **Conclusion**, **Results**, etc. This is especially useful in the medical domain, where comprehending complex abstracts quickly is essential.

## Objective
Medical literature is dense and often difficult to navigate. SkimLit helps by skimming abstracts and classifying sentences into sections, making it easier for researchers and practitioners to comprehend the structure of the paper.

## Dataset
The model is trained using the **PubMed 200k RCT** dataset:
- **PubMed 200k RCT: A Dataset for Sequential Sentence Classification in Medical Abstracts**  
  This dataset consists of medical abstracts with sentences labeled by their role (e.g., Background, Methods, Results, Conclusion).

## Model Architecture
The project implements a **hybrid deep learning model** which combines:
- **Bi-directional LSTM (Bi-LSTM)**: Captures contextual dependencies in sentences both forwards and backwards.
- **Feed-Forward Neural Network (FNN)**: Used for classification after sentence encoding.

For sentence embeddings, the model leverages:
- **Universal Sentence Encoder (USE)**: Pre-trained to generate meaningful sentence embeddings.
- **Positional Embeddings**: Adds the notion of sentence order and position in the abstract.

### Performance
The hybrid model achieves the following results:
- **Accuracy**: 83.46%
- **Precision**: 83.37%
- **Recall**: 83.46%
- **F1-Score**: 83.32%

These results were compared against other Artificial Neural Network (ANN) models, and the hybrid model outperformed them.

## Project Files
- **`helpers_utility.py`**: Contains helper functions used for data preprocessing, embedding generation, and model evaluation.
- **`SKIMLIT.ipynb`**: The main Jupyter notebook where the model is defined, trained, and evaluated.
- **`vectors.tsv`**: A file to visualize token embeddings for analysis purposes (can be used in TensorBoard).
- **`PubMed_200k RCT.pdf`**: The research paper detailing the dataset used for training the model.
- **`Neural Network for Joint Sentence Classification in Medical Paper Abstracts.pdf`**: The research paper that inspired and guided the implementation of the hybrid model.

## How to Run
1. Clone the repository and install required dependencies using `requirements.txt`.
2. Run the `SKIMLIT.ipynb` notebook to train the model and test it on the dataset.
3. Use TensorBoard to visualize embeddings using `vectors.tsv`.

## Future Work
- Explore attention mechanisms to enhance the model's ability to focus on important parts of the text.
- Experiment with transformer-based models for potentially improved performance.
- Test on other medical datasets to generalize the model.

## References
- [PubMed 200k RCT Dataset](https://github.com/wasiahmad/Clinical-Document-Classification)
- Neural Network for Joint Sentence Classification in Medical Paper Abstracts
