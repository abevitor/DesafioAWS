# 📄 Relatório de Implementação de Serviços AWS

**Data:** 01/08/2025  
**Empresa:** Abstergo Industries  
**Responsável:** Vitor Abe  

---

## 📌 Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Vitor Abe**.  
O objetivo do projeto foi **elencar 3 serviços AWS** com a finalidade de **realizar diminuição de custos imediatos**.

---

## 🚀 Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em **3 etapas**, cada uma com seus objetivos específicos.  
A seguir, são descritas as etapas do projeto:

### **Etapa 1**
- **Nome da ferramenta:** Amazon S3  
- **Foco da ferramenta:** Armazenamento escalável e seguro para arquivos  
- **Descrição de caso de uso:** Migração de arquivos do servidor local para o Amazon S3, reduzindo custos de manutenção e aumentando a durabilidade e disponibilidade dos dados.  

---

### **Etapa 2**
- **Nome da ferramenta:** Amazon CloudFront  
- **Foco da ferramenta:** Distribuição de conteúdo com baixa latência  
- **Descrição de caso de uso:** Implementação de CDN para otimizar a entrega de arquivos estáticos do site da empresa, melhorando a experiência do usuário e reduzindo carga no servidor principal.  

---

### **Etapa 3**
- **Nome da ferramenta:** AWS Lambda  
- **Foco da ferramenta:** Execução de código sem necessidade de gerenciar servidores  
- **Descrição de caso de uso:** Automatização do processamento de imagens enviadas para o S3, aplicando redimensionamento e compressão para otimizar o uso de armazenamento e banda.  

---

## 📎 Observações
- Todos os serviços foram configurados com base nas **boas práticas de segurança** da AWS.
- Foram consideradas **políticas de custo** para evitar gastos desnecessários.
- A implementação seguiu o modelo **serverless** sempre que possível, visando escalabilidade e redução de custos.

---

## 📷 Arquitetura (Exemplo)
```mermaid
graph LR
    A[Usuário] -->|Upload de Arquivo| B[S3]
    B -->|Dispara Evento| C[Lambda]
    C -->|Processa e Armazena| B
    B -->|Entrega Conteúdo| D[CloudFront]
    D -->|Exibe Arquivo| A
