# Build the simplest model

```text
import numpy as np
import pandas as pd
```

## Keras is the simplest ML library, so I hope you enjoy it

```text
from keras.models import Sequential
from keras.layers import Dense

model = Sequential()

model.add(Dense(units=2, activation='relu', input_dim=2))
model.add(Dense(units=1))

model.compile(
    loss='mean_squared_error',
    optimizer='sgd',
    metrics=['accuracy']
)
```

1. first, we created a `sequential model`
2. then, we added two `dense layer(actually neural network)` for it. the first layer has one neural node, the second has one neural node, too.
3. sgd = Stochastic gradient descent

## After that, let us feed data into our model

```text
model.fit(x, y, epochs=100, batch_size=1)
```

## Then do a prediction

```text
model.predict(np.array([[170, 96]]))
```

