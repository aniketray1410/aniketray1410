import numpy as np
import matplotlib.pyplot as plt

# Generate synthetic data
x = np.linspace(0, 10, 20)
y = 2 * x + np.random.normal(0, 2, 20)

# Fit a linear curve
coefficients = np.polyfit(x, y, 1)
poly = np.poly1d(coefficients)

# Plot the original data and fitted curve
plt.scatter(x, y, label='Data')
plt.plot(x, poly(x), color='red', label='Fitted Curve')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Linear Polynomial Curve Fitting')
plt.legend()
plt.grid(True)
plt.show()


