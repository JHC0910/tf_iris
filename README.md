# Iris Classifier by TensorFlow

## 採用資料集
**iris** from sklearn.data.load()

## 使用模型
Multilayer perceptron
* Input layer with 4 input dimension
* Hidden layers:
  * 100 neurons
  * 200 neurons
  * 200 neurons
* Output layer with 3 output dimension (3 answers)
~~~js
model.add(tf.keras.layers.Dense(input_dim = 4, units = 100, activation=tf.nn.relu))
model.add(tf.keras.layers.Dropout(0.2))
model.add(tf.keras.layers.Dense(units = 200, activation=tf.nn.relu))
model.add(tf.keras.layers.Dropout(0.2))
model.add(tf.keras.layers.Dense(units = 200, activation=tf.nn.relu))
model.add(tf.keras.layers.Dropout(0.2))
model.add(tf.keras.layers.Dense(units = 3, activation=tf.nn.softmax))
~~~

 
 
 
## 準確率
* Train accuracy 97.5%
* Test accuracy 96.7%
 
