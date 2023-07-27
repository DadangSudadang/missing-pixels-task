# Missing Pixels Task
Repository for Missing Pixels task from AI class.

Training code (read-only, only for checking the output): [Google Colab](https://colab.research.google.com/drive/190PMGtKssth3qN9GOeYAsU3ZZjk2gTVy?usp=sharing).  
Testing code (runnable in Google Colab): [Google Colab](https://colab.research.google.com/drive/1xeWMM-3jQGHSL9NsRZutu6May4qJaW-W?usp=sharing).  

The Jupyter Notebook files for training and testing code are also available as missing_pixels_training.ipynb and missing_pixels_testing.ipynb in this repository.

Each training_size_* folder contains results of training with 200, 2,000 or 20,000 images. * represents the dataset size. The file format is as follows:
- model_cnn_missingpixel_*Data.h5 = The model checkpoint after training.
- history_*Data.npy = The training history for observing the loss over training epochs in numpy array format. Use:
  ```trn_history = np.load('history_*Data.npy',allow_pickle='TRUE').item()```
  In place of `history.history` to see the saved training history.
- history_*Data.png = The plot of model loss (MSE) from history_*Data.npy.
- Recreated Image *.png = The result of prediction using the respective model.
