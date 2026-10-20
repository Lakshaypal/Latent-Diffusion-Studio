# 🎨 Text-to-Image Generation App

A Flask-based web application that generates images from text descriptions using the Stable Diffusion model. This application provides a simple interface where users can input text prompts and receive AI-generated images in response.

## ✨ Features

- 🖼️ Text-to-image generation using Stable Diffusion v1.5
- 🎯 Simple and intuitive web interface
- ⚡ Local model inference (generation time depends on hardware)
- 🚀 Support for both CPU and GPU (CUDA) processing

## 📋 Prerequisites

- 🐍 Python 3.10 or 3.11 with compatible PyTorch dependencies
- 💻 CUDA-capable GPU (optional, but recommended for faster generation)
- 📦 pip (Python package installer)

## 🛠️ Installation

1. Clone this repository:
```bash
git clone https://github.com/Lakshaypal/Text-to-image-generations.git
cd Text-to-image-generations
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

3. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

1. Start the Flask application:
```bash
python app.py
```

2. Open your web browser and navigate to:
```
http://localhost:5001
```

3. Enter your text prompt in the input field and click the generate button to create an image.

## 🔧 Technical Details

- ⚙️ Built with Flask 3.1+
- 🤖 Uses Stable Diffusion v1.5 from Hugging Face
- 💪 Supports both CPU and GPU processing
- 🖼️ Images are generated synchronously and returned as base64-encoded PNG files

## 📦 Dependencies

- 🔥 torch
- 🎯 diffusers
- 🔄 transformers
- 🖼️ Pillow
- 🌐 Flask>=3.1,<4
- ⚙️ Werkzeug>=3.1,<4

## 📝 Notes

- ⏳ The first run will download the Stable Diffusion model, which may take some time depending on your internet connection.
- 🚀 GPU acceleration is automatically enabled if a CUDA-capable GPU is available.
- 🔌 The application runs on port 5001 by default.
- The configured model is `runwayml/stable-diffusion-v1-5`. First startup needs access to its files and enough memory; CPU generation can be slow.
- This is a development demo: `python app.py` enables Flask debug mode. For a local-only preview without the reloader, use `flask --app app run --host 127.0.0.1 --port 5001`. Do not expose the debug server publicly.
- Model access and use remain subject to the model provider's terms, separately from this repository's code licence.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- 🎨 Stable Diffusion model by RunwayML
- 🤗 Hugging Face for providing the model and tools
