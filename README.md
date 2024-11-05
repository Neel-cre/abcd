# A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK

PHASE-1:-

Project Overview:-
This project implements a Long Short-Term Memory (LSTM) network for recognizing emotions from text dialogues. The model also incorporates speaker information, allowing it to learn patterns related to who is speaking, in addition to the textual content. The ultimate goal is to predict the emotion associated with a sequence of text while utilizing speaker features to improve classification accuracy.

The four emotion classes used in this task are:

Angry, 
Happy, 
Neutral, 
Sad


Dataset:-
you can directly load the dataset from hugging face 

from datasets import load_dataset
# Load the dataset
dataset = load_dataset("Zahra99/IEMOCAP_Text")

The dataset contains 5 sessions which include dialogues, with each dialogue labeled with one of the four emotions mentioned above. Each dialogue is split into sentences, and speaker information is used to enrich the model's understanding.

Sentences: Tokenized versions of text (lists of integers).
Speakers: Additional features representing speakers.
Targets: Emotion labels.


Model Architecture:-
The model uses:

1. Embedding Layer: Converts word indices into dense vectors.
2. LSTM Layer: Processes word embeddings to learn sequential patterns.
3. Speaker Information: Speaker features are concatenated with LSTM outputs.
4. Dense Layer: Fully connected layers for final classification.
5. Dropout Layer: Regularizes the model by randomly dropping units during training.


Key Features:-

Stratified Splitting: Ensures that class distribution is preserved in training, validation, and test sets.
Class Weights: Corrects for class imbalances by adjusting weights based on class frequencies.
Confusion Matrix: Visualizes the model's performance across the four classes.
Precision, Recall, and F1-score: Metrics to evaluate the quality of predictions, especially for imbalanced classes.



To set up the project on your local machine, follow these steps:

1. git clone [https://github.com/ayushhimmatsinghka/A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK.git](https://github.com/ayushhimmatsinghka/A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK)
2. cd A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK


2. Install Dependencies
Ensure you have Python 3.7+ installed. Then install the required Python packages:
pip install -r Requirements.txt

1. After simply setting up the Requirements you can run the python file to get the results 
2. After training, you should see results similar to this:

![image](https://github.com/user-attachments/assets/000182a5-50e7-4e94-8664-412479b0c16e)
![image](https://github.com/user-attachments/assets/c39aa5bf-6fb4-4c67-9132-8d071db120f9)

PHASE-2:-

Improvements
Significant improvements were made to enhance model accuracy and robustness:

1. Bidirectional LSTM (BiLSTM): Replacing LSTM with BiLSTM for both sentence and dialog models resulted in a 63% accuracy for sentence classification and 72% accuracy for dialog classification, marking a slight improvement.
2. Multi-Head Attention: Introduced in the dialog model to focus on relevant parts of dialogues, contributing to improved contextual understanding.
3. Attention-Based Pooling: Implemented to refine the dialog model’s focus on key dialog sections, enhancing performance on longer contexts.


A PDF document, improvements_EE798R_improvements_pdf.pdf, is included, detailing these upgrades and also added the updated code with file name assignment_ee798r_ayush_210245_improvement.py

result obtained for dialog model-
![image](https://github.com/user-attachments/assets/b3cd91ac-de07-4ff0-8e29-0b40ace3e1e9)



