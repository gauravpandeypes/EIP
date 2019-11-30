```
val_acc: 0.8163
```

\# Define the model

model = Sequential()

model.add(SeparableConv2D(64, 3, padding="same", input_shape=(32, 32, 3))) #(32,32,3)x1  RF : 3

model.add(BatchNormalization())

model.add(Activation('relu'))



model.add(SeparableConv2D(128, 3)) #(30,30,3)x128  RF : 5

model.add(BatchNormalization())

model.add(Activation('relu'))



model.add(MaxPooling2D(pool_size=(2, 2))) #(15,15,3)x128  RF : 5

model.add(Dropout(0.1))



model.add(SeparableConv2D(64, 3)) #(13,13,3)x64  RF : 9 

model.add(BatchNormalization())

model.add(Activation('relu'))



model.add(SeparableConv2D(128, 3)) #(11,11,3)x128  RF : 13

model.add(BatchNormalization())

model.add(Activation('relu'))



model.add(MaxPooling2D(pool_size=(2, 2))) #(5,5,3)x128  RF : 15

model.add(Dropout(0.1))



model.add(SeparableConv2D(64, 3)) #(3,3,3)x64  RF : 23

model.add(BatchNormalization())

model.add(Activation('relu'))



model.add(SeparableConv2D(128, 3)) #(1,1,3)x128  RF : 31





model.add(Flatten())

model.add(Dense(num_classes, activation='softmax'))

\# Compile the model

model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])



