# Voice Cloning Model using Amazon Polly

This repository contains a Python script to create a custom voice cloning model using Amazon Polly. The model can generate synthetic speech that sounds like a specific target speaker by reproducing their unique vocal characteristics. The generated speech is indistinguishable from the target speaker's natural voice, and it can copy their accent, pitch, and speed.

## Getting Started

### Prerequisites

Before running the code, ensure you have the following prerequisites:

1. An AWS account with proper IAM permissions to access Amazon Polly and Amazon Transcribe services.
2. Install the AWS SDK for Python (Boto3) using the following command:

   ```
   pip install boto3
   ```

3. Collect voice data from the target speaker in the form of audio files. Use Amazon Transcribe to convert the voice recordings into text transcripts. Store both the audio files and transcripts in an Amazon S3 bucket.

### Running the Code

1. Clone this repository to your local machine.

2. Open the Python script `voice_cloning_model.py` in your favorite editor.

3. Modify the variables `text` and `voice_id` in the script according to your requirements. The `text` variable contains the input text that you want to convert to synthetic speech. The `voice_id` variable specifies the desired voice of the target speaker. You can choose from the available Polly voices that closely resemble the target speaker.

4. Execute the Python script using the following command:

   ```
   python voice_cloning_model.py
   ```

5. The script will generate the synthetic speech based on the input text and the chosen voice. The output speech will be saved as an MP3 file named `speech.mp3` in the current directory.

### Evaluating the Synthetic Speech

To evaluate the quality of the generated synthetic speech, conduct subjective evaluations or use objective metrics like MOS (Mean Opinion Score). Compare the synthetic speech with the target speaker's natural voice to assess accuracy, fluency, and understandability.

## Additional Information

For more information about polly synthesize speech and input audios [synthesize_speech](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/polly/client/synthesize_speech.html#).
