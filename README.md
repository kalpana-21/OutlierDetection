# Out-of-distribution detection
Out-of-distribution (OOD) detection is a task in machine learning that involves identifying samples or data points that are essentially different from the training data distribution. In other words, OOD detection is the process of detecting inputs that are outside the range of the data that a model was trained on.
OOD detection is important because many machine learn- ing models are designed to work only within the range of data that they were trained on, and may give unreliable or incorrect predictions when presented with inputs that are significantly different from the training data. This is par- ticularly important in safety-critical applications where the consequences of incorrect predictions can be severe.
Out of Distribution detection using machine learning has become significantly popular in recent years, with various approaches available. This is currently being solved using SVMs by identifying the normal region.
Reconstruction methods have gained traction for anomaly detection since the availability of deep learning. The idea behind these methods is that a model that learns to compress and reconstruct normal data will be unable to do so with anomalous data because it has only been trained on normal data. Therefore, a high reconstruction error can indicate the presence of anomalous data.
The main concept is that if an autoencoder is trained effec- tively with ample data and can produce a precise replica of the input data, it should have a stable and minimal reproduc- tion error when given data that is comparable to the training data. However, if the autoencoder encounters input that is substantially different from what it was trained on, it will generate an unusual or extreme reproduction error, indicat- ing that it was unable to reproduce it accurately. Therefore, if an input has a high reproduction error, it is likely to be an anomaly if it should resemble the training data. This approach is especially beneficial when the data has a high dimensionality, making it challenging to establish what is normal behavior or identify what is too extreme to be con- sidered normal. For instance, a VAE that has been trained on MNIST images will struggle to reproduce a picture of a human face, and if presented with such an image, it will generate a relatively high reproduction error, indicating an anomaly.
VAE has been implemented so as to detect anomalies and used a loss function to train the VAE that balances recon- struction error and KL divergence. VAE labels samples that are out of distribution as 1 and those that belong to the distribution as 0.