```
Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
390/390 [==============================] - 31s 79ms/step - loss: 1.3735 - acc: 0.5013 - val_loss: 1.5521 - val_acc: 0.4956
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
390/390 [==============================] - 23s 60ms/step - loss: 1.0122 - acc: 0.6410 - val_loss: 1.0952 - val_acc: 0.6188
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
390/390 [==============================] - 23s 59ms/step - loss: 0.8954 - acc: 0.6825 - val_loss: 0.9391 - val_acc: 0.6724
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
390/390 [==============================] - 23s 60ms/step - loss: 0.8271 - acc: 0.7094 - val_loss: 1.0117 - val_acc: 0.6577
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
390/390 [==============================] - 23s 60ms/step - loss: 0.7824 - acc: 0.7238 - val_loss: 0.8811 - val_acc: 0.7050
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
390/390 [==============================] - 23s 59ms/step - loss: 0.7497 - acc: 0.7355 - val_loss: 0.9020 - val_acc: 0.6983
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
390/390 [==============================] - 23s 59ms/step - loss: 0.7240 - acc: 0.7453 - val_loss: 0.7652 - val_acc: 0.7400
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
390/390 [==============================] - 23s 59ms/step - loss: 0.7023 - acc: 0.7526 - val_loss: 0.7512 - val_acc: 0.7435
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
390/390 [==============================] - 23s 59ms/step - loss: 0.6859 - acc: 0.7594 - val_loss: 0.7597 - val_acc: 0.7432
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
390/390 [==============================] - 23s 59ms/step - loss: 0.6723 - acc: 0.7637 - val_loss: 0.6708 - val_acc: 0.7743
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
390/390 [==============================] - 23s 59ms/step - loss: 0.6563 - acc: 0.7684 - val_loss: 0.7402 - val_acc: 0.7510
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
390/390 [==============================] - 23s 59ms/step - loss: 0.6428 - acc: 0.7755 - val_loss: 0.7098 - val_acc: 0.7599
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
390/390 [==============================] - 23s 59ms/step - loss: 0.6362 - acc: 0.7774 - val_loss: 0.6925 - val_acc: 0.7699
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
390/390 [==============================] - 23s 59ms/step - loss: 0.6255 - acc: 0.7822 - val_loss: 0.6658 - val_acc: 0.7769
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
390/390 [==============================] - 23s 60ms/step - loss: 0.6212 - acc: 0.7830 - val_loss: 0.7069 - val_acc: 0.7622
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
390/390 [==============================] - 23s 59ms/step - loss: 0.6124 - acc: 0.7846 - val_loss: 0.6674 - val_acc: 0.7773
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
390/390 [==============================] - 23s 59ms/step - loss: 0.6012 - acc: 0.7883 - val_loss: 0.6617 - val_acc: 0.7780
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
390/390 [==============================] - 23s 59ms/step - loss: 0.5993 - acc: 0.7883 - val_loss: 0.6786 - val_acc: 0.7713
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
390/390 [==============================] - 23s 59ms/step - loss: 0.5907 - acc: 0.7935 - val_loss: 0.6324 - val_acc: 0.7883
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
390/390 [==============================] - 23s 59ms/step - loss: 0.5884 - acc: 0.7933 - val_loss: 0.6440 - val_acc: 0.7798
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0004065041.
390/390 [==============================] - 23s 59ms/step - loss: 0.5828 - acc: 0.7970 - val_loss: 0.6526 - val_acc: 0.7809
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.000389661.
390/390 [==============================] - 23s 58ms/step - loss: 0.5821 - acc: 0.7940 - val_loss: 0.6245 - val_acc: 0.7881
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0003741581.
390/390 [==============================] - 23s 58ms/step - loss: 0.5724 - acc: 0.7984 - val_loss: 0.6655 - val_acc: 0.7768
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0003598417.
390/390 [==============================] - 23s 58ms/step - loss: 0.5781 - acc: 0.7949 - val_loss: 0.6167 - val_acc: 0.7953
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.0003465804.
390/390 [==============================] - 23s 58ms/step - loss: 0.5644 - acc: 0.8023 - val_loss: 0.6274 - val_acc: 0.7919
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0003342618.
390/390 [==============================] - 23s 58ms/step - loss: 0.5616 - acc: 0.8041 - val_loss: 0.6251 - val_acc: 0.7909
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.0003227889.
390/390 [==============================] - 23s 58ms/step - loss: 0.5628 - acc: 0.8015 - val_loss: 0.6102 - val_acc: 0.7930
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.0003120774.
390/390 [==============================] - 23s 59ms/step - loss: 0.5519 - acc: 0.8052 - val_loss: 0.5955 - val_acc: 0.8022
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.000302054.
390/390 [==============================] - 23s 59ms/step - loss: 0.5541 - acc: 0.8047 - val_loss: 0.6339 - val_acc: 0.7917
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.0002926544.
390/390 [==============================] - 23s 58ms/step - loss: 0.5468 - acc: 0.8070 - val_loss: 0.6110 - val_acc: 0.7969
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.0002838221.
390/390 [==============================] - 23s 58ms/step - loss: 0.5495 - acc: 0.8066 - val_loss: 0.6214 - val_acc: 0.7933
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 0.0002755074.
390/390 [==============================] - 23s 59ms/step - loss: 0.5471 - acc: 0.8085 - val_loss: 0.6235 - val_acc: 0.7930
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 0.000267666.
390/390 [==============================] - 23s 58ms/step - loss: 0.5441 - acc: 0.8092 - val_loss: 0.6162 - val_acc: 0.7963
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 0.0002602585.
390/390 [==============================] - 22s 58ms/step - loss: 0.5360 - acc: 0.8117 - val_loss: 0.6148 - val_acc: 0.7960
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 0.00025325.
390/390 [==============================] - 23s 58ms/step - loss: 0.5344 - acc: 0.8140 - val_loss: 0.6270 - val_acc: 0.7918
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 0.0002466091.
390/390 [==============================] - 22s 58ms/step - loss: 0.5362 - acc: 0.8114 - val_loss: 0.6174 - val_acc: 0.7956
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 0.0002403076.
390/390 [==============================] - 23s 58ms/step - loss: 0.5351 - acc: 0.8118 - val_loss: 0.6227 - val_acc: 0.7945
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 0.0002343201.
390/390 [==============================] - 23s 58ms/step - loss: 0.5325 - acc: 0.8133 - val_loss: 0.6013 - val_acc: 0.8029
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 0.0002286237.
390/390 [==============================] - 23s 58ms/step - loss: 0.5356 - acc: 0.8128 - val_loss: 0.5965 - val_acc: 0.8041
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 0.0002231977.
390/390 [==============================] - 23s 58ms/step - loss: 0.5299 - acc: 0.8127 - val_loss: 0.6153 - val_acc: 0.7965
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 0.0002180233.
390/390 [==============================] - 23s 58ms/step - loss: 0.5265 - acc: 0.8162 - val_loss: 0.6126 - val_acc: 0.7993
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 0.0002130833.
390/390 [==============================] - 23s 58ms/step - loss: 0.5269 - acc: 0.8135 - val_loss: 0.6149 - val_acc: 0.7996
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 0.0002083623.
390/390 [==============================] - 23s 59ms/step - loss: 0.5233 - acc: 0.8159 - val_loss: 0.6079 - val_acc: 0.7966
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 0.0002038459.
390/390 [==============================] - 23s 58ms/step - loss: 0.5178 - acc: 0.8174 - val_loss: 0.6172 - val_acc: 0.7962
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 0.0001995211.
390/390 [==============================] - 23s 58ms/step - loss: 0.5185 - acc: 0.8181 - val_loss: 0.5936 - val_acc: 0.8038
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 0.0001953761.
390/390 [==============================] - 23s 58ms/step - loss: 0.5193 - acc: 0.8183 - val_loss: 0.6085 - val_acc: 0.8010
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 0.0001913998.
390/390 [==============================] - 22s 58ms/step - loss: 0.5209 - acc: 0.8175 - val_loss: 0.6054 - val_acc: 0.7994
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 0.0001875821.
390/390 [==============================] - 23s 58ms/step - loss: 0.5176 - acc: 0.8196 - val_loss: 0.6067 - val_acc: 0.7992
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 0.0001839137.
390/390 [==============================] - 23s 58ms/step - loss: 0.5147 - acc: 0.8197 - val_loss: 0.5955 - val_acc: 0.8029
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 0.000180386.
390/390 [==============================] - 22s 58ms/step - loss: 0.5094 - acc: 0.8215 - val_loss: 0.5958 - val_acc: 0.8045
Model took 1151.52 seconds to train
```

**Group Members**

=> Gaurav Pandey - Wednesday, Online

=> Utkarsh Pandey - Saturday, Online

=> Aditya Shukla - Saturday, Online
