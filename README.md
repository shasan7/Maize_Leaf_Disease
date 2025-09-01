# Maize Leaf Disease Detection

## Dataset Link: https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset

## Kaggle Notebook: https://www.kaggle.com/code/shasan7/maize-leaf-disease/

The images were transformed and normalized using torch, then we fed them to the **pretrained RegNetY-120 model for fine-Tuning**

**The best validation accuracy achieved by our model is 95.47%**.

Training Summary:

    Epoch [1/20]  Train Loss: 0.3213 | Train Acc: 88.27%  || Val Loss: 0.1940 | Val Acc: 92.24%
    Saved new best model with val_acc: 92.24%
    Epoch [2/20]  Train Loss: 0.1618 | Train Acc: 94.75%  || Val Loss: 0.1750 | Val Acc: 94.39%
    Saved new best model with val_acc: 94.39%
    Epoch [3/20]  Train Loss: 0.1405 | Train Acc: 95.13%  || Val Loss: 0.1706 | Val Acc: 93.32%
    Epoch [4/20]  Train Loss: 0.0897 | Train Acc: 96.96%  || Val Loss: 0.1474 | Val Acc: 95.11%
    Saved new best model with val_acc: 95.11%
    Epoch [5/20]  Train Loss: 0.0809 | Train Acc: 96.99%  || Val Loss: 0.2306 | Val Acc: 93.44%
    Epoch [6/20]  Train Loss: 0.0888 | Train Acc: 96.78%  || Val Loss: 0.1790 | Val Acc: 95.11%
    Epoch [7/20]  Train Loss: 0.0904 | Train Acc: 96.81%  || Val Loss: 0.2067 | Val Acc: 94.87%
    Epoch [8/20]  Train Loss: 0.0695 | Train Acc: 97.73%  || Val Loss: 0.2116 | Val Acc: 94.51%
    Epoch [9/20]  Train Loss: 0.0584 | Train Acc: 97.97%  || Val Loss: 0.2141 | Val Acc: 93.68%
    Epoch [10/20]  Train Loss: 0.0516 | Train Acc: 98.21%  || Val Loss: 0.2610 | Val Acc: 92.12%
    Epoch [11/20]  Train Loss: 0.0620 | Train Acc: 97.94%  || Val Loss: 0.1991 | Val Acc: 95.47%
    Saved new best model with val_acc: 95.47%
    Epoch [12/20]  Train Loss: 0.0424 | Train Acc: 98.60%  || Val Loss: 0.2817 | Val Acc: 93.20%
    Epoch [13/20]  Train Loss: 0.0465 | Train Acc: 98.33%  || Val Loss: 0.2168 | Val Acc: 93.68%
    Epoch [14/20]  Train Loss: 0.0639 | Train Acc: 97.58%  || Val Loss: 0.2326 | Val Acc: 93.44%
    Epoch [15/20]  Train Loss: 0.0305 | Train Acc: 98.96%  || Val Loss: 0.2435 | Val Acc: 93.68%
    Epoch [16/20]  Train Loss: 0.0475 | Train Acc: 98.57%  || Val Loss: 0.2227 | Val Acc: 94.63%
    Epoch [17/20]  Train Loss: 0.0465 | Train Acc: 98.45%  || Val Loss: 0.1999 | Val Acc: 94.63%
    Epoch [18/20]  Train Loss: 0.0259 | Train Acc: 99.22%  || Val Loss: 0.3752 | Val Acc: 89.86%
    Epoch [19/20]  Train Loss: 0.0465 | Train Acc: 98.42%  || Val Loss: 0.2451 | Val Acc: 94.75%
    Epoch [20/20]  Train Loss: 0.0414 | Train Acc: 98.60%  || Val Loss: 0.3145 | Val Acc: 93.32%


Obtained Results:

    Classification Report:

                    precision    recall  f1-score   support
    
            Blight       0.90      0.95      0.92       229
       Common_Rust       0.98      0.97      0.98       261
    Gray_Leaf_Spot       0.91      0.83      0.87       115
           Healthy       1.00      1.00      1.00       233
    
          accuracy                           0.95       838
         macro avg       0.95      0.94      0.94       838
      weighted avg       0.96      0.95      0.95       838


    Confusion Matrix:

    [[217   3   9   0]
     [  7 254   0   0]
     [ 18   1  96   0]
     [  0   0   0 233]]


![Confusion Matrix: ](Conf_Mat.png)

![Accuracy Curve: ](Acc.png)

![Loss_Curve): ](Loss.png)
