# Frank or Not Frank

This project uses a deep learning model to identify if an image contains Frank the dog or not. The model is based on the VGG16 architecture and uses transfer learning for binary classification.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Training](#training)
- [Inference](#inference)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Prerequisites

- Python 3.7+
- PyTorch
- torchvision
- OpenCV
- Pillow

### Clone the Repository

```sh
git clone https://github.com/yourusername/frank_or_not.git
cd frank_or_not
```

### Install Dependencies

You can install the required dependencies using pip:

```sh
pip install torch torchvision opencv-python pillow
```

## Usage

### Inference

To run the model on your local machine using your webcam, make sure you have the model file `best_frank_or_not_model_run_1.pth` in the same directory as `frank_or_not.py`. Then execute:

```sh
python frank_or_not.py
```

This will open a window showing the webcam feed with the prediction overlaid on the video.

### Training

If you need to retrain the model, you can use the `train_and_evaluate.py` script. The training script is set up to handle multiple training runs and implements early stopping.

Ensure your dataset is organized as follows:

```
dataset/
    train/
        frank/
        not_frank/
    valid/
        frank/
        not_frank/
```

Then, execute:

```sh
python train_and_evaluate.py
```

This script will perform multiple training runs, save the best model based on validation accuracy, and store it as `best_frank_or_not_model_run_X.pth`.

## Inference

The `frank_or_not.py` script performs real-time inference using your webcam. Make sure the model file is in the same directory as the script and run:

```sh
python frank_or_not.py
```

### Example Output

The script will display a window with the webcam feed and overlay the prediction ("Frank" or "Not Frank") on each frame.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
