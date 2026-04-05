# NLU---Assignment-1

NLU Assignment: Supervised Sentiment Analysis
This assignment and associated bakeoff are devoted to supervised sentiment analysis using the ternary (positive/negative/neutral) version of the Stanford Sentiment Treebank (SST-3) as well as a new dev/test dataset drawn from restaurant reviews. The task involves implementing a baseline system and defining a model that performs effectively across both the movie review and restaurant datasets. Evaluation is based on the mean of the macro-F1 scores for the two datasets.

Model Architecture
The system utilizes a BERT-base model for tokenization and generating contextual token embeddings. These embeddings are fed into a bidirectional LSTM (BiLSTM) layer to capture sequential dependencies from both directions of the text. A classification head is applied to the final hidden state of the LSTM to produce the sentiment prediction.

Hyperparameter Optimization
To identify the most effective configuration, a systematic grid search was conducted. The optimization process focused on the following variables:

LSTM Hidden Dimension: Testing various sizes for the recurrent layers.

Number of Layers: Evaluating depth in the BiLSTM component.

Directionality: Comparing bidirectional vs. unidirectional LSTM performance.

Activation Functions: Testing different non-linearities for the classification head.

Evaluation and Generalization
The central objective is to develop a system that generalizes well beyond its training data. By training on SST-3 and assessing on restaurant reviews, the assignment tests the model's robustness against domain shift. Performance is measured using Macro-F1 to ensure high quality across all sentiment classes, regardless of distribution imbalances.
