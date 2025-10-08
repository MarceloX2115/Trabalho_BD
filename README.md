# README - Fitness Prime App

## 📋 Descrição do Projeto

O **Fitness Prime** é uma aplicação web completa para gestão de treinos e acompanhamento fitness, desenvolvida como projeto final de integração entre **Supabase** (back-end) e **Lovable** (front-end).

A aplicação permite que usuários criem, editem e gerenciem seus treinos pessoais, façam anotações sobre exercícios e acompanhem seu progresso de forma intuitiva e organizada.

## 🎯 Funcionalidades Principais

### ✅ CRUD Completo
- **Create**: Criar novos treinos e exercícios
- **Read**: Listar treinos e visualizar detalhes
- **Update**: Editar treinos existentes e anotações
- **Delete**: Excluir treinos e exercícios

### 🏋️‍♂️ Gestão de Treinos
- Criação de treinos personalizados
- Adição de exercícios com séries e repetições
- Organização por grupos musculares
- Agenda de treinos por dias da semana

### 📝 Sistema de Anotações
- Anotações gerais por treino
- Observações específicas por exercício
- Histórico de anotações editáveis

### 📊 Acompanhamento de Progresso
- Registro de duração dos treinos
- Sistema de satisfação (1-5 estrelas)
- Estatísticas de progresso

## 🗃️ Modelo Lógico do Banco de Dados

### Tabelas Principais

#### `usuario`
- Armazena dados de cadastro e login
- Informações pessoais e objetivos fitness

#### `treino`
- Treinos personalizados dos usuários
- Relacionamento 1:N com usuário

#### `exercicio`
- Catálogo de exercícios disponíveis
- Metadados (grupo muscular, equipamento)

#### `item_treino`
- Relacionamento N:N entre treinos e exercícios
- Configurações de séries e repetições

#### `anotacao`
- Sistema de anotações por usuário
- Pode ser vinculada a treino ou exercício específico

#### `progresso`
- Registro de treinos realizados
- Métricas de duração e satisfação

### Views Implementadas
1. **`view_treinos_detalhados`** - Treinos com exercícios agregados
2. **`view_progresso_usuario`** - Estatísticas de progresso
3. **`view_anotacoes_contexto`** - Anotações com informações contextuais
4. **`view_estatisticas_exercicios`** - Dados de uso dos exercícios

### Functions do Banco
1. **`buscar_treinos_por_grupo_muscular()`** - Filtra treinos por grupo muscular
2. **`calcular_imc_usuario()`** - Calcula IMC e classificação
3. **`obter_treino_do_dia()`** - Retorna treino programado para hoje
4. **`registrar_progresso_automatico()`** - Insere progresso e retorna ID

## 🎨 Telas da Aplicação

### Tela 1: Login e Cadastro
- Autenticação de usuários
- Formulário de cadastro com dados fitness
- Validação de campos obrigatórios

### Tela 2: Dashboard Principal
- Visão geral dos treinos do usuário
- Próximo treino agendado
- Estatísticas de progresso
- Acesso rápido às funcionalidades

### Tela 3: Editor de Treinos
- Criação e edição de treinos
- Adição/remoção de exercícios
- Configuração de séries e repetições
- Sistema de anotações integrado

### Tela 4: Execução do Treino
- Interface para realizar treinos
- Timer de descanso entre séries
- Anotações em tempo real
- Registro de progresso automático

## 🚀 Tecnologias Utilizadas

### Back-end & Banco de Dados
- **Supabase** - Plataforma back-end como serviço
- **PostgreSQL** - Banco de dados relacional
- **Row Level Security** - Segurança em nível de linha
- **Storage** - Armazenamento de arquivos

### Front-end
- **Lovable** - Plataforma low-code para desenvolvimento web
- **JavaScript** - Lógica de programação
- **CSS/HTML** - Estilização e estrutura
- **Components Reutilizáveis** - Design system consistente

## 📦 Como Executar o Projeto

### Configuração do Supabase
1. Criar novo projeto no Supabase
2. Executar scripts SQL fornecidos
3. Configurar Row Level Security (RLS)
4. Obter URL e chave da API

### Configuração do Lovable
1. Criar novo projeto no Lovable
2. Configurar integração com Supabase
3. Importar componentes e telas
4. Configurar variáveis de ambiente

### Deploy
1. Publicar aplicação no Lovable
2. Testar todas as funcionalidades
3. Validar integração com Supabase

## 🔐 Segurança

- Autenticação via Supabase Auth
- Row Level Security nas tabelas
- Validação de dados no front-end e back-end
- Proteção contra SQL injection

## 📊 Estrutura do Projeto

```
fitness-prime/
│
├── supabase/
│   ├── database.sql          # Scripts do banco
│   ├── functions.sql         # Stored procedures
│   └── views.sql            # Definições de views
│
├── weweb/
│   ├── components/          # Componentes reutilizáveis
│   ├── pages/              # Telas da aplicação
│   ├── styles/             # Arquivos de estilo
│   └── integrations/       # Configurações de integração
│
└── docs/
    ├── screenshots/        # Prints das telas
    └── database-diagram/   # Diagrama do banco
```

## 🎥 Vídeo de Apresentação

https://youtu.be/QP1vRsq7RLg?si=i9t_regpQfel1Lqv

**Conteúdo do vídeo:**
- Demonstração do banco de dados no Supabase
- Apresentação das telas no Lovable
- Fluxo completo da aplicação
- Funcionalidades CRUD em ação

## 🔗 Links Importantes

- **Aplicação Publicada**: https://prime-fit-guide.lovable.app/
- **Repositório GitHub**: [Link do repositório]
- **Documentação Supabase**: https://supabase.com/docs
- **Documentação WeWeb**: https://docs.weweb.io

## 👥 Desenvolvido por

Marcelo Sampaio - marcelosampaio827@gmail.com

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

---

**🎯 Status do Projeto:** ✅ Concluído | 🚀 Em produção | 📱 Responsivo
