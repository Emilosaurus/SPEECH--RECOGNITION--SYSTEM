# SPEECH  RECOGNITION  SYSTEM

# Whisper MP3 Transcription

This project uses OpenAI's Whisper ASR model to transcribe MP3 audio files into readable text paragraphs with proper punctuation.

## 👨‍💻 Intern Details

**Company:** CODTECH IT SOLUTIONS  
**Name:** Emil Saj Abraham  
**Intern ID:** CT08DL252  
**Domain:** AI  
**Duration:** 8 weeks  
**Mentor:** Neela Santhosh

## 🔧 Requirements

Install the following Python packages in your environment:

```bash
pip install --upgrade transformers torch torchaudio accelerate
pip install deepmultilingualpunctuation
```

> 💡 Recommended: Use a virtual environment like `conda` or `venv`.

## 🧠 Model

This uses the `"openai/whisper-medium"` model. You can switch to `"openai/whisper-large"` for better accuracy.

## 📂 Usage

```python
from transformers import pipeline

# Load the Whisper model
asr = pipeline("automatic-speech-recognition", model="openai/whisper-medium")

# Provide path to your MP3 file
file_path = "Sample Audio.mp3"

# Transcribe the audio
result = asr(file_path, return_timestamps=True)

# Print nicely formatted paragraph
print("\n📝 Transcription:\n")
print(result["text"])
```

## 🔊 Sample Audio Playback

<audio controls>
  <source src="Sample Audio.mp3" type="audio/mpeg">
</audio>

## ✅ Output

The script outputs a punctuated paragraph of transcribed audio.

---

### Optional Enhancements

- Use `deepmultilingualpunctuation` for improved punctuation restoration.
- Add CLI or GUI for ease of use.

## 📄 License

MIT License. Free to use and modify.
