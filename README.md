# Ai-Meeting-Summarizer

Universal AI Meeting Summarizer
A powerful, multilingual AI assistant that automatically transcribes, identifies speakers, and generates intelligent summaries for meetings from any audio source. This prototype is designed to be a platform-agnostic solution, working with audio from Google Meet, Zoom, Microsoft Teams, and more.

Developed in Coimbatore, India, this project showcases a complete, end-to-end AI workflow from raw audio to actionable business intelligence.

✨ Features
This application is a feature-rich platform designed to automate the entire post-meeting workflow.

Core Intelligence Engine
High-Accuracy Multilingual Transcription: Powered by OpenAI's large-v3 Whisper model for state-of-the-art accuracy.

Multi-Language Support: Full support for English, Tamil, Hindi, Malayalam, and Kannada.

Automatic Language Detection: Prevents inaccurate transcriptions by verifying that the audio language matches the user's selection.

Intelligent Speaker Recognition: Uses pyannote.audio for voiceprint analysis. It identifies pre-enrolled speakers and uses a similarity threshold to assign generic labels (Speaker 1, Speaker 2) to unknown voices, avoiding misidentification.

AI-Powered Summarization: Leverages the Google Gemini API to automatically generate:

A concise meeting summary.

A list of key decisions.

A checklist of all identified action items.

The main topics discussed.

Analytics & Integrations
Talk-Time Analytics: Generates an interactive pie chart showing the percentage of time each participant spoke.

Google Calendar Integration: A dashboard that securely connects to your Google Calendar to display a list of your upcoming meetings with video links.

User & System Management
Full Speaker Management: An intuitive UI to enroll new speaker voiceprints and view or delete existing ones.

Conversational Transcript: Displays the final transcript in a clean, script-like format for easy reading.

GPU Accelerated: The application is designed to leverage GPU hardware for a 10x+ speed improvement in processing.

🛠️ Technology Stack
AI Models: OpenAI Whisper large-v3, Pyannote.audio, Google Gemini Pro

Application Framework: Python & Streamlit

Data & Analytics: Pandas, Plotly

Authentication & APIs: Google OAuth 2.0, Google Calendar API

Development Environment: Google Colab with T4 GPU Acceleration

🚀 How to Run This Project
This project is designed to be run in a Google Colab environment. Follow these steps carefully to get started.

1. Prerequisites (One-Time Setup)
Before running the notebook, you must complete the following setup:

Google Drive: Create a main folder named AI_Summarizer_Project in your Google Drive. Inside it, create four empty subfolders: models, pip_cache, hf_cache, and voiceprints.

Google Cloud Project:

Create a project in the Google Cloud Console.

Enable the Google Calendar API.

Configure the OAuth Consent Screen (as an "External" app) and add your email as a test user.

Create OAuth 2.0 Credentials for a Desktop app.

Download the JSON file, rename it to credentials.json, and upload it to your AI_Summarizer_Project folder on Google Drive.

API Keys & Tokens: You need to get three secret keys:

Hugging Face Token: Create a read token from hf.co/settings/tokens. You must also accept the user conditions on the model pages for pyannote/speaker-diarization-3.1, pyannote/segmentation-3.0, and pyannote/embedding.

Google Gemini API Key: Get your key from aistudio.google.com/app/apikey.

Ngrok Authtoken: Get your token from your ngrok Dashboard.

2. Running the Notebook
Open in Colab: Open the AI_Summarizer_Project.ipynb notebook in Google Colab.

Set Up Secrets: In the Colab sidebar, click the key icon (🔑) and add your three secrets with these exact names:

HF_TOKEN

GEMINI_API_KEY

NGROK_AUTH_TOKEN

Enable GPU: Go to Runtime > Change runtime type and select T4 GPU as the hardware accelerator.

Run the Master Setup Cell: Execute the first large code cell. The first time you run this, it will take several minutes to download all the models and dependencies to your Google Drive cache. Subsequent runs will be much faster.

Run the Application Cell: Execute the second large code cell (the one starting with %%writefile app.py). This will create the application file.

Run the Launcher Cell: Execute the final code cell. This will start the application and print a public ngrok URL.

Click the URL to open your AI Meeting Summarizer in a new browser tab.

3. How to Use the Application
Enroll Speakers: Go to the "Enroll New Speaker" tab to upload a short voice sample for each person you want the app to recognize.

Manage Speakers: Go to the "Manage Speakers" tab to view or delete enrolled voiceprints.

Process a Meeting: Go to the "Process Meeting" tab, select the language spoken, upload your audio file, and click "Analyze Meeting."

View Calendar: Go to the "Calendar" tab and follow the on-screen instructions to authorize access to your Google Calendar and view your upcoming events.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

📧 Contact
Mohamed Rilvan Rinas Z
rilvanrinas@gmail.com

Email: [rilvanrinas@gmail.com]

Fiverr: [https://www.fiverr.com/mohamed_rinas_1/buying?source=avatar_menu_profile]
