# Sign-Language-DL

## SyncSign
- Project Introduction
SyncSign is a dynamic real-time sign language interpretation application. It is a fascinating and complex project that aims to accurately identify and interpret signs or symbols using Computer Vision and Long Short-Term Memory (LSTM) models of deep learning. LSTM models are a specialized type of recurrent neural network (RNN) that excel in processing sequential data by capturing long-term dependencies and patterns, making them well-suited for tasks such as computer vision and real-time detection.

- Project Scope
Project Definition: SyncSign includes real-time sign language interpretation within a dynamic environment. By employing computer vision and LSTM models, it can accurately identify different signs in varying environments like changing lighting and sign orientations.

- Objectives:
Ensure real-time processing capabilities for practicality.
Help hearing impaired in interpretation and communication.
Understand the working of LSTM deep learning models.

- Data Collection: In the data collection phase, we utilized OpenCV to capture real-time video feed for sign recognition. Each sign was annotated and recorded in sequences of 30 frames, with each sequence having a length of 30 frames. The annotated signs included "hello," "thanks," and "iloveyou". Data for each sign was stored separately in.npy files within individual folders, ensuring organized and easily accessible datasets for training and testing purposes. This helped in data collection to provide a space for LSTM model implementation for real-time sign detection and classification.

- Model Type and Architecture: Through employing TensorFlow's Keras API, SyncSign is able to perform real-time detection and classification of signs in dynamic environments. The model architecture comprises multiple LSTM (Long Short-Term Memory) layers for sequential processing, followed by dense layers for classification.

An input layer with LSTM units configured for 64 neurons, set to return sequences and utilizing the RELU activation function. This layer accepts input sequences of 30 frames, each containing 1662 features.
A subsequent LSTM layer with 128 neurons, also configured to return sequences and utilizing RELU activation.
A final LSTM layer with 64 neurons, configured to return only the final output sequence, employing RELU activation.
Dense layers for further processing, including a 64-neuron layer followed by a 32-neuron layer, both utilizing RELU activation.
An output layer employing the softmax activation function, with the number of neurons corresponding to the total number of sign classifications.
Additionally, the model is compiled using the Adam optimizer and categorical cross-entropy loss function, with categorical accuracy as the evaluation metric.

- Training and Optimization: To continuously improve the model's performance and efficiency, a separate Python script can be executed to train and optimize the model whenever new data becomes available. Through TensorFlow's Keras API, the model is trained for 1000 epochs on the training dataset. To ensure the model's generalizability and its performance, testing and training data has a 95:5 partition. The data is prepared for training by loading sequences of frames corresponding to each sign action. These sequences were then converted into numpy arrays, annotated with their respective categorical labels, thus creating the input-output pairs for model training. This approach to training ensures the model's proficiency in real-time sign detection and classification. Additionally, it ensures adaptability to evolving datasets, therefore better results and optimization.

- Results: The model's performance is evaluated based on categorical accuracy, which measures the proportion of correctly classified signs. The model's performance is continuously monitored and improved through training and optimization. The results demonstrate the model's proficiency in real-time sign detection and classification, making it a valuable tool for the hearing impaired community.



