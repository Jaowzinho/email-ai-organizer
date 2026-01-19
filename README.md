# 📧 Email AI Organizer (n8n)

Projeto de automação que utiliza **n8n + Inteligência Artificial** para analisar, classificar e organizar e-mails automaticamente em uma planilha do **Google Sheets**.

---

## 🚀 Funcionalidades

- 📥 Coleta e-mails automaticamente do Gmail
- 🤖 Analisa o conteúdo usando IA
- 🏷️ Classifica os e-mails por:
  - Categoria (Estudo, Financeiro, Trabalho, Promoção, etc.)
  - Prioridade (Alta, Média ou Baixa)
- 📝 Gera resumo objetivo e ação sugerida
- 📊 Salva cada e-mail como uma linha no Google Sheets
- ⏱️ Executa automaticamente via agendamento

---

## 🛠️ Tecnologias Utilizadas

- **n8n** – Orquestração da automação
- **Gmail API** – Leitura dos e-mails
- **IA (LLM)** – Análise e classificação dos e-mails
- **JavaScript (Code Node)** – Tratamento e padronização dos dados
- **Google Sheets API** – Armazenamento organizado das informações

---

## 🔄 Fluxo da Automação

1. ⏰ Schedule Trigger
2. 📧 Get many messages (Gmail)
3. 🔀 Split Out (1 e-mail por vez)
4. ⏳ Wait (controle de rate limit)
5. 🤖 Message a model (IA)
6. 🧠 Code Node (tratamento do JSON)
7. 📊 Append row in Google Sheets

---

## 📋 Estrutura dos Dados no Sheets

Cada e-mail gera uma linha com as seguintes colunas:

- Assunto  
- Remetente  
- Categoria  
- Prioridade  
- Resumo  
- Ação sugerida  

---

## ⚠️ Observações Importantes

- O projeto utiliza apenas o **snippet** dos e-mails (não acessa o corpo completo)
- Não inventa informações
- Possui controle de **rate limit** para evitar bloqueio da IA
- Ideal para organização pessoal, estudos e produtividade

---

## 📌 Possíveis Melhorias Futuras

- Agrupar e-mails por prioridade
- Envio de notificações para e-mails críticos
- Dashboard visual
- Suporte a múltiplas contas de e-mail
