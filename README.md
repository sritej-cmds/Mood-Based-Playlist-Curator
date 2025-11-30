Mood-Based Playlist Curator

An agentic, context-aware music recommendation system that builds personalised playlists using mood detection, semantic RAG retrieval, real-time weather and time-of-day context, agentic reasoning, Spotify track suggestions, and reflective explanations.
Built using Python, Flask, Transformers, Sentence-BERT, FAISS, and the Spotify API

System Flow (High-Level)

User Input → Mood Classifier (BART) → Semantic Retrieval (FAISS + MiniLM) → 
Weather + Time Context → Agentic Reasoning (Playlist Intent) → 
Spotify API (Track List) → Mistral Reflection → Store Playlist → Frontend Display

Features

Mood understanding using NLP classification
Semantic RAG song lookup (MiniLM embeddings + FAISS)
Real-time weather and time-of-day context
Agent-style explanation for playlist reasoning
Spotify API integration for track fetching
Fully functional backend and clean frontend

My Contributions 

1. RAG Retrieval Layer
Implemented semantic search over songdesc.csv
Encoded descriptions with all-MiniLM-L6-v2
Built FAISS similarity lookup for mood → song mapping
Added fallback logic for ambiguous queries

2. Weather and Time-of-Day Context
Integrated OpenWeatherMap for real-time weather
Added time-of-day logic (morning/evening/night)
Injected context into playlist generation
Ensured tone/genre varies with weather and time

3. Agentic Reasoning (Playlist Intent)
Built reasoning module combining mood, weather, time and intent
Generated human-style explanations for playlist decisions

4. Reflection Module (Mistral)
Added a reflective LLM step
Designed prompts to make the explanation natural and human-like

Tech Stack

Backend: Python, Flask
NLP: BART, MiniLM, Transformers
Embeddings: Sentence-BERT
Retrieval: FAISS
Context: OpenWeatherMap API
Music: Spotify API
Frontend: HTML/CSS/JS

Installation

git clone https://github.com/sritej-cmds/Mood-Based-Playlist-Curator
cd Mood-Based-Playlist-Curator
pip install -r requirements.txt
python app_final.py

Acknowledgements

Built with teammates during the PESU I/O GenAI Hands-On Program.
Special thanks to our mentors for the guidance.
