
# Continuous Time Signal Convolution Code

This repository contains a Python code implementation for convolving continuous time signals, both in 1D and 2D. The code allows you to perform convolution between two signals without using prebuilt functions and provides the ability to plot the input signals as well as the result of the convolution using IPython Notebook or Jupyter.

## Prerequisites

Make sure you have the following installed:

- Python (version 3.0 or higher)
- NumPy library
- Matplotlib library
- Jupyter Notebook or JupyterLab

## Usage

1. Clone the repository to your local machine or download the code files.

```shell
git clone https://github.com/your_username/continuous-signal-convolution.git

2. Launch Jupyter Notebook or JupyterLab.

```shell
jupyter notebook  # For Jupyter Notebook
```
```shell
jupyter lab  # For JupyterLab
```

3. In the Jupyter interface, navigate to the repository's directory and open the desired Python notebook file:
   - For 1D signals, open `convolve_1D.ipynb`
   - For 2D signals, open `convolve_2D.ipynb`

4. Customize the input signals by modifying the code cells in the notebook. Replace the example signals with your desired data.

5. Run the notebook cells to perform the convolution and visualize the results. The input signals and the resulting convolution output will be plotted using `matplotlib` within the notebook.

## Examples

### Convolution of 1D Signals

Let's take a look at an example of using the continuous time signal convolution code in Jupyter Notebook to convolve two 1D signals.

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the 1D signals
signal1 = np.array([1, 2, 3, 4, 5])
signal2 = np.array([1, 0, -1])

# Perform the convolution
result = convolve1D(signal1, signal2)

# Plotting the signals
plt.figure(figsize=(8, 6))

# Plot the first input signal
plt.subplot(311)
plt.plot(signal1)
plt.title('Input Signal 1')
plt.xlabel('Index')
plt.ylabel('Value')
plt.grid(True)

# Plot the second input signal
plt.subplot(312)
plt.plot(signal2)
plt.title('Input Signal 2')
plt.xlabel('Index')
plt.ylabel('Value')
plt.grid(True)

# Plot the output signal
plt.subplot(313)
plt.plot(result)
plt.title('Convolution Result')
plt.xlabel('Index')
plt.ylabel('Value')
plt.grid(True)

plt.tight_layout()
plt.show()
```

In this example, we define two 1D signals (`signal1` and `signal2`) and perform the convolution using the `convolve1D` function. We then plot the input signals and the resulting convolution output using `matplotlib` within the Jupyter Notebook.

### Convolution of 2D Signals

Let's take a look at an example of using the continuous time signal convolution code in Jupyter Notebook to convolve two 2D signals.

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the 2D signals
signal1 = np.array([[1, 2, 3],
                    [4, 5, 6],
                    [7, 8, 9]])



signal2 = np.array([[1, 0, -1],
                    [0, 1, 0],
                    [-1, 0, 1]])

# Perform the convolution
result = convolve2D(signal1, signal2)

# Plotting the signals
plt.figure(figsize=(12, 4))

# Plot the first input signal
plt.subplot(131)
plt.imshow(signal1, cmap='gray')
plt.title('Input Signal 1')
plt.colorbar()

# Plot the second input signal
plt.subplot(132)
plt.imshow(signal2, cmap='gray')
plt.title('Input Signal 2')
plt.colorbar()

# Plot the output signal
plt.subplot(133)
plt.imshow(result, cmap='gray')
plt.title('Convolution Result')
plt.colorbar()

plt.tight_layout()
plt.show()
```

In this example, we define two 2D signals (`signal1` and `signal2`) and perform the convolution using the `convolve2D` function. We then plot the input signals and the resulting convolution output using `matplotlib` within the Jupyter Notebook.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---
