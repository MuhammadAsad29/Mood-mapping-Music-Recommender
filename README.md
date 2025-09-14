# 🎶 Mood Mapping Music Recommender

**Short description:** An interactive mood-based music recommender that maps user text input to music genre suggestions using internal dictionaries and simple sentiment analysis (TextBlob).

## Detailed description
This project implements a **Mood-Based Music Recommender System** that does **not** rely on external datasets. Instead, it uses **predefined Python dictionaries** to map detected moods to a set of music genres. The system analyzes user-provided text describing their mood, applies simple keyword detection and sentiment polarity (via TextBlob), and returns genre suggestions, an emoji, and a friendly message.

### Key points
- **No external datasets are used.** All mood-to-genre mappings are stored as in-notebook dictionaries.
- Mood detection is performed using keyword checks plus TextBlob polarity scoring to handle ambiguous inputs.
- The interface is interactive (built with `ipywidgets`) and displays results with emojis and a short explanation box.

## Features
- Detects moods: `happy`, `sad`, `angry`, `excited`, `relaxed`, `neutral`, and some finer states like `anxious` (if implemented).
- Returns suggested genres from internal dictionaries (example: happy → pop, dance, upbeat rock).
- Provides emoji feedback and short motivational or contextual messages.
- Lightweight — no dataset downloads required; easy to run locally.
- Suitable for demonstration, teaching, or as a frontend for a larger recommender system.

This project is ideal for students, beginners, and hobbyists who want to understand the basics of 
recommendation systems without diving into complex machine learning models.

## How it works (implementation summary)
1. User enters a free-text mood description in the notebook UI (or selects a sample).
2. The code runs simple keyword matching (e.g., 'happy', 'sad', 'angry') and computes a sentiment polarity using TextBlob.
3. The mood is assigned based on keywords and polarity thresholds.
4. A dictionary lookup returns a short list of genres associated with that mood, and the UI displays the result.

## Tech stack / dependencies
- Python 3.8+
- textblob
- ipywidgets
- jupyter (Notebook or Lab)
- (optional) pandas — only if you expand the project later to use real datasets

Install dependencies:
```bash
pip install textblob ipywidgets
python -m textblob.download_corpora
```

## How to run
1. Clone the repository and open the notebook (example filename used here):
```bash
git clone https://github.com/MuhammadAsad29/Mood-mapping-Music-Recommender.git
cd mood-mapping-music-recommender
jupyter notebook "Mood mapping Music Recommender.ipynb"
```

2. Run the notebook cell that builds and displays the widget UI. Interact by typing your mood and clicking the recommendation button (or enable live re-analysis).

## Example mapping (illustrative)
```python
mood_to_genres = {
    "happy": ["pop", "dance", "upbeat rock"],
    "sad": ["acoustic", "blues", "indie folk"],
    "relaxed": ["ambient", "chillout", "lo-fi"],
    "angry": ["metal", "hard rock", "punk"],
    "excited": ["edm", "electro", "pop"],
    "neutral": ["ambient", "electronic", "instrumental"]
}
```

## Notes & next steps
- If you later want more sophisticated recommendations, you can replace the dictionaries with a dataset-driven approach (Spotify audio features, collaborative filtering, or content-based models).
- The project is intentionally simple and suitable for demonstrations.

---
**Author:** Muhammad Asad
