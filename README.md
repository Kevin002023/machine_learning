# Machine Learning Project 1 for the Higher Diploma in Computer Science and Data Analytics

## Speech-to-Text and Sentiment Analysis of 2024 Presidential Debates

This project leverages advanced speech-to-text models and natural language processing to analyze a segment of audio from the 2024 presidential debates. The workflow includes speaker diarization, transcription, and sentiment analysis to provide a comprehensive breakdown of the audio data.

## Project Overview

1. **Speaker Diarization Analysis**:
   - Identified the times when each speaker started and stopped talking within the audio segment.

2. **Speech-to-Text Analysis**:
   - Created a detailed transcript of the audio, segmented by speaker and time.

3. **Large Language Model (LLM) Analysis**
- Queries the transcript to extract insights such as:
  - Sentiment analysis.
  - Identification of speaker names.
  - Association of speakers with specific ideological perspectives.

4. **Testing AssemblyAI with a second audio file**
- Additional testing with more complex scenarios audio file(e.g., laughtrack, backing music, accents etc).

## Libraries Used
The project utilizes the following Python libraries:

- [**whisper**](https://github.com/openai/whisper): For speech-to-text transcription.
- [**os**](https://docs.python.org/3/library/os.html): For file and directory handling.
- [**csv**](https://docs.python.org/3/library/csv.html): To read and write CSV files.
- [**pandas**](https://pandas.pydata.org/): For data manipulation and analysis.
- [**matplotlib**](https://matplotlib.org/): For creating visualizations.
- [**pydub**](https://github.com/jiaaro/pydub): For audio file manipulation.
- [**openai**](https://pypi.org/project/openai/): For integrating with OpenAI's API.
- [**requests**](https://docs.python-requests.org/): For making HTTP requests to APIs.
- [**assemblyai**](https://www.assemblyai.com/): For advanced audio processing.
- [**pyannote.audio**](https://github.com/pyannote/pyannote-audio): For speaker diarisation.
- [**Authtoken**](https://example.com): For securely storing API tokens (custom module).
- [**collections**](https://docs.python.org/3/library/collections.html): For handling specialized container datatypes like `defaultdict`.
- [**numpy**](https://numpy.org/): For numerical operations and array handling.


## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Required Packages**:
   Install the dependencies listed above using `pip`:
   ```bash
   pip install whisper pandas matplotlib pydub openai requests assemblyai pyannote.audio numpy
   ```

3. **Installation of WhisperX**
   Using [Chocolatey](https://chocolatey.org/) for Windows or [Homebrew](https://brew.sh/) for linux/mac
   ```bash
   choco install ffmpeg
   ```

   ```bash
   brew install ffmpeg
   ```

3. **Set Up API Keys**:
   - Ensure you have valid API keys for **OpenAI** and **AssemblyAI**.
   - Set them as environment variables:
     ```bash
     export OPENAI_API_KEY="your_openai_api_key"
     export ASSEMBLYAI_API_KEY="your_assemblyai_api_key"
     ```

4. **Run the Analysis**:
   Execute the main script to perform the analysis:
   ```bash
   python main.py
   ```


## API Keys
Some components require API keys:
- **AssemblyAI API Key**: For advanced audio processing.
- **Pyannote Pipeline Token**: For speaker diarisation.

Add these keys in an `Authtoken.py` file or as environment variables to ensure secure usage.

---

## Project Structure
```
project-directory/
|-- project.ipynb   # Main analysis notebook
|-- data/
|   |-- raw/              # Directory for input audio files
|   |-- processed/        # Directory for processed data
|-- model.cache/          # Pipeline stored here to expediate running of notebook
|-- README.md             # Project documentation
```


---

## Acknowledgments
- [**OpenAI Whisper**](https://github.com/openai/whisper): For transcription.
- [**AssemblyAI**](https://www.assemblyai.com/): For audio analysis.
- [**Pyannote**](https://github.com/pyannote/pyannote-audio): For speaker diarisation.
- [**Matplotlib**](https://matplotlib.org/): For visualization.

---

## Author
[Kevin O'Leary]
