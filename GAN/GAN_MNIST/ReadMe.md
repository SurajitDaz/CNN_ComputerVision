**Dataset:**<br>
The inbuilt dataset in TensorFlow, which returns train_images and train_labels as the first tuple. The second tuple contains the test set, which is not here. Link: [TensorFlow official documentation ](https://www.tensorflow.org/api_docs/python/tf/keras/datasets/mnist/load_data)

**Project Pipe Line:** <br>
DCGAN implementation can be divided into six steps. They are as follows (Ref. manual for implementation https://www.tensorflow.org/tutorials/generative/dcgan):<br>

* Importing Libraries with the specific versions
  - numpy - 1.19.2

  - tensorflow - 2.4.1

  - matplotlib - 3.3.2

  - skimage - 0.17.2

* Data Loading and Visualisation

* Data Preprocessing
  - **Step-1 Image normalization:** We normalize the image pixels in range (-1, 1) using the following formula. Dividing raw pixel values of range (0, 255) by 127.5 will make it in the range (0, 2) and when we subtract 1 from all the values, we get (-1, 1).
  - **Step-2 Resizing Image:** Here, we first normalised the data between [-1, 1] for faster training, then , resized images to [32, 32] and added another dimension as an image channel using an inbuilt function in skimage library (https://scikit-image.org/docs/dev/api/skimage.transform.html#resize). 
  - **Step-2 Batch/Suffle** We batch and shuffle the dataset. Refer to [this](https://www.tensorflow.org/api_docs/python/tf/data/Dataset#batch) for batch and [this](https://www.tensorflow.org/api_docs/python/tf/data/Dataset#shuffle) for the shuffle.

 
* Model Building

* Model Training

* Generating a GIF of Generated Images