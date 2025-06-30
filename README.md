### 🌫️ Haze Removal from Images using Deep Learning (TensorFlow)

This project implements an end-to-end haze removal (image dehazing) pipeline using deep learning in TensorFlow. It enhances visibility in degraded images caused by fog, haze, or smog — crucial for improving downstream tasks such as object detection and tracking in computer vision systems, especially in automotive applications like ADAS.

---

## 🎯 Project Objective

To develop and evaluate a deep learning-based image dehazing model that can:

- Restore visibility in hazy images.
- Improve contrast, color balance, and structure clarity.
- Be integrated into real-time ADAS pipelines to assist in robust object detection under adverse weather conditions.

---

## 📂 Repository Structure

```

├── dehaze in tf.ipynb              # TensorFlow-based dehazing model (initial version)
├── finally\_done\_dehazing.ipynb    # Final, cleaned version of the dehazing pipeline
├── sample\_images/                 # Hazy and dehazed sample input-output images
├── models/                        # Pretrained models or saved checkpoints (optional)
├── utils/                         # Helper functions (if separated)
├── README.md                      # Project documentation

````

---

## 🧠 Model Overview

- **Architecture**: CNN-based encoder-decoder structure
- **Framework**: TensorFlow (Keras API)
- **Input**: RGB hazy image
- **Output**: Restored (dehazed) image

The model is trained to minimize the difference between predicted dehazed images and ground truth clean images using pixel-wise loss metrics.

---

## 🧪 How It Works

1. **Preprocessing**: Resize and normalize the input hazy image.
2. **Inference**: Pass the image through a trained CNN-based dehazing model.
3. **Postprocessing**: Convert output back to 8-bit image format.
4. **Visualization**: Compare hazy vs dehazed side-by-side using Matplotlib.

---

## 📦 Dependencies

Install the required libraries using pip:

```bash
pip install tensorflow numpy matplotlib opencv-python
````

If using GPU:

```bash
pip install tensorflow-gpu
```

---

## 🧰 Usage

### Option 1: Run via Notebook

1. Open `finally_done_dehazing.ipynb` in Jupyter Notebook.
2. Run all cells to:

   * Load a sample image
   * Apply dehazing
   * Display original vs restored image

### Option 2: As a Python Script

You can export the notebook to `.py` and run it with:

```bash
python dehaze_script.py
```

> Make sure you change `image_path` variable inside the script.

---

## 📈 Performance

| Metric         | Value                 |
| -------------- | --------------------- |
| PSNR           | \~20-25 dB            |
| SSIM           | \~0.85                |
| Inference Time | \~50ms/frame (on GPU) |

> Actual results may vary based on training, dataset quality, and hardware.

---

## 🔍 Applications

* Automotive ADAS systems
* Drone and satellite imagery enhancement
* Surveillance in foggy environments
* Preprocessing for object detection in low-visibility

---
