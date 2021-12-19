# dann_handwriting_recognition
Domain adversarial training of a neural network (DANN) to recognize handwritten digits after being trained to read digits from images. The advantage of using a DANN over a typical neural network is that it is possible to take an existing neural network and adapt it to a new but related problem set in order to save on training time and costs.

This notebook implements domain adversarial training of a neural network, a paradigm of deep learning that allows a neural network trained on one set of data to effectively make predictions on a different set of data (that has the same categories). The DANN used for this is defined in [Ganin et al., 2016](https://arxiv.org/pdf/1505.07818.pdf).

The code here first trains on the Street View House Numbers (SVHN) dataset and makes predictions on this data set. It then attempts to make predictions on handwritten digits from the MNIST data set. This is used as a baseline to compare the effects of using the DANN architecture. The network is then trained using DANN to align the source (SVHN) and target (MNIST) data set domains. Once this is completed, our network then tries to identify the handwritten digits from the MNIST data set. 

The goal is to demonstrate significant improvement from the network trained on just the SVHN data set. We define success as an increase in accuracity of at least 10%. 
