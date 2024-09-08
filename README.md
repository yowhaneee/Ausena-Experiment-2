## PA 2.1 NORMALIZATION PROBLEM:
Normalization is one of the most basic preprocessing techniques in data analytics. This involves centering and scaling process. Centering means subtracting the data from the mean and scaling means dividing with its standard deviation. Mathematically, normalization can be expressed as:
𝑍 = 𝑋 − 𝑥̅ / 𝜎

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and .std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as X_normalized.npy

    # Start 
    import numpy as np
    
    # Create a random 5x5 ndarray
    X = np.random.random((5, 5))
    
    # Normalize X (subtract the mean and divide by the standard deviation)
    X_normalized = (X - X.mean()) / X.std()
    
    # Save the normalized ndarray as X_normalized.npy
    np.save('X_normalized.npy', X_normalized)
    
    # Testing if the npy file will work by loading
    np.load('X_normalized.npy')
    
    # End

## PA 2.2 DIVISIBLE BY 3 PROBLEM:
Create the following 10 x 10 ndarray. which are the squares of the first 100 positive integers.

From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy
    
    # Start
    import numpy as np
    
    # Get the squares of first 100 positive integers
    s = np.arange(1,101) ** 2
    
    # Make the array into a 10 x 10 matrix
    A = s.reshape(10,10)
    
    # Determine all the elements that are divisible by 3
    div_by_3 = A[A % 3 == 0]
    
    # Save the Result as div_by_3.npy
    np.save('div_by_3.npy', div_by_3)
    
    # Testing if the npy file will work by loading
    np.load('div_by_3.npy')
    
    # End
