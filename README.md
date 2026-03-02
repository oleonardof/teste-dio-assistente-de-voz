# Assistente de Voz Multilíngue com Whisper e OpenRouter

Este projeto demonstra como criar um assistente de voz simples dentro de um Jupyter Notebook ou Google Colab. O fluxo permite gravar áudio no navegador, transcrever a fala com Whisper, enviar o texto para um modelo de linguagem e gerar uma resposta que é convertida novamente em áudio.

A ideia inicial era utilizar a API do ChatGPT diretamente. Durante os testes ocorreram limitações relacionadas ao uso da API, então a implementação foi adaptada para utilizar o OpenRouter. O OpenRouter funciona como um gateway que permite acessar diferentes modelos de linguagem através de uma única API.

O objetivo do notebook é mostrar, de forma prática, como integrar captura de áudio, reconhecimento de fala, modelos de linguagem e síntese de voz em um único fluxo.

---

## Como o assistente funciona

O funcionamento segue uma sequência simples:

1. O usuário grava um áudio diretamente no navegador.
2. O áudio é enviado para o ambiente Python.
3. O Whisper realiza a transcrição da fala para texto.
4. O texto é enviado para um modelo de linguagem via OpenRouter.
5. O modelo gera uma resposta em texto.
6. A resposta é convertida em áudio usando gTTS.

Fluxo resumido:

Usuário fala → gravação no navegador → Whisper (speech to text) → modelo de linguagem via OpenRouter → resposta em texto → gTTS (text to speech) → áudio da resposta.

---

## Tecnologias utilizadas

Python  
Whisper  
OpenRouter API  
gTTS (Google Text to Speech)  
JavaScript MediaStream API  
Jupyter Notebook ou Google Colab  

---

## Como executar

Primeiro clone o repositório:


