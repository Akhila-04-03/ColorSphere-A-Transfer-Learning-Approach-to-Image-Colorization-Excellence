# ColorSphere-A-Transfer-Learning-Approach-to-Image-Colorization-Excellence
Image colorization is the process of adding colors to grayscale images, transforming them into visually meaningful color representations. This technique is essential for restoring historical photos, enhancing medical imaging, and improving the visual quality of old or damaged pictures. This paper implement an image colorization approach using the ECCV16 and SIGGRAPH17 models, both of which leverage convolutional neural networks and transfer learning to produce high-quality results. By working in the LAB colorspace instead of RGB, these models achieve more realistic and vibrant colorizations, demonstrating the effectiveness of deep learning in image colorization.
## Image Colorization with ECCV16 and SIGGRAPH17 Models

This repository implements an image colorization approach using two deep learning models—*ECCV16* and *SIGGRAPH17*—which leverage convolutional neural networks and transfer learning. The models process grayscale images and apply color to generate visually meaningful and vibrant colorized images.

### Features
- *Colorization Models*: Utilizes the ECCV16 and SIGGRAPH17 models pre-trained on large datasets to generate high-quality, realistic colorizations.
- *LAB Colorspace*: Colorization is performed in the LAB colorspace, enabling more vivid and lifelike results.
- *Normalization*: Implements custom normalization for lightness (L) and color channels (A, B) to enhance colorization quality.

### Setup
1. Clone the repository and install required dependencies:
    bash
   
    git clone https://github.com/richzhang/colorization.git
    pip install -r colorization/requirements.txt
    
3. Add the cloned path to your system:
    python
   
    import sys
    sys.path.append('/path/to/colorization')
    

### Usage
1. *Load Models*:
   python
   
   import colorizers
   
   colorizer_eccv16 = colorizers.eccv16().eval()
   
   colorizer_siggraph17 = colorizers.siggraph17().eval()
   

3. *Colorize Images*:
   To colorize a grayscale image, use the following command:
   bash
   
   python demo_release.py -i /path/to/your/image.jpg
   
   Replace /path/to/your/image.jpg with the path to your input image.
### Evaluation
Evaluation component for assessing the quality of the colorized images against ground-truth color images using three metrics:
- *PSNR (Peak Signal-to-Noise Ratio)*: Measures image fidelity, with higher values indicating better quality.
- *MSE (Mean Squared Error)*: Evaluates the average difference in pixel values between the colorized and original images, where lower values represent better accuracy.
- *SSIM (Structural Similarity Index)*: Assesses the structural similarity between the colorized and original images, with values closer to 1 indicating higher similarity.
This metrics helps to ientify which model produced more realistic and visually appealing images.
### Implementation Details

LAB Colorspace: The models operate in the LAB colorspace, where:

L (Luminance) channel preserves the grayscale image’s details.
A and B (Color) channels are predicted by the models to add realistic colors.
Normalization:

The L channel (lightness) is centered and scaled to ensure consistent brightness across images.
The A and B channels (color) are scaled to control color intensity and enhance color vibrancy.

### Contact
For questions or feedback, feel free to reach out:

Email: raveendranakhila629@gmail.com

LinkedIn: [Akhila Raveendran](https://www.linkedin.com/in/akhila-raveendran-pm/)
