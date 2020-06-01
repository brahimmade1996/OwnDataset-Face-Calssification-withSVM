# OwnDataset-Face-Calssification-withSVM
This is a fast implementation of a face classification system trained from scratch on your own dataset. The implementation is based on Facenet from keras, on MTCNN for face extraction and on an SVM for face identification/recognition/verification. The path to your own dataset has to be selected. The procedure is based mainly on using FaceNet and MTCNN to extract the faces from the training dataset. Then the images are fed into an SVM that is trained to recognize the extracted faces. The SVM model is saved with the aid of embeddings of '.npz' format. Finally the whole framework is tested using input from a Web camera or the camera of your laptop. The framework can be extended to any application you desire. The evaluation of the framework is easy to implement and light to carry out. Memory constraint was taken into consideration during the development of this framework. 

# Face Extraction with FaceNet and MTCNN
For face extraction we deploy Facenet and MTCNN, in order to extract the faces for any input image. It is used as a preprocessing step,before training our SVM with the faces, to further perform classification.

# Training SVM with detected extracted faces
So we use the face detectors to extract only the faces from the images of our training dataset. Then we train our SVM for these images and we try to achieve a high Classification accuracy. After the SVM model is saved in the form of embeddings, so we can easily reload the model to any new SVM using the Sklearn libary.This helps a lot when testing/evaluating on a device where memory is an issue, or when fast deployment is required.

# Test using MTCNN or Viola-Jones algorithm
After training the SVM and saving the embeddings, you can easily reload the small-size embeddings in a new SVM of the sklearn libary. Hence evaluation can be then performed. For evaluation we give the chance to the user to either use MTCNN or Haar Cascade detector which is more commonly known as the Viola-Jones Algorithm. So for extracting the faces, as the preprocessing step before evaluating them on our trained SVM, you can choose the face detection model, by choosing which script to run. MTCNN yields higher accuracy in general, during face detection, however Viola-Jones detector is simpler and lighter to use. Hence it's up to the user which one he/she prefers to use.


Credits to **Machine Learning Mastery** for offering some useful insight and code to help this repository become reality.
