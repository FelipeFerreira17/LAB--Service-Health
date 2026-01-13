# LAB  – Verificação de Incidente no Azure (Service Health)

## Contexto
Antes de iniciar qualquer troubleshooting em recursos do cliente,
é fundamental validar se o problema é causado por um incidente
no próprio Azure.

Este laboratório simula o primeiro passo de um atendimento
de Suporte Cloud N1.

---

## 🎯 Objetivo
- Verificar se há incidentes ativos no Azure
- Identificar a região e o serviço afetado
- Determinar a responsabilidade (Azure x Cliente)
- Registrar corretamente a verificação no ticket

---

## 🧠 Cenário
Usuário informa que a aplicação está fora do ar.
Ainda não há confirmação se o problema é do Azure
ou do ambiente do cliente.

---

## 🪜 Passo a Passo

### Passo 1 – Acessar o Portal Azure
1. Acesse https://portal.azure.com
2. Faça login com sua conta Azure

---

### Passo 2 – Localizar o Service Health
1. No menu lateral, clique em **All services**
2. Procure por **Service Health**
3. Clique em **Service Health**

---

### Passo 3 – Verificar Incidentes Ativos
Na tela do Service Health, analise:

- **Service issues**
- **Planned maintenance**
- **Health advisories**

Verifique:
- Nome do serviço afetado
- Status do incidente
- Regiões impactadas

---

### Passo 4 – Verificar a Região do Recurso
1. Identifique em qual **região Azure** o recurso do cliente está
   - Exemplo: Brazil South
2. Compare com as regiões listadas no incidente

📌 Se a região do cliente **não estiver listada**, o problema
provavelmente **não é do Azure**.

---

### Passo 5 – Analisar Detalhes do Incidente (se existir)
Se houver incidente:
- Leia o resumo
- Verifique:
  - Horário de início
  - Impacto
  - Status (Investigating / Resolved)

📌 Não tente corrigir recursos do cliente enquanto o incidente estiver ativo.

---

### Passo 6 – Conclusão da Análise
Existem dois cenários possíveis:

#### ✅ Cenário A – Existe incidente do Azure
- Serviço afetado
- Região afetada
- Responsabilidade: Microsoft Azure

➡️ Ação N1:
- Informar o cliente
- Acompanhar atualização do Azure
- Registrar no ticket

---

#### ✅ Cenário B – NÃO existe incidente do Azure
- Nenhum problema registrado para o serviço/região

➡️ Ação N1:
- Prosseguir com troubleshooting do ambiente do cliente
- Registrar a verificação no ticket

---

## 📝 Registro no Ticket (Exemplo)

```text
Verificação inicial realizada no Azure Service Health.
Nenhum incidente ativo identificado para o serviço e região utilizados.
Responsabilidade do ambiente do cliente.
