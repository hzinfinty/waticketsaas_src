# Whaticket SaaS - Plataforma de Atendimento Multi-usuários

![Status](https://img.shields.io/badge/status-ativo_e_em_desenvolvimento-green)
![Mantido por](https://img.shields.io/badge/Mantido%20por-Hyô%20Seido-blue)

Uma plataforma de código aberto para atendimento multi-usuários via WhatsApp, ideal para equipes de suporte e vendas que precisam compartilhar um único número de forma organizada e eficiente.

*Este projeto é mantido e desenvolvido por **Hyô Seido**.*

---

<details open>
<summary><strong>🇧🇷 Tutorial em Português (Clique para expandir)</strong></summary>

## ✨ Funcionalidades Principais
- **Múltiplos Atendentes:** Vários usuários atendendo em um único número de WhatsApp.
- **Filas de Atendimento (Chatbot):** Direcione clientes para o departamento certo com um chatbot inicial.
- **Respostas Rápidas:** Crie atalhos para as mensagens mais comuns.
- **Agendamento de Mensagens:** Programe o envio de mensagens para seus contatos.
- **Kanban:** Organize seus tickets em um quadro visual.
- **Tags:** Categorize seus contatos e tickets para melhor organização.

## 🛠️ Tecnologias Utilizadas
- **Frontend:** React.js, Material-UI
- **Backend:** Node.js, Express, Sequelize, TypeScript
- **Banco de Dados:** PostgreSQL
- **Serviços:** Redis para cache, Socket.IO para comunicação em tempo real.

## 🚀 Tutorial de Instalação (Servidor de Produção)

### Pré-requisitos
- Um servidor (VPS) com **Ubuntu 20.04** ou superior.
- Dois subdomínios apontados para o IP do seu servidor (ex: `app.seusite.com` e `api.seusite.com`).

### Passo 1: Acesso e Permissões
Acesse seu servidor como `root` e crie um usuário `deploy` para a instalação:
```bash
adduser deploy
usermod -aG sudo deploy

## Passo 2: Executar o Script de Instalação

sudo apt update && sudo apt install -y git \
&& git clone https://github.com/hzinfinty/waticketsaas_src.git
&& cd instalador-whaticket-main-v.10.0.1 \
&& sudo chmod +x ./install_primaria \
&& sudo ./install_primaria
