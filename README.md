# Лабораторная работа 3, команда Aboba
На основе ноутбука из предыдущего задания, свернуть нейросеть, используя минимум два уровня свертывания.

Слои:

```python
model.add(keras.layers.Conv2D(32, (3, 3), padding='same', activation='relu', input_shape=(32, 32, 3)))
model.add(keras.layers.Conv2D(64, (3, 3), padding='same', activation='relu', input_shape=(32, 32, 3)))
model.add(keras.layers.MaxPooling2D((2, 2)))
model.add(keras.layers.Conv2D(64, (3, 3), padding='same', activation='relu', input_shape=(32, 32, 3)))
model.add(keras.layers.Conv2D(128, (3, 3), padding='same', activation='relu', input_shape=(32, 32, 3)))
model.add(keras.layers.MaxPooling2D((2, 2)))
model.add(keras.layers.Conv2D(128, (3, 3), padding='same', activation='relu', input_shape=(32, 32, 3)))
model.add(keras.layers.MaxPooling2D((2, 2)))

model.add(keras.layers.Flatten())
model.add(keras.layers.Dense(128, activation='relu'))
model.add(keras.layers.Dense(10, activation='softmax'))
```

Параметры компиляции модели:

```python
model.compile(
              optimizer='Nadam',
              loss='mean_squared_error',
              metrics=['accuracy'])
```

Результаты обучения модели:

```
Test loss: 0.03461335226893425

Test accuracy: 0.7745000123977661
```

![image](https://user-images.githubusercontent.com/113666100/229601187-584b7ea4-a3b3-40a4-a0f7-2f3e961e1479.png)
![image](https://user-images.githubusercontent.com/113666100/229601339-3414661a-6d10-4c6f-abc4-6a7118c89dc4.png)

![image](https://user-images.githubusercontent.com/113666100/229601459-17a9b192-0076-45d6-95c1-3fe3b3de91e9.png)
![image](https://user-images.githubusercontent.com/113666100/229601538-15cf97a8-0713-41df-8d41-0179abf6f866.png)
