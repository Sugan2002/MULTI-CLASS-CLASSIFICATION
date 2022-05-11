### EX NO: 03
### DATE: 08.04.2022
# <p align="center"> MULTI-CLASS CLASSIFICATION</P>

## Aim:
To write a python program to implement the multi class classification algorithm .
</br>
</br>

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab

</br>
</br>

## Related Theoritical Concept:

Multiclass Classification:

In multi-class classification, the neural network has the same number of output nodes as the number of classes. Each output node belongs to some class and outputs a score for that class. Class is a category for example Predicting animal class from an animal image is an example of multi-class classification, where each animal can belong to only one category.

The number of classifier models depends on the classification technique we are applying to. •One vs. All:- N-class instances then N binary classifier models •One vs. One:- N-class instances then N* (N-1)/2 binary classifier models •The Confusion matrix is easy to derive but complex to understand.

</br>
</br>

## Algorithm

1. Define dataset with centers=3 
2. Summarize dataset shape 
3. Summarize observations by class label 
4. Summarize first few examples 
5. Plot the dataset and color the by class label


</br>
</br>
</br>

## Program:
```python
/*
Program to implement the multi class classifier.
Developed by  :  P.SUGANYA
RegisterNumber:  212220230049
*/

from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X, y = make_blobs(n_samples=1000, centers=3, random_state=1)
print(X.shape, y.shape)
counter = Counter(y)
print(counter)
for i in range(10):
    print(X[i], y[i])
for label, _ in counter.items():
    row_ix = where(y == label)[0]
    pyplot.scatter(X[row_ix, 0], X[row_ix, 1], label=str(label))
pyplot.legend()
pyplot.show()

```

</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

## Output:
![output](./static/img/expO3NN.PNG)


## Result:
Thus, the python program to implement the multi class classification was implemented successfully.
