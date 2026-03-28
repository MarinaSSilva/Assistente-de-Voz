# 🎙️ Assistente de Voz Inteligente: ChatGPT + Whisper

Este é um projeto inovador que une o poder do Whisper e do ChatGPT (modelos de machine learning da OpenAI) para criar um assistente de voz multi-idiomas. O assistente é capaz de compreender o usuário, processar a pergunta de forma inteligente e responder via áudio, proporcionando uma experiência de comunicação fluida e natural.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1s32kzk2NIGfQDVBbw57enZITNtYAgRnh)

O projeto foi desenvolvido inteiramente no Google Colab, facilitando o teste em tempo real sem a necessidade de configurações complexas de ambiente local.

## 🚀 Tecnologias Utilizadas

*   Python: Linguagem principal do projeto.
*   JavaScript: Utilizado para captura de áudio via navegador (WebRTC).
*   OpenAI Whisper: Modelo poderoso para reconhecimento de fala e transcrição.
*   OpenAI ChatGPT (GPT-3.5 Turbo): Modelo de linguagem para geração de respostas inteligentes.
*   gTTS (Google Text-to-Speech): Biblioteca para sintetizar a resposta de texto em fala.

## 🛠️ O Ciclo de Interação (4 Etapas Cruciais)

O funcionamento do assistente é dividido em quatro passos fundamentais:

1.  Gravação de Áudio: Captura o áudio do usuário diretamente do navegador usando uma Promise em JavaScript e processa o arquivo binário em Python, salvando-o como `.wav`.
2.  Reconhecimento de Fala (Whisper): O modelo Whisper (small) transcreve o áudio gravado em texto com alta precisão, inclusive em português.
3.  Inteligência Contextual (ChatGPT): O texto transcrito é enviado para a API da OpenAI, onde o modelo GPT-3.5 Turbo gera uma resposta baseada na pergunta do usuário.
4.  Síntese de Voz (gTTS): A resposta textual é convertida em um arquivo de áudio MP3, permitindo que o assistente "fale" a resposta automaticamente.

## 📋 Pré-requisitos

Para rodar este projeto, você precisará de:
*   Uma conta no Google para acessar o Colab.
*   Uma API Key da OpenAI. Você pode gerá-la gratuitamente no site da OpenAI, embora o uso do modelo GPT-3.5 esteja sujeito a limites de quota e saldo da plataforma.

## 🔧 Configuração Rápida

1.  Idioma: O projeto está configurado por padrão para o idioma português (`pt`), mas pode ser facilmente alterado na variável global `language`.
2.  Modelo Whisper: Utilizamos o modelo `small` por ser equilibrado entre velocidade e precisão, mas você pode testar as versões `tiny`, `medium` ou `large` no código.
3.  API Key: Insira sua chave no campo `client = OpenAI(api_key="SUA_CHAVE_AQUI")` na etapa 3.

## 💡 Possibilidades Futuras

Este projeto abre portas para diversas aplicações, tais como:
*   Acessibilidade: Integração com avatares de Libras para tradução de áudio em tempo real.
*   Automação Residencial: Comando de dispositivos inteligentes por voz.
*   Educação: Criação de conteúdos audíveis interativos.

---
*Este projeto foi desenvolvido como parte de um estudo sobre IA e processamento de linguagem natural na plataforma DIO.*
