
**Functios for calculation output shape**<br>
```python
def getConv2DOutputShape(imageSideLength, kernel, padding,stride):
    return  (imageSideLength+2*padding-kernel)/stride + 1
    
def getMaxPoolOutputShape(imageSideLength, kernel,stride): #no padding for maxpool
    return  (imageSideLength-kernel)/stride + 1
```


<br><br>**Parmeters number for Conv2D**<br>
by default image_channel is 3, (RGB channels) <br>
```
total parameter for one Conv2D layer =  filters_num * (kernel_size * kernel_size * image_channel  + 1)  
```
Since each filter need 1 bias parameter, we add 1 in the formula



<br><br>**Keras epochs, batch, iterations, and steps_per_epoch** <br>
say you have 512 train data, **batch size** is 32<br>
you need 512/32 = 16 **iterations** to finish fit all the train data fro the first time.
And at that time you finished 1st **epoch**. If you do another 16 iterations with the batch_size 32, and go through the whole data in the second time, you will finish the 2nd **epoch**.<br>
Typically, **steps_per_epoch** = data_size // batch_size (it is the same as the **iterations** you need to go through for one epoch). You can give it other values if you need to.


<br><br>**Good gitbook for keras**<br>
https://ustczen.gitbooks.io/keras/content/optimizers.html
