# N8N-Typebot-EvolutionAPI

Sistema completo de automação para atendimento via WhatsApp com captura inteligente de leads e integração com Google Sheets

## 📋 Sobre o Projeto

Este projeto implementa um bot de atendimento automatizado para WhatsApp que:

- ✅ Recebe e processa mensagens de clientes
- ✅ Apresenta menu interativo de opções
- ✅ Captura informações de leads automaticamente
- ✅ Registra todas as interações em Google Sheets
- ✅ Organiza dados por etapas do funil de vendas

### 🎯 Caso de Uso

Sistema desenvolvido para empresa de estruturas metálicas que automatiza o primeiro contato com clientes interessados em:
- **Porta-Paletes**
- **Mini Porta-Paletes**

## 📸 Screenshots

<div align="center">
  
### Fluxo do TypeBot
<img src="./screenshots/typebot-flow.png" alt="Fluxo TypeBot" width="800"/>

### Workflow N8N
<img src="./screenshots/n8n-workflow.png" alt="Workflow N8N" width="800"/>

### Bot em Ação
<img src="./screenshots/bot-whatsapp.png" alt="Bot WhatsApp" width="400"/>

### Integração Google Sheets
<img src="./screenshots/google-sheets.png" alt="Google Sheets" width="800"/>

</div>

> 💡 **Nota:** Adicione suas capturas de tela na pasta `screenshots/` na raiz do projeto.

## 🏗️ Arquitetura

```
WhatsApp → TypeBot → Webhook (N8N) → Google Sheets

## 📊 Fluxo de Dados

1. **Início**: Cliente envia mensagem no WhatsApp
2. **Captura**: TypeBot captura dados iniciais (nome, telefone, data/hora)
3. **Webhook**: Dados são enviados para N8N via webhook
4. **Validação**: N8N verifica se é novo lead ou lead em etapa
5. **Gravação**: 
   - Novo lead → Grava na aba "Página1"
   - Lead em etapa → Grava na aba "Etapas"
6. **Continuação**: Bot continua fluxo de acordo com opção escolhida
