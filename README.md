# Iris Classifier by TensorFlow

## 採用資料集
**iris** from sklearn.data.load()

## 使用模型
Multilayer perceptron
* Input layer with 4 input dimension (4 features)
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

## Result
* 雖然模型本身很簡單，但是對於這類監督式學習的問題來說其參數空間已足夠涵蓋。
我們可以看到不論是測試或是訓練均得到優秀的結果。

* 對於訓練的結果，可做以下的調整:
  * Overfitting: 當訓練結果很好但測試結果卻很差時，可嘗試Dropout或將模型的參數空間減少。
  * Underfitting: 當訓練結果及測試結果都很差時，可先試著增加模型複雜度還有減少訓練的資料。
 
