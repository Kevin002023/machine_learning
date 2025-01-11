# Machine Learning Project 1 for the Higher Diploma in Computer Science and Data Analytics

## Speech-to-Text and Sentiment Analysis of 2024 Presidential Debates

This project leverages advanced speech-to-text models and natural language processing to analyze a segment of audio from the 2024 presidential debates. The workflow includes speaker diarization, transcription, and sentiment analysis to provide a comprehensive breakdown of the audio data.

## Project Overview

1. **Speaker Diarization Analysis**:
   - Identified the times when each speaker started and stopped talking within the audio segment.

2. **Speech-to-Text Analysis**:
   - Created a detailed transcript of the audio, segmented by speaker and time.

3. **Sentiment and Insights Extraction**:
   - Fed the transcript into a large language model (LLM) to perform sentiment analysis and extract key insights from the discussion.

## Packages and Libraries Used

The following Python packages were used in the project:

- **[whisper](https://github.com/openai/whisper)**: For speech-to-text transcription.
- **[os](https://docs.python.org/3/library/os.html)**: To manage file paths and environment variables.
- **[csv](https://docs.python.org/3/library/csv.html)**: For handling CSV files.
- **[pandas](https://pandas.pydata.org/)**: For data manipulation and analysis.
- **[matplotlib.pyplot](https://matplotlib.org/stable/tutorials/introductory/pyplot.html)**: For creating visualizations of the data.
- **[pydub](https://pydub.com/)**: For processing and manipulating audio files.
- **[openai](https://platform.openai.com/docs/)**: To query the LLM for sentiment and insight extraction.
- **[requests](https://docs.python-requests.org/en/latest/)**: For making HTTP requests.
- **[assemblyai](https://www.assemblyai.com/)**: For speaker diarization and speech-to-text analysis.
- **[pyannote.audio](https://github.com/pyannote/pyannote-audio/blob/develop/README.md**)

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Required Packages**:
   Install the dependencies listed above using `pip`:
   ```bash
   pip install whisper pandas matplotlib pydub openai requests assemblyai
   ```

3. **Installation of WhisperX**
   Using [Chocolatey](https://chocolatey.org/) for Windows or [Homebrew](https://brew.sh/)
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

## Workflow Details

### 1. Speaker Diarization
- Used **AssemblyAI** to identify when each speaker started and stopped talking.
- Results were saved as a CSV file, containing speaker labels and timestamps.

### 2. Speech-to-Text Transcription
- Leveraged **Whisper** and **AssemblyAI** models to convert speech into text.
- Combined the diarization output to produce a transcript segmented by speaker.

### 3. Sentiment and Insights Analysis
- Fed the segmented transcript into the **OpenAI API** to:
  - Perform sentiment analysis for each speaker’s statements.
  - Extract key topics and insights discussed during the debate.

### 4. Visualization
- Created visualizations with **Matplotlib** to represent speaker activity and sentiment trends over time.

## Outputs

1. **Speaker Diarization File**:
   - CSV file containing speaker labels and timestamps.
2. **Transcript File**:
   - Text file with the transcript segmented by speaker.
3. **Sentiment Report**:
   - Detailed sentiment analysis report for each speaker.
4. **Visualizations**:
   - Graphs and charts representing speaker activity and sentiment trends.

## Future Enhancements
- Integrate additional natural language processing models to detect bias or rhetorical strategies.
- Expand the analysis to include real-time processing for live debates.
- Enhance visualizations with interactive dashboards.

## License
This project is licensed under the MIT License. See the LICENSE file for details.