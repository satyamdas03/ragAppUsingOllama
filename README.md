Semantic Search using Retrieval Augmented Generation (RAG)
In this project, we will create a web application that allows users to input a URL and a question, and the application will use Retrieval Augmented Generation (RAG) to provide a relevant answer.
Broad Steps

Load the Data: Load the data from the provided URL using the WebBaseLoader.
Create the Embeddings and Save in a Vector Database (FAISS): Split the data into smaller chunks using the RecursiveCharacterTextSplitter, and then convert the chunks into embeddings using the OllamaEmbeddings. Store the embeddings in a vector database (FAISS).
Implement the RAG: Use the RAG model to retrieve the most relevant information from the vector database based on the user's question, and then use a Language Model to generate the final answer.

Main Understanding of the Code Methodologies

Loading the Data: We will use the WebBaseLoader to load the data from the provided URL.
Splitting the Data: The RecursiveCharacterTextSplitter will be used to split the data into smaller chunks.
Creating the Embeddings: The OllamaEmbeddings will be used to convert the data chunks into embeddings and store them in the FAISS vector database.
Parsing the Output: The StrOutputParser will be used to parse the output from the RAG model.

Implementation Details
rag.py

Step 1: Load the data from the provided URL using the WebBaseLoader. Split the text into smaller chunks using the RecursiveCharacterTextSplitter.
Step 2: Create the embeddings using the OllamaEmbeddings and store them in the FAISS vector database.
Step 3: Create a function to call the Ollama model, providing the user's question and the relevant context from the webpage.
Step 4: Set up the RAG, including initializing the retriever and combining the relevant sections of the webpage to send to the Language Model.
Step 5: Set up the RAG for the entire process.

ui.py

Step 1: Import the necessary libraries, including the nomic-embed-text for embedding the webpage content.
Step 2: Create a Gradio interface with two inputs (URL and question) and one output (the response from the Language Model).
Step 3: Launch the Gradio interface and allow users to input a URL and a question, which will then be processed using the RAG model to provide a relevant answer.

Usage

Run the ui.py script to start the web application.
In the web application, enter the URL of the webpage you want to search and the question you want to ask.
The application will then use the RAG model to retrieve the relevant information from the webpage and generate a response to the question.
