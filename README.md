# Stripe Documentation RAG

A RAG (Retrieval-Augmented Generation) chatbot that answers questions about Stripe API using local LLM and vector search.

## Output Example
```
You: How do webhooks work?

Answer: Webhooks allow your application to receive real-time notifications
about events in your Stripe account. When an event occurs, Stripe sends
an HTTP POST request to your endpoint with event details.

Sources:
  - https://stripe.com/docs/webhooks
```

## How It Works
```
User Question
      ↓
Convert to Embedding
      ↓
Search Chroma Vector DB
      ↓
Retrieve Relevant Docs
      ↓
Qwen generates Answer
```

## Stack

- Qwen 2.5-1.5B-Instruct — Local LLM
- ChromaDB — Vector Database
- Sentence Transformers — Embeddings
- BeautifulSoup — Web Scraping
- LangChain — Text Splitting

## Data Sources

- stripe.com/docs/api
- stripe.com/docs/payments
- stripe.com/docs/billing
- stripe.com/docs/webhooks
- docs.stripe.com/api/authentication
- docs.stripe.com/api/errors
