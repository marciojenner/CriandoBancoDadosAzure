# Desafio DIO — Criação de Banco de Dados SQL no Azure Web Portal (ESCOLA_DB_DIO)

Este repositório documenta o laboratório da DIO cujo objetivo é praticar a **criação e configuração de um Banco de Dados SQL diretamente pelo Azure Web Portal** (portal.azure.com).  
O entregável consiste em registrar **resumos, anotações e dicas** para servir como material de apoio em estudos e futuras implementações.

---

## 🎯 Objetivos de aprendizagem

- Aplicar os conceitos aprendidos em um ambiente prático (Azure);
- Documentar processos técnicos de forma clara e estruturada;
- Utilizar o GitHub como ferramenta para compartilhar documentação.

---

## 🧩 Recurso criado

- **Serviço:** Azure SQL Database
- **Nome do Banco de Dados:** `ESCOLA_DB_DIO`
- **Provisionamento:** feito **diretamente no Azure Web Portal**

> Observação: no Azure SQL Database o banco é criado dentro de um **SQL Server lógico** (logical server), que também é criado/configurado no Portal.

---

## ✅ Pré-requisitos

- Conta ativa no Microsoft Azure
- Acesso ao **Azure Web Portal**: https://portal.azure.com

---

## 🛠️ Passo a passo — Criando pelo Azure Web Portal

### 1) Criar um Resource Group (Grupo de Recursos)
1. Acesse **portal.azure.com**
2. No campo de busca, digite **Resource groups**
3. Clique em **Create**
4. Preencha:
   - **Subscription:** (sua assinatura)
   - **Resource group:** `rg-escola-dio` (exemplo)
   - **Region:** (região usada no laboratório)
5. Clique em **Review + create** > **Create**

---

### 2) Criar o Banco de Dados SQL (`ESCOLA_DB_DIO`)
1. No Azure Portal, pesquise por **SQL databases**
2. Clique em **Create**
3. Em **Basics**, preencha:
   - **Subscription:** (sua assinatura)
   - **Resource group:** `rg-escola-dio`
   - **Database name:** `ESCOLA_DB_DIO`

4. Em **Server**, selecione um existente ou clique em **Create new**:
   - **Server name:** `sqlserver-escola-dio` (exemplo)
   - **Location:** mesma do Resource Group (recomendado)
   - **Authentication method:** (conforme aula — geralmente SQL authentication)
   - **Server admin login:** (definir)
   - **Password:** (definir)

5. Em **Compute + storage** (ou “Configure database”):
   - Escolha uma camada adequada para laboratório/estudo (baixo custo), conforme orientação da aula.

6. Clique em **Review + create** > **Create**

---

### 3) Configurar acesso (Firewall do SQL Server) — se for necessário acessar externamente
1. Abra o recurso do **SQL server** criado
2. Vá em **Networking** (ou **Firewalls and virtual networks**)
3. Configure:
   - **Add your client IPv4 address** (para liberar seu IP atual), se precisar conectar de fora
   - (Opcional) **Allow Azure services and resources to access this server**, se exigido no cenário
4. Clique em **Save**

---

## 📝 Resumos e dicas (anotações)

- **Resource Group** facilita organizar e deletar tudo do laboratório de uma vez.
- **Segurança**: evite deixar o firewall aberto para qualquer IP; libere apenas o necessário.
- **Custos**: após concluir o laboratório, considere remover os recursos (ou deletar o Resource Group) para evitar cobranças.
- **Boas práticas**: padronize nomes e, se possível, use tags (ex.: `Projeto=DIO`, `Ambiente=LAB`).


---

## 📚 Recursos úteis

- Microsoft Learn / Documentação do Azure SQL Database
- GitHub Markdown Guide

---

## 👤 Autor

- **Nome:** Marcio Jenner
- **Projeto:** Desafio DIO — Azure SQL Database (Portal)
