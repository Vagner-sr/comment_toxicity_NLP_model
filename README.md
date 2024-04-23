# Toxicity Detection Project

This project aims to classify text comments into different toxicity categories using machine learning techniques. The goal is to provide a model that can accurately predict whether a given comment contains toxic content, such as insults, threats, or hate speech.

## About the Project
The dataset used contains text comments along with labels indicating the presence of various types of toxicity, including toxic, severe toxic, obscene, threat, insult, and identity hate. We use these labels to train a model to classify comments into these categories.

## Insights Obtained
During the exploratory data analysis, we obtained several valuable insights:

1. **Effect of Text Features**: Certain words and phrases are strong indicators of toxic content in comments.
2. **Impact of Model Architecture**: Different model architectures and hyperparameters affect the model's performance on toxic comment classification.

## Results of the Best Model (Bidirectional LSTM)
After training various models, the best performing model was a Bidirectional LSTM with the following architecture:

- Embedding Layer: Input dimension of 200001, output dimension of 32.
- Bidirectional LSTM Layer: 32 units with tanh activation.
- Fully Connected Layers: 128, 256, and 128 units with ReLU activation.
- Output Layer: Dense layer with sigmoid activation for multi-label classification.
- 
### Model Results:
- **Mean Absolute Error (MAE)**: 0.0617
- **Validation Loss**: 0.0496
- **Precision**: 0.864
- **Recall**: 0.625
- **Accuracy**: 0.467
These results indicate that the Bidirectional LSTM model is capable of effectively detecting toxicity in comments, with good precision and recall.

## Conclusion
This project provides insights into the detection of toxic content in text comments and offers a precise model for multi-label classification. The results can be useful for platforms and communities to automatically moderate comments and maintain a safe environment for users.

### Usage
To use this model for toxicity detection, you can interact with the provided Gradio interface. Simply input a comment into the textbox and the model will predict whether it contains toxic content.
