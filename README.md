The pipeline loads documents, splits them into smaller chunks, converts each chunk into vector embeddings using a SentenceTransformer model, and stores them in ChromaDB.
When a user asks a question, the query is embedded and compared against stored vectors using cosine similarity. The most relevant chunks are retrieved and injected into the LLM prompt to generate an accurate response.
