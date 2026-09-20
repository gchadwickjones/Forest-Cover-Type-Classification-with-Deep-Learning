# Forest Cover Type Classification With Deep Learning
## Project Overview
This project develops a deep learning classification model to predict forest cover types using environmental features such as elevation, slope, soil type as well as geographic variables such as the distance to nearby features.

Several neural networks were initially trained with different architectures and hyperparameters to investigate their effect on classification performance. The performance of the initial models were evaluated using metrics such as accuracy, loss and confusion matrices. The best-performing models were then used as inspiration to create a final model, with the aim of building a model architecture that minimises loss and increases accuracy. 

During model development, 5 models with different architectures and hyperparemeters were trained to be evaluated. These are:
<img width="1190" height="440" alt="84152" src="https://github.com/user-attachments/assets/27c838a2-8c0b-42e7-8b49-12135188c640" />


## Methods 
* Exploratory data analysis and preprocessing
* Stratified train/validation/test split
* Feature standardisation using StandardScaler
* Neural networks built with TensorFlow/Keras
* Hyperparameter experimentation:
    * Hidden-layer size
    * Dropout
    * Learning rate
* Early stopping to reduce overfitting
* Evaluation using:
    * Accuracy
    * Precision, recall and F1-score
    * Confusion matrices
 
## Results
The initial experiments found that increasing the number of hidden units produced the strongest improvement in performance. A lower learning rate also produced better results than the baseline.

The results of the initial models are: 

<img width="990" height="440" alt="74454685" src="https://github.com/user-attachments/assets/6a26c05a-2d27-4582-8fe0-08748963aa5b" />


The final model used:

* 256 → 128 hidden units
* ReLU activation
* 0.0005 learning rate
* Adam optimiser
* Early stopping

The final model achieved 93.09% test accuracy, improving on the best initial model’s accuracy of 90.74%.
<img width="990" height="440" alt="7:8946513" src="https://github.com/user-attachments/assets/a0862951-4dd8-46f3-908a-c98f122f0cd4" />


The confusion matrix showed that the majority of predictions were correctly classified, although some confusion remained between similar forest cover types, particularly Classes 1 and 2.

<img width="1371" height="590" alt="77485132" src="https://github.com/user-attachments/assets/dfc2a317-a741-4f9e-82d0-4442b89680fa" />

## Limitations
The dataset contained a significant class imbalance, with **Classes 1 and 2** representing a large proportion of the observations. Stratified sampling was used to account for this, but the model may still be biased towards the majority classes given that practices such as `oversampling` were not employed to account for minority classes.

## Technologies
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras
* Jupyter Notebook
