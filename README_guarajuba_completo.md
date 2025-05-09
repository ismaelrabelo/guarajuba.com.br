
# guarajuba.com.br

**Guia Turístico e Imobiliário com automação via IA para geração de conteúdo e captação de leads para imóveis no litoral norte da Bahia.**

[![Deploy Status](https://img.shields.io/badge/deploy-ready-brightgreen)](https://guarajuba.com.br)
[![Plataforma IA](https://img.shields.io/badge/IA-integrada-blue)](#)
[![Feito com ❤️ por Litoral Bahia Imobiliária](https://img.shields.io/badge/feito%20por-Litoral%20Bahia-red)](https://litoralbahia.com.br)

---

## ✨ Visão Geral

Este repositório contém:

- **Frontend (Next.js)** com foco em SEO
- **Backend (Strapi CMS)** com campos preparados para conteúdo gerado por IA
- **Automação com IA (OpenAI)** para geração e publicação de artigos semanais
- **Docker + NGINX + HTTPS**

---

## 🚀 Como rodar em produção

```bash
# 1. Subir os serviços com Docker
docker compose up -d

# 2. Configurar HTTPS com Certbot
certbot --nginx -d guarajuba.com.br -d www.guarajuba.com.br
```

---

## 🧠 Automação com IA

O script `automacao_ia_strapi_guarajuba.py` publica artigos otimizados com:

- SEO local (Guarajuba, turismo, imóveis)
- CTA para o site [litoralbahia.com.br](https://litoralbahia.com.br)
- Publicação automática via API do Strapi

Configure o `.env` com:

```env
STRAPI_TOKEN=Bearer sua_token_aqui
OPENAI_KEY=sk-sua-chave-aqui
STRAPI_URL=http://localhost:1337/api/posts
```

Agende com cron para rodar semanalmente.

---

## 🧱 Estrutura do Projeto

```
guarajuba.com.br/
├── frontend/          # Site Next.js
├── backend/           # Strapi CMS
├── scripts/           # Scripts de automação com IA
├── docker-compose.yml
├── nginx-guarajuba.conf
├── .env.exemplo
└── README.md
```

---

## ⚡ Requisitos

- Docker e Docker Compose
- Conta OpenAI com chave de API
- Domínio configurado (guarajuba.com.br)
- Acesso root ou sudo no servidor

---

## © Licença

Projeto público mantido por [Litoral Bahia Imobiliária](https://litoralbahia.com.br). Livre para uso e modificação com créditos.
