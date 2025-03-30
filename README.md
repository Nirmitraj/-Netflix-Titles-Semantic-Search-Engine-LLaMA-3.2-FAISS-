# -Netflix-Titles-Semantic-Search-Engine-LLaMA-3.2-FAISS-
What it does:
Parses a dataset of Netflix titles (netflix_titles.csv) containing metadata like title, director, cast, genre, release year, and description.
Generates a textual representation of each movie or show by combining its key attributes into a structured prompt.
Sends each text to a local LLaMA 3.2 embedding server (via http://localhost:11434/api/embeddings) to generate 3072-dimensional embeddings.
Stores these embeddings in a FAISS index using IndexFlatL2 for fast nearest-neighbor search.
Enables users to input a favorite movie and retrieve the top-k semantically similar titles, based on vector similarity rather than just keyword matching.
