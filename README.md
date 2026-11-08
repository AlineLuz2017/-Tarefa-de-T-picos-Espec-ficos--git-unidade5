# Sistema de Recuperação de Informações (RAG) com VectorDB (FAISS) e LangChain

Este projeto consiste no desenvolvimento de um sistema de Recuperação de Informações (Information Retrieval) utilizando técnicas de Processamento de Linguagem Natural (PLN), embeddings vetoriais e a biblioteca LangChain. O sistema foi implementado em um **Jupyter Notebook no Google Colab** de forma **100% gratuita**, tendo como tema central a **Saúde Mental e Tecnologia**.

## Descrição do Projeto

O objetivo principal é demonstrar o pipeline de um sistema RAG (Retrieval-Augmented Generation) básico:
1. **Criação da base de conhecimento:** Um texto estruturado sobre os impactos da tecnologia na saúde mental.
2. **Chunking:** Divisão do texto em pequenos blocos (`chunks`) para otimizar a busca.
3. **Embeddings:** Conversão dos textos em vetores numéricos utilizando o modelo `all-MiniLM-L6-v2` (HuggingFace).
4. **Armazenamento:** Indexação dos vetores em um Banco de Dados Vetorial utilizando **FAISS**.
5. **Recuperação:** Busca por similaridade para responder de forma eficiente a dúvidas com base no contexto fornecido.

---

## Tecnologias Utilizadas

- **Google Colab** (Ambiente de execução Python em nuvem)
- **LangChain** (`langchain`, `langchain-community`, `langchain-huggingface`, `langchain-text-splitters`)
- **FAISS** (`faiss-cpu`) para indexação e busca vetorial rápida.
- **Sentence-Transformers** (`sentence-transformers`) para geração de embeddings locais.

---

## Estrutura do Repositório

```text
.
├── Avaliação 5 Topicos.ipynb  # Notebook Jupyter contendo todo o código e execuções
└── README.md                  # Documentação do projeto

## Instruções de Instalação e Execução (Via Google Colab)

1. Acesse o Google Colab (colab.research.google.com).

2. Faça o upload do arquivo Avaliação 5 Topicos.ipynb (ou abra diretamente pelo seu GitHub).

3. Na primeira célula do notebook, execute o comando de instalação das dependências:

!pip install -q langchain langchain-community langchain-huggingface faiss-cpu sentence-transformers

4. Execute as células sequencialmente para gerar o texto base, criar o banco FAISS e rodar a busca da pergunta.

## Exemplo de Pergunta e Resposta
Pergunta:

"O que é detox digital e qual a sua importância?"

Resposta Recuperada pelo Sistema:

"O "detox digital" ou pausas programadas longe de smartphones e computadores são práticas essenciais para recuperar o foco, reduzir a exaustão cognitiva e promover o bem-estar emocional."

