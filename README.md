# Pelicia-Mikhail-Anthony-Bennet-D.R.--PA_2
### This is my submission for the second programming assignment

## The first section of this code is called "Normalization Problem"
#### The instruction was to create a random 5x5 array and normalize it using statistical standardization. To do this, I first imported the numpy library. I then created a random 5x5 array called "X" using np.random.random((5,5)). To normalize the array, I used the formula (X - X.mean()) / X.std() which subtracts the mean from each element and divides by the standard deviation. This creates a normalized array where the values are centered around 0 with a standard deviation of 1. Finally, I saved the normalized array to a file called "X_normalized.npy" using np.save().
#### Here's a section of the code that was used:
````
#This creates the random 5X5 array "X"
X = np.random.random((5,5))
#This normalizes the array
X_normalized = (X - X.mean()) / X.std()
#This saves the normalized array as "X_normalized.npy"
np.save('X_normalized.npy', X_normalized)
````
## The second section of this code is called "Divisible by 3 Problem"
#### The goal for this one was to create a 10x10 array of squared numbers from 1 to 100 and extract all elements divisible by 3. In order to do this, I first created an array of the first one hundred positive integers using np.arange(1,101). I then squared these numbers and reshaped them into a 10x10 grid using .reshape(10, 10) **2. To find elements divisible by 3, I used boolean indexing with the condition tenbyten % 3 == 0. Finally, I saved the resulting array to a file called "div_by_3.npy".
#### Here's a section of the code that was used:
````
#This creates an array of the first one hundred positive integers
hundred = np.arange(1,101)
#This squares the numbers and shapes the array into a 10X10 grid
tenbyten = hundred.reshape(10, 10) **2
#This determines all the elements that are divisible by 3
div_by_3 = tenbyten[tenbyten % 3 == 0]
#This saves the array as "div_by_3.npy"
np.save('div_by_3.npy', div_by_3)
````
