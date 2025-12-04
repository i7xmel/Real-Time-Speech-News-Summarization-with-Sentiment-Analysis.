# News Summarization and Voice Analysis Project

A comprehensive toolkit for news article processing and real-time voice analysis with sentiment detection.

## Overview

This project combines two powerful capabilities:
1. **News Article Summarization** - Extract, summarize, and analyze news content
2. **Voice Denoising & Sentiment Analysis** - Process audio with noise reduction and emotional analysis

## Features

### News Summarization Module
- **Article Scraping**: Extract news articles from URLs with title, author, source, and content
- **Machine Learning Summarization**: Uses BART model (distilbart-cnn-12-6) for high-quality text summarization
- **Statistical Summarization**: Implements TF-IDF and word frequency based summarization techniques
- **Sentiment Analysis**: Identifies most positive and negative sentences in articles

### Voice Analysis Module
- **Audio Recording**: Records audio from the system microphone for specified durations
- **Noise Suppression**: Uses advanced noise reduction algorithms to clean audio signals
- **Audio Visualization**: Plots waveforms for both original and denoised audio
- **Speech Transcription**: Leverages OpenAI's Whisper model for accurate speech-to-text conversion
- **Sentiment Analysis**: Performs heuristic sentiment analysis on transcribed text
- **Audio Playback**: Allows playback of processed audio files

## Installation

### Prerequisites
- Python 3.7+
- Microphone access
- Audio output capabilities
- FFmpeg (for audio processing)

**Workflow:**
1. Records audio for 10 seconds from default microphone
2. Applies noise reduction to the recorded audio
3. Displays waveform plots comparing original and denoised audio
4. Converts cleaned audio to text using Whisper
5. Analyzes transcribed text for emotional sentiment
6. Provides audio playback capabilities

## Model Information

### News Processing
- **BART Summarization**: `sshleifer/distilbart-cnn-12-6` trained on CNN-DailyMail dataset
- **Sentiment Analysis**: `distilbert-base-uncased-finetuned-sst-2-english`
- Both models optimized for speed and deployment

### Voice Processing
- **Transcription Model**: Whisper Base
- **Noise Reduction**: Spectral gating technique
- **Sampling Rate**: 44.1 kHz
- **Audio Format**: WAV (16-bit PCM)


### News Summarization
- **Machine Learning Approach**: Higher quality summaries, suitable for production
- **Statistical Approach**: Faster processing, decent results without ML dependencies
- **Sentiment Analysis**: Useful for extracting most polarizing content

### Voice Processing
- Real-time audio recording and processing
- Effective noise suppression for clear transcription
- Basic keyword-based sentiment classification

## Customization

### News Summarization Models
The project supports multiple summarization models:
- Different Pegasus models
- T5 models
- Custom model integration

Modify hf_summarizer.py to experiment with different transformer architectures.

### Sentiment Classification
Voice analysis categorizes sentiment into:
- **Happy** - Contains positive emotion keywords
- **Sad** - Contains negative emotion keywords  
- **Neutral** - No strong emotional indicators

## Output Files (Voice Module)

- recorded_audio.wav - Original recorded audio
- denoised_audio.wav - Processed audio after noise suppression

## Screenshots

<img width="1202" height="700" alt="image" src="https://github.com/user-attachments/assets/62df5c93-a443-4d8b-bffe-f9087a8ecb58" />

## Summarization

<img width="1148" height="532" alt="image" src="https://github.com/user-attachments/assets/c874e519-3309-499e-8027-eff8df25bc26" />

<img width="1129" height="329" alt="image" src="https://github.com/user-attachments/assets/e3a6b3a1-36fa-41a0-8cca-de5e70d1403c" />
<img width="1154" height="455" alt="image" src="https://github.com/user-attachments/assets/c4a68e5e-db12-4f61-8a05-e9ffc680b6ce" />
<img width="1133" height="353" alt="image" src="https://github.com/user-attachments/assets/44a27f40-4994-423b-8eb9-de1bbc759fff" />


