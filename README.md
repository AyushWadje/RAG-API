<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a RAG API with FastAPI



**Author:** Ayush Wadje  


---

## Introducing Today's Project!

In this project, I'm going to build a RAG API with fast API with chorma DB and ollma for LLM
This will help me retrive the relative infromation without training the model again and again.
I'm interested in this because this is a new learing topic for me

### Key tools and concepts

The key tools I used include RAG , chromaDB , fastapi, uvicorn server. Key concepts I learnt include RAG and working of  Fastapi 

### Challenges and wins

This project took me approximately 1.5 hr. The most challenging part was setting up the ollama and using the swagger UI of fast api

## Performing RAG Manually

In this step, I'm going to create a virtual environment of python and installing all the dependencies and pulling the nomic model .
RAG stands for Retrivel Augmented Generation.

![Image](https://nextwork.ai/content_rose_majestic_fennel/uploads/99ec4595-3d7b-5584-a799-aafb9c373bbb_v3j7x5b9)

### Understanding the three parts of RAG

I performed RAG manually by pull the model form Ollama and run the model and addind some personal context . The three parts are retrievel , augumentation, generation

### Comparing the two AI models

The key difference I noticed is nomic embed-text is a model that will convert the text into vertors that are called vertor model . ,text who have a similar meaning get togather.

## Building a Personal Knowledge Base

In this step, I'm going to create a personal documentatio about the me and convert into embeddings. Embeddings are vectors which are similar word are get grouped.

![Image](https://nextwork.ai/content_rose_majestic_fennel/uploads/99ec4595-3d7b-5584-a799-aafb9c373bbb_g3h7m2r5)

### Creating the profile document

I included information about in me in the profile.txt file in that fill given the infromation about me and what I do what is my tech stack and what I like to do in my life and shared a personal infromation about a moment.

### How semantic search finds relevant chunks

When I ask a question, ChromaDB send the tetx to nomic-embed-text and it get converted into vectors and each is 768 dimenisonal and the chromaDB find a vectors who has the related meaning rather than exactly matching the text

## Creating the RAG API with FastAPI

In this step, I'm going to build an API that that wil connect the Rag to user and it send a URL request and get a structured data back which is user is ask for . I'll test it using it own UI which is Swagger UI

![Image](https://nextwork.ai/content_rose_majestic_fennel/uploads/99ec4595-3d7b-5584-a799-aafb9c373bbb_j5m1r8t2)

### How the /ask endpoint works

When a question comes in, my endpoint first taks will be retrieves the when a Question gets ask and 2 will be get the most relevent Chunks form the chromaDB and 3 will be generating a answer form this.

### Testing with Swagger UI

I tested my API by asking what is my name ?. The AI answered with your name is Ayush Wadje. The context used was from the Document which I Provide it creating the vectors and storing in the chromaDB

## Extending to a Multi-User AI Directory

In this project extension, I'm adding multi-user support because... Multi-tenancy means Adding multi-user support teaches you dynamic documentingestion, metadata filtering in      vector databases, and basic multi-tenancy
patterns.

![Image](https://nextwork.ai/content_rose_majestic_fennel/uploads/99ec4595-3d7b-5584-a799-aafb9c373bbb_d5g9k3n7)

### Adding the POST /documents endpoint

In this project extension, I added a POST endpoint that... Metadata filtering allows Adding multi-user support teaches you dynamic document ingestion, metadata filtering in vector databases, and basic multi-tenancy
patterns.

![Image](https://nextwork.ai/content_rose_majestic_fennel/uploads/99ec4595-3d7b-5584-a799-aafb9c373bbb_r8t2w6y1)

### Verifying multi-user filtering

In this project extension, I tested multi-user queries by ask  a question but not mentions any name of the user  .The filter works because when a added the name filter of the user it is giving me the specfic information about that particular user

## Wrapping Up

I did this project today to learn how to use rag and fatsapi Another skill I want to learn is adding a frontend to it to any user can visit the website and deploy the project

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/99ec4595-3d7b-5584-a799-aafb9c373bbb)*
