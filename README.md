# Fully Convolutional Neural Networks for Image Segmentation

This project demonstrates the use of Fully Convolutional Neural Networks (FCNs) for pixel-wise image segmentation. We train an FCN-8 model on a [custom dataset](https://drive.google.com/file/d/0B0d9ZiqAgFkiOHR1NTJhWVJMNEU/view?usp=sharing) prepared by [Divam Gupta](https://github.com/divamgupta/image-segmentation-keras). This dataset contains video frames captured from a moving vehicle and is a subset of the [CamVid dataset](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/), providing real-world segmentation examples.

## Model Architecture

- **Encoder**: A pretrained VGG-16 network is used for feature extraction, capturing complex patterns in the input images.
- **Decoder**: The FCN-8 architecture upsamples the encoded features to the original image size, predicting a segmentation mask for each pixel.
- **Output**: The model outputs a segmentation mask, classifying each pixel into one of 12 predefined categories.

![Architecture](imgs/fcn_8_architecture.png)

### Dataset

The dataset includes video frames of urban scenes, with each frame labeled for semantic segmentation into 12 classes, including road, buildings, cars, pedestrians, and more.

## Usage

### Running Locally or on Colab

1. **Local Setup**:
   - Clone the repository and navigate to the project directory.
   - Install the dependencies with `pip install -r requirements.txt`.
   - Open the `Fully Convolutional Neural Networks for Image Segmentation.ipynb` notebook in Jupyter and run the cells sequentially.

2. **Google Colab**:
   - [Open in Google Colab](https://colab.research.google.com/) and upload `Fully Convolutional Neural Networks for Image Segmentation.ipynb`.
   - Ensure GPU runtime is enabled under `Runtime > Change runtime type > GPU`.
   - Follow the notebook instructions to load the dataset, preprocess images, train the model, and visualize predictions.

## Results

The model is evaluated using metrics such as Intersection over Union (IoU) and Dice Score for each class. Visualization of the results includes ground truth and predicted segmentation masks side by side for qualitative analysis.

### Example Output

![Example Output](imgs/results.png)

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests if you find bugs or have improvements in mind.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.txt) file for details.

## Acknowledgements

- [Divam Gupta](https://github.com/divamgupta/image-segmentation-keras) for providing the dataset.
- The [CamVid dataset](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/) for the inspiration and foundational work in image segmentation.
- The Keras team for their contributions to making deep learning accessible.

## Contact

For questions or feedback, please contact [Ahmad Liaqat](mailto:ahmad786.writes@gmail.com).
