# Vector Databases

## Passo 1 - Introdução a Banco de Dados Vetoriais
Obsidian 

## Passo 2 - Deploy do Qdrant (VectorDB)
```bash
docker compose up
```
Acesso via browser em: http://localhost:6333/dashboard#/collections

## Passo 3 - Trabalhando com textos
Vamos utilizar os Embeddings da OpenAI para texto

```python
from langchain_openai import OpenAIEmbeddings
embedding_model = OpenAIEmbeddings()
```

## Passo 4 - Trabalhando com imagens
Vamos utilizar o modelo CLIP para embedding de images e texto

```python
model = llm.get_embedding_model("clip")
```

## Passo 5 - Transformando em API
Nosso DB pode ser acessado normalmente por uma API

```python
uvicorn 01_api:app --reload
```


## Passo 6 - Primeiro RAG

Navegar para dentro da pasta
```bash
cd src/edai_0001/06-rag
```
Executar RAG
```bash
uv run 01_basic_rag.py
```