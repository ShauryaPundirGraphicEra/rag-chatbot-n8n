# 📚 RAG Chatbot with n8n + OpenAI + Pinecone

This project is a no-code/low-code **AI chatbot** that uses Retrieval-Augmented Generation (RAG) to provide contextual responses based on PDF documents uploaded to Google Drive.

## 🚀 Features

- Uses **n8n** to orchestrate the RAG pipeline
- Automatically processes uploaded PDFs (e.g., books like *Atomic Habits*)
- Embeds chunks using **OpenAI**
- Stores/retrieves vectors using **Pinecone**
- Responds to user chat input using **OpenRouter LLM**

## 🧠 Use Case

- Upload a self-help book or documentation
- Ask contextual questions like "How can I build better habits?"
- Get AI-powered responses based directly on document content

## 📂 Workflow Overview

- `Google Drive Trigger`: Watches for new file uploads
- `Data Loader` → `Text Splitter` → `Embeddings` → `Pinecone Vector Store`
- `Chat Trigger` receives user input
- Uses **retrieved vectors + LLM** to generate a final answer

## 🛠️ Tools Used

- [n8n.io](https://n8n.io/)
- [OpenAI API](https://platform.openai.com/)
- [Pinecone Vector DB](https://www.pinecone.io/)
- [Google Drive API](https://developers.google.com/drive)
- [OpenRouter](https://openrouter.ai/)

## 🔐 Note on Credentials

This project does not include API keys or credentials. Please configure those in your own secure n8n instance.

## 📸 Demo

![Screenshot of Chat UI or Workflow](images/demo-screenshot.png)

## 🤖 Future Improvements

- Add UI for chat
- Swap OpenRouter with custom model
- Add version with code (Python + LangChain)

## 📄 License

MIT
