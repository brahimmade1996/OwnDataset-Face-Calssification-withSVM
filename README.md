# OwnDataset-Face-Calssification-withSVM
This is a fast implementation of a face classification system trained from scratch to your own dataset. The implementation is based on Facenet from keras, on MTCNN for face extraction and on an SVM for face identification/recognition/verification. The path to your own dataset has to be selected. The procedure is based mainly on using FaceNet and MTCNN to extract the faces from the training dataset. Then the images are fed into an SVM that is trained to recognize the extracted faces. The SVM model is saved with the aid of embeddings of .npz format. Finally the whole framework is tested using input from a Web camera or the camera of your laptop. The framework can be extended to any application you desire. Credits to **Machine Learning Mastery** for offering some useful insight and code to help this repository become reality.