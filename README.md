# dio-desafios-n8n

# 🎯 Desafio Criativo: Planejando Automações com N8N Usando Apenas Bons Prompts

---

## 🧱 Passo 1: Defina a automação desejada

**Quero criar uma automação no N8N para:**
Automatizar a gestão semanal de agenda de clientes, registrando compromissos no Google Agenda, fazendo acompanhamento durante a semana e gerando relatórios de atividades concluídas.

**Público ou responsável:**
Assistente virtual/freelancer e o cliente atendido.

**Resultado esperado:**
Cadastrar automaticamente novos compromissos na agenda, checar o status de conclusão das atividades ao longo da semana, gerar uma Memória Semanal de Atividades (ATA) aos domingos e solicitar a lista de novos compromissos para a semana seguinte.

---

## 🧱 Passo 2: Adicione contexto e regras

**Ferramentas envolvidas:**
WhatsApp (via Z-API ou Evolution API), Google Agenda, OpenAI (ChatGPT) e Google Sheets (ou Notion).

**Fluxo desejado:**
1. **Entrada de compromissos:** Receber as mensagens com os compromissos enviados pelo cliente no WhatsApp, extrair os dados (data, hora, título) usando IA e cadastrar no Google Agenda e na planilha de controle.
2. **Checagem de status (Durante a semana):** Enviar mensagens automáticas pelo WhatsApp nos dias/horários definidos para perguntar ao cliente se determinados compromissos foram realizados.
3. **Fechamento e ATA (Domingo):** Compilar o status de todos os compromissos da semana, usar a IA para formatar a "Memória Semanal de Atividades e Compromissos" e enviar o resumo formatado para o cliente no WhatsApp.
4. **Solicitação da nova semana (Domingo):** Enviar uma mensagem automática solicitando os compromissos da próxima semana para reiniciar o ciclo.

**Regras importantes:**
- Ignorar mensagens que não contenham datas ou dados claros de compromissos.
- Se o cliente responder ao acompanhamento que um compromisso foi "cancelado" ou "adiado", atualizar o status correspondente na planilha antes de gerar a ATA.
- O relatório de domingo (ATA) deve conter obrigatoriamente duas seções: "Compromissos Concluídos" e "Compromissos Pendentes/Reagendados".

---

## 🧱 Passo 3: Prompt Final

Atue como um especialista em N8N e engenharia de automação.
Crie uma automação para gerenciar e acompanhar a agenda semanal de um cliente, incluindo o cadastro de compromissos, acompanhamento de status e geração de relatório de fechamento.

Público:
Assistente virtual e cliente final.

Ferramentas envolvidas:
WhatsApp Webhook API, Google Calendar, OpenAI GPT-4o e Google Sheets.

Fluxo:
1. Receber áudio ou texto do cliente no WhatsApp com compromissos e usar o nó da OpenAI para extrair título, data e horário, salvando no Google Calendar e numa planilha do Google Sheets.
2. Agendar checagens automáticas durante a semana no WhatsApp perguntando se as tarefas agendadas foram concluídas.
3. Todo domingo, buscar os registros da semana no Google Sheets, gerar o documento "Memória Semanal de Atividades e Compromissos" formatado via IA e enviar o resumo no WhatsApp do cliente.
4. Após o envio da ATA, disparar uma mensagem automática solicitando a lista de novos compromissos para a semana seguinte.

Regras:
- Tratar dados incompletos ou ambíguos pedindo confirmação antes de agendar no Google Calendar.
- Atualizar o status de cada tarefa no Google Sheets ("Concluído", "Pendente" ou "Reagendado") com base na resposta do cliente durante a semana.
- Separar o relatório final em compromissos realizados e pendentes.

Explique quais nós do N8N devem ser utilizados (ex: Webhook, OpenAI, Google Calendar, Google Sheets, Cron/Schedule Trigger, Switch) e a lógica detalhada do fluxo do workflow.
