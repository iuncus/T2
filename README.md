# Transcription and Translation

## Overview
This script processes a video file to generate a subtitle file (.srt) using Whisper for transcription and NLLB for translation. 

1. Transcode a .wav file with ffmpeg.
2. Transcribe the audio using Whisper.
3. Generate an SRT file containing the transcription.
4. Translate the transcription into a target language using NLLB.
5. Save the translated transcription in a separate SRT file.

## Requirements

### Dependencies
Ensure the following Python packages are installed:

```sh
pip install torch transformers ffmpeg-python
```


### Hardware Requirements
- The script will run on CPU if a CUDA-compatible GPU is unavailable, but performance may be slower.

## Usage
1. Place your audio file in the script's directory and update the `file_name` variable with the correct filename (without the extension).
2. Run all cells


## Configuration
Modify these variables to suit your needs:
```python
src_lang = "auto"  # Source language detection
language = "es"  # Language for forced transcription decoding
tgt_lang = "eng_Latn"  # Target translation language
```

## Notes
- Output files are stored in the `SrtFiles` directory.
- Adjust `batch_size` based on available VRAM.


