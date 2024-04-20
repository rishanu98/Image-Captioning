# Text-Summarizer
## Objective
* To recognize the context of an ikage and describe them 

### Image-Captioning-generator-on-Flckr-8K-dataset
Image caption generator is a process of recognizing the context of an image and annotating it with relevant captions using deep learning, and computer vision. It includes the labeling of an image with English keywords with the help of datasets provided during model training. Imagenet dataset is used to train the CNN model called Xception. Vit transforemr is responsible for image feature extraction. These extracted features will be fed to the gpt2 decoder model which in turn generates the image caption.

### Encoder
* The Vision Transformer, or ViT, is a model for image classification that employs a Transformer-like architecture over patches of the image. An image is split into fixed-size patches, each of them are then linearly embedded, position embeddings are added, and the resulting sequence of vectors is fed to a standard Transformer encoder. In order to perform classification, the standard approach of adding an extra learnable “classification token” to the sequence is used *

### Decoder 
* GPT-2 is a transformers model pretrained on a very large corpus of English data in a self-supervised fashion. inputs are sequences of continuous text of a certain length and the targets are the same sequence, shifted one token (word or piece of word) to the right. The model uses internally a mask-mechanism to make sure the predictions for the token i only uses the inputs from 1 to i but not the future tokens. This way, the model learns an inner representation of the English language that can then be used to extract features useful for downstream tasks. The model is best at what it was pretrained for however, which is generating texts from a prompt. *
![]

### Data Collection from Dataset
* The Flickr-8K dataset contains 8,000 images, each with five textual descriptions, making a total of 40,000 descriptions. The first step in the project is to 
   preprocess the data, including resizing the images, extracting features using a pre-trained CNN, and encoding the textual descriptions into a numerical format.
* For the image caption generator. Flickr 8k dataset is used. There are also other datasets like Flickr30k and MSCOC dataset.
* link https://www.kaggle.com/datasets/adityajn105/flickr8k

### Inference
* The output of the model is softmax function that generates probability distribution across all the words.
* Greedy Search Algorithm was used to select the words with maximum probability.
* ROUGE Score was used as evaluation metrics.

