# Bengali Whisper Transcription

A tool for accurate Bengali speech transcription using OpenAI's Whisper model.

## Overview

This repository contains a Jupyter notebook (`tts_bn.ipynb`) for transcribing Bengali audio files using OpenAI's Whisper automatic speech recognition (ASR) model. The implementation leverages the large-v3 model for optimal accuracy with Bengali language content.

## Features

- High-accuracy Bengali speech recognition
- Support for various Whisper model sizes (tiny to large-v3)
- Automatic GPU detection and utilization when available
- Fallback to CPU processing when necessary
- Comprehensive error handling and diagnostics

## Prerequisites

- Python 3.6+
- PyTorch
- CUDA-compatible GPU (recommended for faster processing)
- FFmpeg

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/SakibAhmedShuva/bengali-whisper-transcription.git
   cd bengali-whisper-transcription
   ```

2. Install the required dependencies:
   ```bash
   pip install -U openai-whisper torch torchvision torchaudio
   ```

3. Install FFmpeg (if not already installed):
   - For Ubuntu/Debian:
     ```bash
     sudo apt update && sudo apt install ffmpeg
     ```
   - For macOS (using Homebrew):
     ```bash
     brew install ffmpeg
     ```
   - For Conda environments:
     ```bash
     conda install ffmpeg
     ```

## Usage

1. Upload your Bengali audio file to your working directory
2. Open `tts_bn.ipynb` in Jupyter Notebook or Google Colab
3. Modify the `audio_file_path` variable to point to your audio file:
   ```python
   audio_file_path = "path/to/your/bengali_audio.m4a"  # Change this to your file path
   ```
4. Run the notebook cells sequentially

## Model Selection

The notebook defaults to using the `large-v3` model for optimal transcription quality. If you're experiencing memory issues or need faster processing, you can change the model size:

```python
model_size = "large-v3"  # Options: "large-v3", "large-v2", "medium", "small", "base", "tiny"
```

Smaller models will consume less memory and run faster, but may offer reduced accuracy.

## Performance Notes

- **GPU Processing**: For optimal performance, a CUDA-compatible GPU with at least 10GB VRAM is recommended when using the large models.
- **CPU Processing**: While the notebook can run on CPU, transcription will be significantly slower, especially with larger models.
- **Audio Length**: Longer audio files will require more processing time and memory.

## Troubleshooting

- **GPU Memory Issues**: If you encounter GPU memory errors, try using a smaller model size.
- **Audio File Not Found**: Ensure the path to your audio file is correct and the file exists.
- **Audio Format Issues**: If transcription fails due to audio format issues, try converting your file to WAV format.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Sakib Ahmed Shuva - [GitHub Profile](https://github.com/SakibAhmedShuva)
