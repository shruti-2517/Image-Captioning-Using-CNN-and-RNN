# Image Captioning using CNNs and RNNs (VGG16 + LSTM)

This project demonstrates **Image Captioning**, i.e., generating textual descriptions for images using **Deep Learning**.
It combines **Convolutional Neural Networks (CNNs)** for extracting image features and **Recurrent Neural Networks (RNNs)** for generating captions in natural language.

The model uses **VGG16** (pre-trained on ImageNet) as an **encoder** and **LSTM** as a **decoder** to predict captions word by word.


##  Workflow

1. **Data Preprocessing**

   * Captions are cleaned, lowercased, tokenized, and stripped of punctuation.
   * A vocabulary of unique words is created.
   * Each image is mapped to one or more processed captions.

2. **Feature Extraction**

   * Each image is passed through **VGG16**.
   * The output from the penultimate layer (`fc2`) is saved as image features.

3. **Sequence Preparation**

   * Each caption is split into sequences for training the model to predict the next word.
   * Captions are padded to ensure equal sequence length.

4. **Model Training**

   * The model is trained using **categorical cross-entropy loss**.
   * At each step, the model learns to predict the next word in the caption given the current words and image features.

5. **Caption Generation**

   * During inference, the model starts with the `<start>` token.
   * It predicts one word at a time until the `<end>` token is reached.
   * The final generated caption is displayed for the given image.


## Technologies Used

| Component           | Description                                  |
| ------------------- | -------------------------------------------- |
| **Language**        | Python                                       |
| **Framework**       | TensorFlow / Keras                           |
| **CNN Model**       | VGG16 (Pre-trained on ImageNet)              |
| **RNN Model**       | LSTM                                         |
| **Text Processing** | Keras Tokenizer                              |
| **Visualization**   | Matplotlib                                   |
| **Dataset Used**    | Flickr8k                                     |





