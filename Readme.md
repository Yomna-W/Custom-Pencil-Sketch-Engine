# Custom Pencil Sketch Generator in Python

A lightweight Python project that transforms standard RGB images into artistic pencil sketches using **OpenCV** and **NumPy**—built completely from scratch without relying on high-level wrapper functions.

Unlike pre-built library shortcuts, this project demonstrates the underlying mechanics of image processing, including manual color space conversion, custom 2D Gaussian kernel generation, spatial convolution, and pixel-wise blend operations to achieve a classic pencil sketch effect.

## ✨ Features

* **Manual Grayscale Conversion:** Computes luminance explicitly using standard human-perception weights ($Y = 0.299R + 0.587G + 0.114B$).

* **Custom Convolution Engine:** Implements spatial filtering from scratch, featuring a custom 2D Gaussian kernel builder and nested loop convolution with reflection boundary padding.

* **Color-Dodge Blending:** Inverts and divides pixel layers mathematically to mimic traditional hand-drawn pencil line art.

* **Pure Python & NumPy Logic:** Relies on fundamental matrix operations for educational and illustrative computer vision workflows.

## 🛠️ Requirements

Make sure you have Python installed along with the required dependencies:

```
pip install opencv-python numpy


```

## 🚀 Getting Started

1. Clone or download this repository to your local machine:

   ```
   git clone https://github.com/your-username/pencil-sketch-generator.git
   cd pencil-sketch-generator
   
   
   ```

2. Place your target image in your project directory (or update the file path inside your script).

3. Run your script:

   ```
   python sketch.py
   
   
   ```

## 🔍 How It Works

1. **Grayscale Layer:** Converts the input RGB image into a single-channel grayscale representation using weighted luminance.

2. **Inversion:** Inverts the grayscale values ($255 - \text{pixel}$) to prepare for the blend step.

3. **Gaussian Smoothing:** Generates a Gaussian kernel and convolves it across the inverted image to soften details and create a broad background blur.

4. **Pencil Sketch Blend:** Blends the grayscale layer with the inverted blurred layer using a mathematical color-dodge algorithm (`grey / (255 - blur)`), isolating high-contrast edges resembling pencil strokes.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check out the issues page for your repository.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).