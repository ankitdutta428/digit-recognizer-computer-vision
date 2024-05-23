# Digit Recognizer Computer Vision
 This is a computer vision project which I completed by using Deep Learning models on the MNIST dataset, and then identifying the digits.

 These are the following steps which I undertook to complete the project:

 1) Directly linking the kaggle dataset and google colab python notebook. The first few lines of the python notebook are to establish the connection between Kaggle dataset and Google Colab notebook.
 2) After taking the dataset performing the necessary pre-processing and make the model using tensorflow which has been given in the step 3.
 3) The code for building the model is:
```
  model = tf.keras.models.Sequential([
  tf.keras.layers.Conv2D(32,(3,3),activation = 'relu', input_shape=(28,28,1)),
  tf.keras.layers.Conv2D(32,(3,3),activation = 'relu'),
  tf.keras.layers.MaxPooling2D(2,2),
  tf.keras.layers.Conv2D(64,(3,3),activation = 'relu',padding = 'Same'),
  tf.keras.layers.Conv2D(64,(3,3),activation = 'relu',padding = 'Same'),
  tf.keras.layers.MaxPooling2D(pool_size = (2,2), strides = (2,2)),
  tf.keras.layers.Dropout(0.25),
  tf.keras.layers.Conv2D(64,(3,3),activation = 'relu',padding = 'Same'),
  tf.keras.layers.Conv2D(64,(3,3),activation = 'relu',padding = 'Same'),
  tf.keras.layers.MaxPooling2D(pool_size = (2,2), strides = (2,2)),
  tf.keras.layers.Dropout(0.25),
  tf.keras.layers.Flatten(),
  tf.keras.layers.Dense(256, activation='relu'),
  #tf.keras.layers.Dropout(0.50),
  tf.keras.layers.Dense(256, activation='relu'),
  tf.keras.layers.Dropout(0.50),
  tf.keras.layers.Dense(10, activation='softmax')
])
model.summary()
```
4) After building the model, use the suitable optimizer and then obtain the results. In this case, the Adam optimizer was used.
5) Using the connection established between kaggle and Colab, the .csv file was directly sent to the Kaggle competition.
6) The submission was judged and it achieved an accuracy of 99.325%.
7) The results obtained after using the code has been attached with this repository as submission_.csv

**Happy Coding**
