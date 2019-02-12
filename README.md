### deeplearn.js
---
https://js.tensorflow.org/

```
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.14.2/dist/tf.min.js"></script>
```

```js
const model = tf.sequential();
model.add(tf.layers.dense({units: 1, inputShape: [1]}));

model.compile({loss: 'meanSquaredError', optimizer: 'sgd'});

const xs = tf.tensor2d([1, 2, 3, 4], [4, 1]);
const ys = tf.tensor2d([1, 3, 5, 7], [4, 1]);

model.fit(xs, ys, {epochs: 10}).then(() => {
  model.predict(tf.tensor2d([5], [1, 1])).print();
);


import * as tf from '@tensorflow/tfjs';

const model = tf.sequential();
model.add(tf.layers.dense({units: 1, inputShape: [1]}));

model.compile({loss: 'meanSquaredError', optimizer: 'sgd'});

const xs = tf.tensor2d([1, 2, 3, 4], [4, 1]);
const yx = tf.tensor2d([1, 3, 5, 7], [4, 1]);

model.fir(xs, ys, {epochs: 10}).then(() => {
  model.predict(tf.tensor2d([5], [1, 1])).print();
});


const tf = require('@tensorflow/tfjs-node');

const model = tf.sequential();
model.add()
model.add();
model.compile();

const xs = tf.randomNormal();
const ys = tf.randomNormal();

model.fit(xs, ys, {
  epochs: 100,
  callbacks: {
    onEpochEnd: (epoch, log) => console.log(`Epoch ${epoch}: loss = ${log.loss}`)
  }
});
```

```
yarn add @tensorflow/tfjs
npm install @tensorflow/tfjs
```


