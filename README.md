# PyDinoAI

Training a CNN to play the [chrome://dino](chrome://dino/) game by itself.

![Demo](https://raw.githubusercontent.com/Aniruddha-Tapas/PyDinoAI/master/dino.gif)

## Steps to implement: 

* Open [chrome://dino](chrome://dino/) in your browser. Then run `create_training_data.py`. Adjust the region of interest [(380,150,970,290)](https://github.com/Applied-Programming/PyDinoAI/blob/master/create_training_data.py#L64) according to the position of the game in your computer screen. This will save the dino game pixel data from the ROI and the corresponding keys pressed for events as tuples in a file called `training_data.npy`.

* Next, run the `check-data.ipynb` by using `jupyter notebook` command. This will duplicate the data and balance it so that our neural networks doesn't overfit on one particular keypress.

* Once the data is created, run `train_model.py.` I used [AlexNet](https://github.com/BVLC/caffe/tree/master/models/bvlc_alexnet) CNN model to train our image data on. You can use other networks or your own custom one too. 

* When a model is saved after training, you can use put it to test. Open up the browser with the dino game and just run `test_model.py`. Not perfectly, but the dino will start dodging cactuses and flying dinos to increase the score.

* More the training data, more the training time, better would be our AI.

* Here I have run the program on my CPU for 10 epochs. Feel free to modify.

## Credits:

Thanks to [Sentdex](https://github.com/Sentdex) for the inspiration. This sort of project can be applied to myriad of use cases like self-driving car simulations and so on. Innovate accordingly.

<hr>
