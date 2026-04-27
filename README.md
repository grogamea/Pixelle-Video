# Pixelle-Video

A fork of [AIDC-AI/Ovis](https://github.com/AIDC-AI/Pixelle-Video) focused on video understanding and generation with multimodal large language models.

## Overview

Pixelle-Video extends the original Pixelle architecture to support video inputs, enabling temporal reasoning, video captioning, video question answering, and more.

## Features

- 🎥 **Video Understanding**: Process and reason over video sequences
- 🖼️ **Image Support**: Full backward compatibility with image inputs
- 🤖 **Multimodal LLM**: Powered by state-of-the-art vision-language models
- ⚡ **Efficient Inference**: Optimized for both single-GPU and multi-GPU setups
- 🐳 **Docker Ready**: Pre-configured Docker and DevContainer support

## Quick Start

### Prerequisites

- Python 3.10+
- CUDA 11.8+ (for GPU support)
- 24GB+ VRAM recommended

### Installation

```bash
# Clone the repository
git clone https://github.com/your-org/Pixelle-Video.git
cd Pixelle-Video

# Install dependencies
pip install -e .
```

### Using Docker

```bash
# Build the Docker image
docker build -t pixelle-video .

# Run the container
docker run --gpus all -it pixelle-video
```

### Using Dev Container

Open the project in VS Code and select **Reopen in Container** when prompted.

## Usage

### Video Question Answering

```python
from pixelle_video import PixelleVideoModel

model = PixelleVideoModel.from_pretrained("pixelle-video-7b")

response = model.chat(
    video="path/to/video.mp4",
    question="What is happening in this video?"
)
print(response)
```

### Video Captioning

```python
from pixelle_video import PixelleVideoModel

model = PixelleVideoModel.from_pretrained("pixelle-video-7b")

caption = model.caption(video="path/to/video.mp4")
print(caption)
```

## Model Zoo

| Model | Parameters | Video Frames | Download |
|-------|-----------|--------------|----------|
| Pixelle-Video-7B | 7B | Up to 64 | Coming Soon |
| Pixelle-Video-14B | 14B | Up to 64 | Coming Soon |

## Benchmarks

| Benchmark | Pixelle-Video-7B | Pixelle-Video-14B |
|-----------|-----------------|------------------|
| MVBench | TBD | TBD |
| VideoMME | TBD | TBD |
| EgoSchema | TBD | TBD |

## Documentation

Full documentation is available at [https://your-org.github.io/Pixelle-Video](https://your-org.github.io/Pixelle-Video).

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the Apache 2.0 License — see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [AIDC-AI](https://github.com/AIDC-AI) for the original Pixelle codebase
- The open-source community for invaluable tools and models

## Citation

```bibtex
@misc{pixelle-video,
  title={Pixelle-Video: Multimodal Large Language Model for Video Understanding},
  author={Your Team},
  year={2024},
  url={https://github.com/your-org/Pixelle-Video}
}
```
