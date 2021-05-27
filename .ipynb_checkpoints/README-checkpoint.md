# LSTM Stock Predictor
---
The following code attempts to use deep learning recurrent neural networks to model bitcoin closing prices.  

One model will use the Fear and Greed indicators to predict the closing price while the second model will use a window of closing prices to predict the closing price.

## Parameters
---
Both models utilise the parameters below:  
* Window size of 10 days as higher window size appeared to produce lower loss in the model.  
* Setup with 10 units per layer (same as the window size) and 20% dropout
* 30 epochs and batch size 30 as higher number of epochs did not produce much improved loss

## Evaluation
---
**Which model has a lower loss?**  
The second model (closing prices) produced a lower loss of only 0.0056 while the first model (fear and greed) had a loss of 0.0489.  

**Which model tracks the actual values better over time?**  
The closing prices model tracked the values better over time.  
![](/Resources/closing.png)  
And for comparison the fng model.  
![](/Resources/fng.png)  
**Which window size works best for the model?**  
I found that higher window size works better for both models and produced the lower loss within the model.