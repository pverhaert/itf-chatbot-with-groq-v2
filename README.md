# ITF Chatbot with Groq API

This project is a Streamlit application that leverages the Groq API to provide an interactive chatbot experience for ITF-related information.

## Technologies

- [Git](https://git-scm.com/downloads)
- [Python 3.x](https://www.python.org/downloads/)
- [Streamlit](https://streamlit.io/)
- [Groq API](https://groq.com/)

## Prerequisites

- Python 3.11 or higher
- Git

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/pverhaert/itf-chatbot-with-groq-v2.git itf-chatbot`
   cd itf-chatbot
   ```
2. (Optional) Create and activate a virtual environment:  
`python -m venv .venv`  
`source .venv/bin/activate`  # On Unix or macOS  
`.venv\Scripts\activate.bat`  # On Windows
3. Install dependencies: `pip install -r requirements.txt`


## Configuration

### Groq API Key

Obtain a Groq API key from the [Groq API documentation](https://console.groq.com/docs/quickstart).

### Environment Setup

1. Rename `.env.example` to `.env`
2. Edit `.env`:
   - Replace `gsk_xxx` with your Groq API key
   - Set `PREFERRED_MODEL` to your desired model (see [supported models](https://console.groq.com/docs/models))

## Usage

Run the application: `streamlit run main.py`   
Alternatively, use the provided `run.bat` script on Windows.


## Editing Personalities

The chatbot personalities are defined in the `presets/personas.py` file. 
You can modify existing personalities or add new ones by editing this file.

### Adding a New Personality

1. Open `presets/personas.py`
2. Add a new dictionary to the `personas` list with the following structure:
````python
personas = {
   "General Chatbot": """
   I am a helpful AI assistant named Groq....
   """,
   "New Personality Name": """
   Description of the personality and its behavior""",
}
````

### Updating an Existing Personality

1. Locate the personality you want to update in the `personas` list
2. Modify the `key : value` fields as needed

### Deleting a Personality

1. Find the personality you want to remove in the `personas` list
2. Delete the entire `key : value` entry for that personality

Remember to save the file after making changes. 
The updated personalities will be available the next time you run the application.

## Deployment

This application is deployed on Streamlit Cloud:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://itf-chatbot.streamlit.app)
