
# Sierpiński Pyramid Visualization

## Project Overview

The **Sierpiński Pyramid Visualization** project provides a fascinating exploration of fractal geometry by visualizing the Sierpiński Pyramid, a three-dimensional fractal formed by recursively subdividing a tetrahedron. This project demonstrates how simple recursive processes can generate complex geometric structures, making it an excellent educational tool for understanding fractals and recursion in mathematics.

## Introduction to Sierpiński Pyramid

The Sierpiński Pyramid is a 3D fractal named after the Polish mathematician Wacław Sierpiński. It begins with a solid tetrahedron and divides it into smaller tetrahedrons at each level of recursion. The result is a beautiful and intricate shape that exhibits self-similarity at different scales.

### Key Concepts

- **Fractal Geometry**: Fractals are structures that exhibit self-similarity, meaning that they look similar at different scales. The Sierpiński Pyramid is a classic example of this concept.
- **Recursion**: This project relies on recursive functions to divide the tetrahedron into smaller pyramids, showcasing the power of recursive programming.

## Code Explanation

The project consists of a Python script that uses the **NumPy** and **Matplotlib** libraries to generate and visualize the Sierpiński Pyramid.

### Dependencies

```python
pip install numpy matplotlib
```

### Imports

```python
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d.art3d import Poly3DCollection
```

- **NumPy** is used for numerical operations and array manipulations.
- **Matplotlib** is a plotting library that facilitates 2D and 3D visualizations.
- **Poly3DCollection** from Matplotlib helps create 3D polygon collections.

### Main Functions

1. **sierpinski_pyramid(vertices, level)**: This function recursively generates the vertices of the Sierpiński Pyramid.

   - **Parameters**:
     - `vertices`: A NumPy array containing the four vertices of the tetrahedron.
     - `level`: An integer representing the depth of recursion.

   - **Returns**: A list of vertices representing the smaller pyramids generated at the specified recursion level.

   - **Logic**:
     - If the recursion level is `0`, it returns the current vertices.
     - Otherwise, it calculates midpoints of the edges and forms new vertices for the smaller pyramids.
     - The function calls itself recursively for each new pyramid until the desired level is reached.

```python
def sierpinski_pyramid(vertices, level):
    ...
```

2. **plot_pyramid(pyramids)**: This function visualizes the Sierpiński Pyramid using Matplotlib.

   - **Parameters**:
     - `pyramids`: A list of vertices representing the Sierpiński Pyramid.

   - **Logic**:
     - It creates a 3D plot and adds each pyramid to the collection.
     - Sets the axes labels and limits for better visualization.

```python
def plot_pyramid(pyramids):
    ...
```

### Main Execution

The `main()` function initializes the vertices of the base tetrahedron and calls the functions to generate and visualize the Sierpiński Pyramid.

```python
def main():
    vertices = np.array([
        [0, 0, 0],   # Vertex A
        [1, 0, 0],   # Vertex B
        [0.5, np.sqrt(3)/2, 0],  # Vertex C
        [0.5, np.sqrt(3)/6, np.sqrt(2/3)]  # Vertex D (top)
    ])
    
    level = 3  # Change this to create a more detailed pyramid
    pyramids = sierpinski_pyramid(vertices, level)
    plot_pyramid(pyramids)
```

### Execution Entry Point

The script's entry point checks if the script is being run directly and calls the `main()` function to execute the program.

```python
if __name__ == "__main__":
    main()
```

## Visualization

When executed, the program generates a 3D visualization of the Sierpiński Pyramid. Users can observe the fractal structure and appreciate how the complexity increases with the recursion level.

## Usage Instructions

1. **Clone the Repository**: Download the project to your local machine.
   ```bash
   git clone https://github.com/username/Sierpiski-Pyramid-Visualization.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd Sierpiski-Pyramid-Visualization
   ```
3. **Install Required Libraries**:
   Make sure you have Python installed, then install the necessary libraries:
   ```bash
   pip install numpy matplotlib
   ```
4. **Run the Visualization**:
   Execute the main script to generate the visualization:
   ```bash
   python Sierpinski_Pyramid_Visualization.py
   ```

## Conclusion

The Sierpiński Pyramid Visualization project serves as an excellent introduction to fractals and recursion in mathematics. By providing a visual representation of these concepts, the project aims to engage and educate users, making complex mathematical ideas more accessible.
