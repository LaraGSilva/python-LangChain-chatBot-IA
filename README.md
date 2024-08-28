# Chatbot com Inteligencia Artificial - Eurofarma

Este projeto tem como objetivo desenvolver um chatbot inteligente utilizando a biblioteca LangChain e a API do OpenAI para fornecer informações detalhadas sobre a Eurofarma, suas operações e benefícios.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- **`app.py`**: Arquivo principal da aplicação Streamlit que executa o chatbot e lida com a interface do usuário.
- **`util/`**: Diretório contendo funções utilitárias:
  - **`embeddings.py`**: Funções para criar e gerenciar o `vectorstore` e a cadeia de conversação.
  - **`file.py`**: Funções para processar arquivos e criar blocos de texto.
- **`html/`**: Diretório contendo templates HTML usados na aplicação:
  - **`template.py`**: Templates HTML para exibir as mensagens do chatbot.
- **`img/`**: Diretório com imagens usadas na aplicação, como logos e ícones.

## Dependências

- `streamlit`
- `streamlit-chat`
- `langchain`
- `openai`

## Fluxo da LLM

1. **Carregamento dos Documentos**:
   - O usuário faz o upload de documentos através da interface do Streamlit.
   - Os arquivos são processados e o texto é extraído e dividido em blocos (chunks).

2. **Criação do Vectorstore**:
   - Os blocos de texto são transformados em vetores usando técnicas de embeddings.
   - Esses vetores são armazenados em um `vectorstore` para facilitar a recuperação eficiente de informações.

3. **Configuração da Cadeia de Conversação**:
   - A cadeia de conversação é configurada utilizando o `vectorstore` criado.
   - Isso permite que o chatbot compreenda e responda às consultas com base nas informações armazenadas.

4. **Interação com o Chatbot**:
   - Quando um usuário faz uma pergunta, o chatbot consulta a cadeia de conversação.
   - A LLM (Language Model) do OpenAI é usada para gerar uma resposta com base na consulta e nas informações do `vectorstore`.
   - A resposta é então exibida ao usuário na interface do Streamlit.

5. **Feedback e Treinamento**:
   - O chatbot é monitorado e ajustado conforme necessário para melhorar a precisão e a relevância das respostas.
   - O feedback dos usuários pode ser utilizado para treinar e aprimorar o modelo continuamente.

## Tela inicial: upload do documento
![image](https://github.com/user-attachments/assets/37db15f2-627d-4cf4-9f32-06810c8e76d5)


## Tela: Fluxo pergunta e resposta (Bot e User)
![image](https://github.com/user-attachments/assets/eac51320-33cd-4f51-99eb-60b7d3bf6fc8)

Desenvolvido por Lara Gonçalves da Silva.

