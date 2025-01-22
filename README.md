# ai-powered-chatbot
AI-powered chatbot for querying supplier and product information using FastAPI, React, and LangGraph.
# AI-powered Chatbot for Supplier and Product Information

This project is an AI-powered chatbot built to query a **supplier** and **product** database. It uses **FastAPI** for the backend, **React** for the frontend, **LangGraph** for agent workflows, and **Hugging Face Transformers** for summarization of product and supplier data.

## Features
- Users can interact with the chatbot using natural language.
- The chatbot can retrieve product and supplier information from a **MySQL** or **PostgreSQL** database.
- Data is summarized using the **Hugging Face transformers pipeline**.
- Responsive user interface built with **React** and **Material UI** or **Tailwind CSS**.
- Scalable and extensible with **LangGraph**.

## Tech Stack
- **Backend**: FastAPI, LangGraph, Hugging Face Transformers, MySQL/PostgreSQL
- **Frontend**: React, Axios, Material UI/Tailwind CSS
- **Database**: MySQL or PostgreSQL
- **LLM for Summarization**: Hugging Face's **BART** model or any other transformer model

## Installation

### Backend
1. Clone the repository and navigate to the backend folder:
   ```bash
   git clone https://github.com/<your-username>/ai-powered-chatbot.git
   cd ai-powered-chatbot/backend



How It Works
The backend is a FastAPI server that uses LangGraph to interact with the MySQL/PostgreSQL database.
The chatbot queries the database for product and supplier information based on natural language input, and returns a structured response.
The data is then passed through a summarization model (using Hugging Face's BART or similar) to generate a more concise version of the response.
The frontend (React) displays the chat interface, allowing the user to input queries and view the responses.
Example Queries:
"Show me all products under brand X."
"Which suppliers provide laptops?"
"Give me details of product ABC."

API Endpoints
POST /query/
This endpoint takes a query in natural language and returns the corresponding product or supplier data.

Request Body:


{
  "query": "Show me all products under brand X"
}
Response:

{
  "query": "Show me all products under brand X",
  "result": "Product ABC details...",
  "summary": "High performance laptop from BrandX."
}
Notes
Ensure that your MySQL or PostgreSQL database is running and accessible.
The chatbot can be extended with more features like authentication, advanced query handling, and multiple summarization models.
You can also deploy the backend and frontend separately if required, using Docker or cloud platforms like AWS, Heroku, or Vercel.

