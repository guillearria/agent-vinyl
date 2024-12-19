# Agent Vinyl: A Vertical AI Agent for DJs and Vinyl Enthusiasts

## Overview
**Agent Vinyl** is an intelligent assistant designed for DJs and vinyl collectors. The project leverages cutting-edge LLM technology and LangChain to provide personalized setlist generation, vinyl care advice, track recommendations, and DJ mixing tips. This application bridges the gap between music enthusiasts and AI, offering tools that simplify and enhance the art of DJing and vinyl collection.

## Features

### 1. **Setlist Generator**
- Input mood, genre, or BPM to generate a curated setlist.
- Leverages Discogs metadata and LLM reasoning for smooth transitions between tracks.

### 2. **Vinyl Care Advisor**
- Chatbot powered by LangChain to offer advice on cleaning, storing, and maintaining vinyl records.

### 3. **Track Recommendation System**
- Recommends new or rare tracks based on user collections.
- Integrates Discogs API for real-time pricing and availability.

### 4. **DJ Techniques Assistant**
- Provides mixing tips, including transition strategies and beatmatching advice.

### 5. **AI-Powered Search**
- Query the system for personalized advice, such as transitioning between tracks or selecting tracks for specific vibes.

## Architecture

### Tech Stack
- **Backend**: Python, FastAPI
- **Frontend**: Streamlit
- **Database**: SQLite (expandable to Firebase or AWS RDS)
- **LLM Framework**: LangChain (OpenAI GPT or Hugging Face transformers)
- **APIs**: Discogs, Spotify, MusicBrainz (optional)

### LangChain Implementation
- **Setlist Generator Chain**:
  - Combines user preferences and Discogs metadata for custom recommendations.
- **Chatbot Chain**:
  - Uses conversational memory for interactive vinyl care advice.
- **Recommendation Chain**:
  - Analyzes user collections and metadata to suggest tracks.

## Installation

### Prerequisites
1. Python 3.9+
2. [Discogs API Key](https://www.discogs.com/developers/)
3. OpenAI API Key (or alternative for LLMs)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/guillearria/agent-vinyl.git
   cd agent-vinyl
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Add API keys:
   - Create a `.env` file in the project root:
     ```env
     DISCOGS_API_KEY=your_discogs_api_key
     OPENAI_API_KEY=your_openai_api_key
     ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

## Usage

1. **Launch the App**:
   - Open the URL provided by Streamlit in your browser.

2. **Explore Features**:
   - Navigate to the **Setlist Generator** to create playlists.
   - Use the **Vinyl Care Chatbot** for maintenance tips.
   - Check out **Track Recommendations** for expanding your collection.

3. **Feedback**:
   - Use the built-in feedback button to share your experience.

## Project Structure

```
agent-vinyl/
├── app.py                # Streamlit application
├── backend/
│   ├── api.py            # FastAPI backend
│   ├── chains.py         # LangChain workflows
│   └── database.py       # Database configuration
├── data/
│   └── sample_vinyl.csv  # Example vinyl collection data
├── utils/
│   ├── audio.py          # Audio analysis utilities
│   └── prompts.py        # LLM prompts
├── requirements.txt      # Project dependencies
└── README.md             # Project documentation
```

## Future Enhancements

1. **Audio Analysis**:
   - Use Librosa to analyze uploaded tracks for BPM and key.
2. **Mobile App**:
   - Develop a React Native or Flutter version.
3. **Multi-Agent System**:
   - Enable LangChain agents for simultaneous API queries.
4. **Community Features**:
   - Add a forum for DJs and vinyl enthusiasts to share insights.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For questions or support, please contact:
- **Author**: Guillermo Arria
- **Email**: guillermo.arriadevoe@gmail.com
- **GitHub**: [guillearria](https://github.com/guillearria)
