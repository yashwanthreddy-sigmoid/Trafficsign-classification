### Business Problem
We were given a dataset that has 43 different classes of traffic signals. So, our target is to determine the correct class the picture belongs to if a new sign is given to us.

### Problem Statement
Given a traffic sign image, we need to classify it into one of the groups of signs given in the dataset.

## Source of Data
Source: https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

## Real-world/Business objectives and constraints.
Very low-latency requirement. Errors can be very costly. 

## Used Approach to solve the problem

To solve this problem, we are using convolutional neural networks(CNN'S). Our neural network is inspired by LE-NET5.

The network used is called Le-Net that was presented YannLe Cun  http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf .

Our network is very similar to LE-NET5.Our network is:

The model consists of the following layers:
    
    • STEP 1: THE FIRST CONVOLUTIONAL LAYER #1
        ◦ Input = 32x32x1
        ◦ Output = 28x28x6
        ◦ Output = (Input-filter+1)/Stride* => (32-5+1)/1=28
        ◦ Used a 5x5 Filter with input depth of 3 and output depth of 6
        ◦ Apply a RELU Activation function to the output
        ◦ pooling for input, Input = 28x28x6 and Output = 14x14x6

    • STEP 2: THE SECOND CONVOLUTIONAL LAYER #2
        ◦ Input = 14x14x6
        ◦ Output = 10x10x16
        ◦ Layer 2: Convolutional layer with Output = 10x10x16
        ◦ Output = (Input-filter+1)/strides => 10 = 14-5+1/1
        ◦ Apply a RELU Activation function to the output
        ◦ Pooling with Input = 10x10x16 and Output = 5x5x16
        
        
    • STEP 3: FLATTENING THE NETWORK
        ◦ Flatten the network with Input = 5x5x16 and Output = 400
        
        
    • STEP 4: FULLY CONNECTED LAYER
        ◦ Layer 3: Fully Connected layer with Input = 400 and Output = 120
        ◦ Apply a RELU Activation function to the output
        
        
    • STEP 5: ANOTHER FULLY CONNECTED LAYER
        ◦ Layer 4: Fully Connected Layer with Input = 120 and Output = 84
        ◦ Apply a RELU Activation function to the output
        
        
    • STEP 6: FULLY CONNECTED LAYER
        ◦ Layer 5: Fully Connected layer with Input = 84 and Output = 43

## Conclusion

We are able to acheive 88 percent accuracy on testing data. And 100 percent accuracy on testing data.


## Built With
• ipython-notebook - Python Text Editor

• sklearn ,Keras- Machine learning library

• seaborn, matplotlib.pyplot, - Visualization libraries

• numpy- number python library

• pandas - data handling library


## Authors
• yashwanthreddysomala
