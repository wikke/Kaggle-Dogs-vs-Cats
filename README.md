# Dogs vs. Cats Redux: Kernels Edition

[Dogs vs. Cats Redux: Kernels Edition](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition)

- Keras with VGG16 pre-trained model, **Transfer Learning Practice**
- Add 2 layer on top, like below

```
output = GlobalAveragePooling2D()(output)
model_vgg16_pred = Dense(2, activation='softmax')(output)
```

- a `fit_generator`,`evaluate_generator`,`predict_generator` way to handle data. Keep eyes on `steps`,`steps_per_epoch`,`validation_steps`,`epochs`, etc.

- better loss & metrics to train model faster and better.
```
model_vgg16_model.compile(loss='binary_crossentropy', optimizer='nadam',  metrics=['binary_accuracy'])
```