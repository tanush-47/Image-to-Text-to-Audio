# Image to Text to Audio

This Python script allows you to convert text from an image to an audio file. The script uses the `pytesseract` library to extract text from the image and the `gtts` library to convert the extracted text to speech.

## Requirements

- Python 3.x
- `pytesseract` library
- `Pillow` library
- `gtts` library
- Tesseract-OCR

You also need to install Tesseract-OCR. Instructions for different operating systems are as follows:

Use the package manager to install Tesseract.

```bash
sudo apt-get install tesseract-ocr
```

## Usage

1. **Clone the Repository**

2. **Prepare an Image**

   Place the image file you want to process in the same directory as the script.

3. **Set the path**

   Modify the script to include the path to your image file. Example:

4. **Execute the Script**

   ```bash
   python image_to_audio.py
   ```

5. **Listen to the Audio**

   The extracted text will be saved as an audio file named `output_audio.mp3`.

## Script Explanation

### Text Extraction

The script uses the `pytesseract` library to extract text from an image:

```python
result = pytesseract.image_to_string(img)
```

### Text to Speech Conversion

The script uses the `gtts` library to convert the extracted text to speech and save it as an MP3 file:

```python
tts = gtts.gTTS(result)
tts.save("output_audio.mp3")
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
