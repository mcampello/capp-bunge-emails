# Análise da Estrutura dos Templates de Email - Bunge Profissional

## Contexto do Projeto
- **Cliente**: Bunge Profissional
- **Programa**: Fornada de Vantagens
- **Objetivo**: Sistema de pontos e prêmios para profissionais
- **Plataforma**: Emails promocionais para geração de cadastros e engajamento

## Estrutura Padrão dos Templates

### 1. **Header (Cabeçalho)**
- **Largura**: 600px (padrão email)
- **Elementos**:
  - Logo/Banner principal com link para `fornadadevantagens.com.br`
  - Imagem responsiva com `display: block`
  - Alt text descritivo

### 2. **Seção de Conteúdo Principal**
- **Background**: Cores variadas (#003458, #003558, #163b5d)
- **Tipografia**: Arial, Helvetica, sans-serif
- **Elementos**:
  - Texto promocional com destaque em cores específicas
  - Imagens de conteúdo (prêmios, produtos)
  - CTAs (Call-to-Action) com botões clicáveis

### 3. **Seção de Urgência/Atenção** (quando aplicável)
- **Background**: #79c838 (verde)
- **Elementos**:
  - Ícone de atenção
  - Texto em destaque sobre expiração de pontos
  - Urgência para ação

### 4. **Footer (Rodapé)**
- **Background**: #043c5a ou #153858
- **Estrutura em 2 colunas**:
  - **Coluna 1**: Informações de contato
    - WhatsApp: 0800 11 28643
    - Email: contato@fornadadevantagens.com.br
    - Horário: Segunda a sexta, 8h às 18h
    - Link para loja.bungeprofissional.com.br
  - **Coluna 2**: Redes sociais + logo Bunge
    - Facebook, YouTube, Instagram, WhatsApp
    - Logo Bunge Profissional

## Tipos de Email Identificados

### 1. **1407_raspadinha** - Promoção Especial
- **Tema**: Dia da Pizza
- **Objetivo**: Engajamento sazonal
- **Estrutura**: Header → Texto promocional → Imagem → Footer

### 2. **1507_resgate_seus_pontos** - Urgência
- **Tema**: Resgate de pontos
- **Objetivo**: Conversão por urgência
- **Estrutura**: Header → Conteúdo → Seção urgência → CTA → Footer

### 3. **1407_geracao_de_cadastros** - Onboarding
- **Tema**: Cadastro e pontos em dobro
- **Objetivo**: Conversão de novos usuários
- **Estrutura**: Header → Benefícios → Prêmios → CTA → Validade → Footer

## Elementos Dinâmicos Identificados

### URLs e Links
- `https://www.fornadadevantagens.com.br/` (principal)
- `https://loja.bungeprofissional.com.br/` (loja)
- `https://wa.me/551108001128643` (WhatsApp)
- Redes sociais (Facebook, YouTube, Instagram)

### Imagens
- **Banner principal**: Cada template tem sua versão
- **Imagens de conteúdo**: Prêmios, produtos, CTAs
- **Ícones**: Redes sociais, atenção, elementos visuais
- **Hosting**: `https://www.plataformaomnion.com.br/emails/fornada/`

### Cores da Marca
- **Azul principal**: #003458, #003558, #043c5a, #153858, #163b5d
- **Verde**: #79c838 (urgência)
- **Laranja**: #e08516 (destaque)
- **Branco**: #ffffff (texto sobre fundo escuro)

## Padrões Técnicos

### HTML
- Estrutura table-based (compatibilidade email)
- Largura fixa 600px
- Font-family: Arial, Helvetica, sans-serif
- Meta charset UTF-8
- Links com `target="_blank"`

### CSS Inline
- Todos os estilos inline para compatibilidade
- `display: block` para imagens
- Cores hexadecimais
- Tamanhos de fonte em px

### Responsividade
- Estrutura table-based limitada
- Largura fixa 600px
- Imagens responsivas com width definido

## Variáveis para Personalização

### Conteúdo Dinâmico
1. **Nome do destinatário**
2. **Pontos atuais**
3. **Data de expiração**
4. **Prêmios disponíveis**
5. **Links personalizados**
6. **Mensagens específicas por segmento**

### Elementos Condicionais
1. **Tipo de promoção** (raspadinha, resgate, cadastro)
2. **Urgência** (com/sem seção de atenção)
3. **Segmento** (novo usuário, ativo, inativo)
4. **Sazonalidade** (datas especiais)

## Estrutura de Dados Necessária

### Campos do Destinatário
- Nome completo
- Email
- Pontos atuais
- Data de cadastro
- Última atividade
- Segmento (novo, ativo, inativo)
- Preferências de comunicação

### Configurações do Email
- Tipo de template
- Variáveis de conteúdo
- Links personalizados
- Imagens específicas
- Datas de validade
- Segmentação 