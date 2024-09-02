# ITF Chatbot with Groq API

[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://itf-chatbot.streamlit.app)

An interactive Streamlit-based chatbot application that leverages the Groq API to provide ITF-related information and
support multiple personalities.

## Features

- Interactive chat interface powered by Streamlit
- Integration with Groq API for natural language processing
- Customizable chatbot personalities
- Easy deployment on Streamlit Cloud

## Technologies

- [Python](https://www.python.org/) (3.10 or 3.11)
- [Git](https://git-scm.com/) (for version control)
- [Streamlit](https://streamlit.io/)
- [Groq API](https://groq.com/)

## Installation

1. Clone the repository:

````bash
git clone https://github.com/pverhaert/itf-chatbot-with-groq-v2.git itf-chatbot
cd itf-chatbot
````

2. Create and activate a virtual environment:

````bash
python -m venv .venv
source .venv/bin/activate  # On Unix or macOS
.venv\Scripts\activate.bat  # On Windows
````

3. Install dependencies: `pip install -r requirements.txt`
4. Rename `.env.example` to `.env`

Note: On Windows, you can use the `install.bat` script to automate steps 2-4.

## Configuration

1. Obtain a [Groq API key](https://console.groq.com/keys) from the Groq console.
2. Edit the `.env` file:
    - Replace `gsk_xxx` with your Groq API key
    - Set `PREFERRED_MODEL` to your desired model (see [supported models](https://console.groq.com/docs/models))

## Usage

1. Start the application: `streamlit run main.py`\
   On Windows, you can use the `run.bat` script.
2. Open your web browser and navigate to the provided local URL (usually `http://localhost:8501`).
3. Interact with the chatbot by selecting a personality and entering your queries.

## Customizing Personalities

Chatbot personalities are defined in `presets/personas.py`. To modify or add personalities:

1. Open `presets/personas.py`
2. Edit the `personas` dictionary:
   ````python
   personas = {
      "General Chatbot": "I am a helpful AI assistant named Groq...",
      "New Personality": "Description of the new personality...",
   }
   ````
3. Save the file and restart the application for changes to take effect.

## Deployment

This application is deployed on Streamlit Cloud. You can access it [here](https://itf-chatbot.streamlit.app).

To deploy your own version:

1. Fork this repository
2. Connect your GitHub account to Streamlit Cloud
3. Deploy the forked repository following Streamlit Cloud's instructions

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
