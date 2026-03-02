# 🎙️ Assistente de Voz Multi-Idiomas com Whisper e OpenRouter

Um assistente de voz inteligente que transcreve áudio, processa linguagem natural
e responde em voz sintetizada — tudo rodando no Google Colab.

---

## 📥 Como Executar

Baixe o arquivo abaixo e faça o upload no seu próprio Google Colab:

[⬇️ Baixar Notebook](https://github.com/SEU_USUARIO/SEU_REPOSITORIO/raw/main/assistente-de-voz/Cópia_de_Assistente_de_Voz_Multi_Idiomas_Com_Whisper_e_ChatGPT.ipynb)

1. Acesse [colab.research.google.com](https://colab.research.google.com)
2. Clique em **Arquivo → Fazer upload de notebook**
3. Selecione o arquivo baixado
4. Siga as instruções dentro do notebook

---

## 📖 Sobre o Projeto

Este notebook implementa um pipeline completo de assistente de voz:

**Áudio → Transcrição → Resposta por LLM → Voz Sintetizada**

A ideia original era utilizar a API da **OpenAI (ChatGPT)** como modelo de linguagem.
Porém, devido a limitações de cota e problemas com billing, o projeto foi adaptado
para usar o **OpenRouter** — uma plataforma que oferece acesso gratuito a diversos
modelos de linguagem como Llama, Gemma e outros.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Função |
|-----------|--------|
| OpenAI Whisper | Transcrição de áudio para texto |
| OpenRouter | API de LLM gratuita (substituto do ChatGPT) |
| gTTS | Síntese de voz (texto para áudio) |
| Google Colab | Ambiente de execução |

---

## 🔄 Pipeline do Projeto

🎤 Gravação → 🔊 Whisper → 🤖 OpenRouter LLM → 🔈 gTTS

---

## ⚙️ Configuração

### Dependências
pip install openai-whisper openai gTTS

### API Key do OpenRouter
1. Crie conta gratuita em openrouter.ai
2. Acesse Keys → Create Key
3. Cole no notebook:
os.environ['OPENROUTER_API_KEY'] = 'sua-chave-aqui'

---

## 🔀 Por que OpenRouter?

| Provedor | Status | Motivo |
|----------|--------|--------|
| OpenAI (ChatGPT) | ❌ | Cota excedida |
| Anthropic (Claude) | ❌ | Exige depósito mínimo |
| Google Gemini | ❌ | Biblioteca descontinuada + cota zerada |
| OpenRouter | ✅ | Gratuito, sem cartão, múltiplos modelos |

Modelos gratuitos disponíveis:
- google/gemma-3-27b-it:free
- meta-llama/llama-3.3-70b-instruct:free
- mistralai/mistral-7b-instruct:free

💡 Todo modelo com :free no final é gratuito!

---

## 📝 Observações

- O Whisper roda localmente — não precisa de API key
- Se um modelo estiver sobrecarregado, basta trocar o nome do modelo
- A variável `language` controla o idioma da transcrição e da voz

---

## 📄 Licença

Projeto de uso educacional, livre para modificações.
