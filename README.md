# A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK

Project Overview:-
This project implements a Long Short-Term Memory (LSTM) network for recognizing emotions from text dialogues. The model also incorporates speaker information, allowing it to learn patterns related to who is speaking, in addition to the textual content. The ultimate goal is to predict the emotion associated with a sequence of text while utilizing speaker features to improve classification accuracy.

The four emotion classes used in this task are:

Angry
Happy
Neutral
Sad


Dataset:-
The dataset contains dialogues, with each dialogue labeled with one of the four emotions mentioned above. Each dialogue is split into sentences, and speaker information is used to enrich the model's understanding.

Sentences: Tokenized versions of text (lists of integers).
Speakers: Additional features representing speakers.
Targets: Emotion labels.




Model Architecture:-
The model uses:

Embedding Layer: Converts word indices into dense vectors.
LSTM Layer: Processes word embeddings to learn sequential patterns.
Speaker Information: Speaker features are concatenated with LSTM outputs.
Dense Layer: Fully connected layers for final classification.
Dropout Layer: Regularizes the model by randomly dropping units during training.


Key Features:-

Stratified Splitting: Ensures that class distribution is preserved in training, validation, and test sets.
Class Weights: Corrects for class imbalances by adjusting weights based on class frequencies.
Confusion Matrix: Visualizes the model's performance across the four classes.
Precision, Recall, and F1-score: Metrics to evaluate the quality of predictions, especially for imbalanced classes.



To set up the project on your local machine, follow these steps:

git clone [https://github.com/your-username/your-repo-name.git](https://github.com/ayushhimmatsinghka/A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK)
cd A-SELF-ATTENTIVE-EMOTION-RECOGNITION-NETWORK


2. Install Dependencies
Ensure you have Python 3.7+ installed. Then install the required Python packages:
pip install -r requirements.txt

after simply setting up the Requirements you can run the python file to get the results 
Results
After training, you should see results similar to this:

![image](https://github.com/user-attachments/assets/000182a5-50e7-4e94-8664-412479b0c16e)
![image](https://github.com/user-attachments/assets/c39aa5bf-6fb4-4c67-9132-8d071db120f9)


