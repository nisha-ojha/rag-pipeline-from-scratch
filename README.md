The pipeline loads documents, splits them into smaller chunks, converts each chunk into vector embeddings using a SentenceTransformer model, and stores them in ChromaDB.
When a user asks a question, the query is embedded and compared against stored vectors using cosine similarity. The most relevant chunks are retrieved and injected into the LLM prompt to generate an accurate response.
I convert both the query and document chunks into dense embeddings using a transformer model. Then I compute cosine similarity between the query vector and stored vectors in ChromaDB. Cosine similarity measures the angle between vectors, allowing semantically similar texts to have higher similarity scores. I retrieve the top-k most similar chunks and pass them to the LLM for grounded generation.

FAST API INTEGRATION
converted the RAG project into a real backend API server using FastAPI


