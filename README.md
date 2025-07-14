# Image Transformation with PIL and NumPy

This Jupyter Notebook (`image-transform.ipynb`) demonstrates fundamental image manipulation techniques using Python's Pillow (PIL) library and NumPy for pixel-level operations. It covers importing images, viewing them as numerical arrays, performing basic arithmetic operations (addition and subtraction) on image arrays, and utilizing PIL's built-in blending functionality.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Image Loading & Display:** Load and display images using the Pillow library.
- **NumPy Integration:** Convert images to NumPy arrays to perform mathematical operations on pixel data.
- **Image Addition:** Demonstrate element-wise addition of two images, with proper handling for pixel value overflow.
- **Image Subtraction:** Showcase element-wise subtraction of two images, with proper handling for negative pixel values.
- **Image Blending:** Utilize `PIL.Image.blend` for simple alpha blending of two images.
- **Error Handling Insights:** Includes a section highlighting common pitfalls (e.g., data type conversion, value clipping) and their corrections.

## Prerequisites

Before running this notebook, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Pillow (PIL)
- NumPy
- Matplotlib (for displaying images within the notebook, though `img.show()` is also used)

## Installation

1.  **Clone the repository (or download the notebook):**
    ```bash
    git clone https://github.com/ZeroWraith/Image-transformation
    cd your-repo-name
    ```

2.  **Install the required Python packages:**
    ```bash
    pip install jupyter pillow numpy matplotlib
    ```

## Usage

1.  **Place your images:** Ensure `house.png` and `heart.png` (or any other `.png` images you wish to use, updated in the notebook) are in the same directory as the `image-transform.ipynb` file.
    * `house.png` (used as `img1`)
    * `heart.png` (used as `img2`)
    * *(Note: The notebook expects images of the same dimensions for direct array operations. The corrected code includes resizing.)*

2.  **Start Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

3.  **Open the notebook:** In your web browser, navigate to the Jupyter Notebook interface and open `image-transform.ipynb`.

4.  **Run the cells:** Execute the cells sequentially to see the image loading, array transformations, and resulting images.

## Examples

The notebook demonstrates the following transformations:

### Original Images

| Image 1 (`house.png`) | Image 2 (`heart.png`) |
|-----------------------|-----------------------|
| ![House Image](house.png) | ![Heart Image](heart.png) |

### Image Addition (Corrected Method)

This section shows how to correctly add two images by converting them to NumPy arrays, performing element-wise addition, and clipping values to the valid 0-255 range to prevent overflow.

![Result of Image Addition](Screenshot%202025-07-14%20162900.png)

### Image Blending (PIL `Image.blend`)

An alternative method for combining images using PIL's `Image.blend` function, which allows for alpha-controlled mixing.

![Result of Image Blending](Screenshot%202025-07-14%20163545.png)

### Matrix Subtraction Operation

Demonstrates element-wise subtraction of image arrays, again with clipping to ensure valid pixel values.

![Result of Image Subtraction](Screenshot%202025-07-14%20164624.png)

## Contributing

Feel free to fork this repository, make improvements, and submit pull requests. Suggestions for new image manipulation techniques or clearer explanations are always welcome!

## License

This project is open-source and available under the [MIT License](LICENSE).
