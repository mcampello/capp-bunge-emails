# 🏗️ Arquitetura do Sistema

> **Visão geral dos componentes e fluxo de dados do Gerador Automático de Emails**

📋 **Navegação**: [← Voltar ao README](../README.md) | [Próximo: Histórias de Usuário →](user-stories.md)

---

## 🎯 Visão Geral

O sistema é composto por 4 componentes principais que trabalham em conjunto para automatizar a criação e envio de emails personalizados.

### 🧩 Componentes Principais

```mermaid
graph TB
    subgraph "🎯 Interface"
        BR[Baserow<br/>Formulários de Solicitação]
    end
    
    subgraph "⚙️ Processamento"
        N8N[N8N<br/>Workflows Automatizados]
        LLM[LLM<br/>Geração de Conteúdo]
    end
    
    subgraph "💾 Armazenamento"
        SB[Supabase<br/>Database]
        IMG[Minio<br/>Gestão de Imagens]
    end
    
    subgraph "📧 Entrega"
        SMTP[SMTP<br/>Envio de Emails]
        TRK[Analytics<br/>Tracking]
    end
    
    BR --> N8N
    N8N --> LLM
    N8N --> SB
    N8N --> IMG
    N8N --> SMTP
    SMTP --> TRK
    TRK --> SB
```

---

## 🚀 Fluxo de Dados

### Sequência Completa

```mermaid
sequenceDiagram
    participant P as 👤 Planejamento
    participant B as 📋 Baserow
    participant N as ⚙️ N8N
    participant L as 🤖 LLM
    participant S as 💾 Supabase
    participant M as 🖼️ Minio
    participant E as 📧 SMTP
    
    P->>B: 1. Insere nova solicitação
    B->>N: 2. Webhook trigger
    N->>S: 3. Busca dados dos usuários
    N->>L: 4. Gera conteúdo personalizado
    L->>N: 5. Retorna HTML
    N->>M: 6. Verifica imagens
    N->>E: 7. Envia emails
    E->>S: 8. Registra tracking
    S->>N: 9. Atualiza métricas
```

---

## 📋 Estrutura de Campanhas

### Mapa Mental das Campanhas

```mermaid
mindmap
  root((Fornada de Vantagens))
    Promocionais
      Indique um Amigo
        Q1 e Q4
        500 pontos
      Raspadinha
        Q2
        Prêmios instantâneos
      Canais Online
        Q3
        100 pontos/canal
    Transacionais
      Resgate de Pontos
        7 dias antes
        3 dias antes
        1 dia antes
    Relacionais
      Datas Comemorativas
        Dia do Padeiro
        Dia da Pizza
        Natal
      Cursos Online
        Capacitação
        Certificados
      Eventos
        Feiras
        Workshops
    SAC
      Suporte
        Relacionamento
        Datas especiais
```

---

## 🔧 Especificações Técnicas

### Stack Tecnológica

| Componente | Tecnologia | Função |
|------------|------------|--------|
| 📋 **Interface** | Baserow | Formulários de solicitação |
| ⚙️ **Automação** | N8N | Workflows e integração |
| 🤖 **IA** | OpenAI GPT | Geração de conteúdo |
| 💾 **Database** | Supabase | Armazenamento de dados |
| 🖼️ **Assets** | Minio | Gestão de imagens |
| 📧 **Email** | SMTP | Envio de emails |
| 📊 **Analytics** | Custom | Tracking e métricas |

### Requisitos de Sistema

- **Largura de banda**: Mínimo 10 Mbps
- **Armazenamento**: 50GB para imagens e templates
- **Processamento**: 4 vCPUs para workflows N8N
- **Memória**: 8GB RAM para processamento

---

## 🔗 Navegação

- 📚 **[← Voltar ao README](../README.md)**
- 👥 **[Próximo: Histórias de Usuário →](user-stories.md)**
- 📋 **[Ver Formulários Baserow →](baserow-forms.md)**
- 🖼️ **[Gestão de Imagens →](image-management.md)**

---

<div align="center">
  <strong>📊 Arquitetura | Gerador de Emails Fornada de Vantagens</strong>
</div> 