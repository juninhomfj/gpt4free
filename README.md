# GPT4Free (g4f)

[![PyPI](https://img.shields.io/pypi/v/g4f)](https://pypi.org/project/g4f)
[![Docker Hub](https://img.shields.io/badge/docker-hlohaus789%2Fg4f-blue)](https://hub.docker.com/r/hlohaus789/g4f)
[![Licença: GPL v3](https://img.shields.io/badge/License-GPLv3-red.svg)](https://www.gnu.org/licenses/gpl-3.0.txt)

<p align="center">
  <img src="https://github.com/user-attachments/assets/7f60c240-00fa-4c37-bf7f-ae5cc20906a1" alt="Logo GPT4Free" height="200" />
</p>

<p align="center">
  <strong>
    Criado por <a href="https://github.com/xtekky">@xtekky</a>,<br>
    mantido por <a href="https://github.com/hlohaus">@hlohaus</a>
  </strong>
</p>

<p align="center">
Apoie o projeto no
<a href="https://github.com/sponsors/hlohaus">GitHub Sponsors</a> ❤️
</p>

<p align="center">
Demo ao vivo & documentação: https://g4f.dev | Docs: https://g4f.dev/docs
</p>

---

GPT4Free (g4f) é um projeto orientado pela comunidade que agrega múltiplos provedores acessíveis e interfaces para tornar o trabalho com LLMs modernos e modelos de geração de mídia mais fácil e flexível.  

O GPT4Free tem como objetivo oferecer suporte a múltiplos provedores, GUI local, APIs REST compatíveis com OpenAI e clientes convenientes em Python e JavaScript — tudo sob uma licença voltada à comunidade.

Este README é um guia consolidado, aprimorado e completo para instalar, executar e contribuir com o GPT4Free.

---

## Sumário
- O que está incluído
- Links rápidos
- Requisitos & compatibilidade
- Instalação
  - Docker (recomendado)
  - Imagem Docker Slim
  - Windows (.exe)
  - Python (pip / código-fonte / instalações parciais)
- Executando a aplicação
  - GUI (cliente web)
  - FastAPI / API de Interferência
  - CLI
  - Login opcional em provedores
- Usando o cliente Python
- Usando GPT4Free.js
- Provedores & modelos
- Inferência local & mídia
- Configuração & personalização
- Executando em smartphone
- API de Interferência (compatível com OpenAI)
- Exemplos & padrões comuns
- Contribuindo
- Segurança, privacidade & política de remoção
- Créditos & atribuições
- Projetos que utilizam
- Changelog & releases
- Manifesto / princípios do projeto
- Licença
- Contato & patrocínio
- Apêndice: comandos rápidos & exemplos

---

## O que está incluído
- Biblioteca cliente em Python e cliente assíncrono.
- GUI web local opcional.
- API baseada em FastAPI compatível com OpenAI (API de Interferência).
- Cliente JS oficial para navegador (distribuição g4f.dev).
- Imagens Docker (completa e slim).
- Adaptadores multi-provedor (LLMs, provedores de mídia, backends de inferência local).
- Ferramentas para geração de imagem, áudio e vídeo com persistência de mídia.

---

## Links rápidos
- Site & docs: https://g4f.dev | https://g4f.dev/docs
- PyPI: https://pypi.org/project/g4f
- Docker: https://hub.docker.com/r/hlohaus789/g4f
- Releases: https://github.com/xtekky/gpt4free/releases
- Issues: https://github.com/xtekky/gpt4free/issues
- Comunidade:
  - Telegram: https://telegram.me/g4f_channel
  - Discord News: https://discord.gg/5E39JUWUFa
  - Discord Suporte: https://discord.gg/qXA4Wf4Fsm

---

## Requisitos & compatibilidade
- Python 3.10+ recomendado.
- Google Chrome / Chromium para provedores que usam automação de navegador.
- Docker para implantação em containers.
- Funciona em x86_64 e arm64 (a imagem slim suporta ambos).
- Alguns provedores podem exigir ferramentas específicas da plataforma.

---

## Instalação

### Docker (recomendado)

```bash
docker pull hlohaus789/g4f
docker run -p 8080:8080 -p 7900:7900 \
  --shm-size="2g" \
  -v ${PWD}/har_and_cookies:/app/har_and_cookies \
  -v ${PWD}/generated_media:/app/generated_media \
  hlohaus789/g4f:latest
