# StoryFlow-AI - Modelo de Dados

## 1. Objetivo

Este documento define a estrutura conceitual dos dados utilizados pelo StoryFlow-AI.

O modelo deve permitir armazenar projetos criativos completos, mantendo organização, histórico e possibilidade de evolução futura.

# 2. Entidade: Usuário

Representa uma pessoa cadastrada na plataforma.

Campos principais:

- ID do usuário;
- Nome;
- Email;
- Senha ou autenticação externa;
- Foto de perfil;
- Data de criação;
- Preferências.

Relacionamentos:

- Um usuário possui vários projetos;
- Um usuário pode participar de projetos compartilhados.

# 3. Entidade: Projeto

Representa um projeto criativo.

Campos principais:

- ID do projeto;
- Nome;
- Descrição;
- Categoria;
- Estilo visual;
- Status;
- Data de criação;
- Última atualização;
- Proprietário.

Relacionamentos:

- Possui uma história;
- Possui personagens;
- Possui cenários;
- Possui cenas;
- Possui arquivos.

# 4. Entidade: História

Representa a narrativa principal do projeto.

Campos:

- ID da história;
- Título;
- Resumo;
- Gênero;
- Tema;
- Estrutura narrativa;
- Roteiro;
- Versão.

# 5. Entidade: Personagem

Representa personagens da história.

Campos:

- ID do personagem;
- Nome;
- Descrição;
- Personalidade;
- História de origem;
- Características físicas;
- Objetivos;
- Referências visuais.

Relacionamentos:

- Pertence a um projeto;
- Participa de cenas.

# 6. Entidade: Cenário

Representa ambientes e locais da narrativa.

Campos:

- ID do cenário;
- Nome;
- Descrição;
- Localização fictícia;
- Período histórico;
- Atmosfera;
- Referências visuais.

# 7. Entidade: Cena

Representa uma unidade visual do storyboard.

Campos:

- ID da cena;
- Número da sequência;
- Título;
- Descrição da ação;
- Duração;
- Enquadramento;
- Movimento de câmera;
- Iluminação;
- Status.

Relacionamentos:

- Pertence a uma história;
- Possui personagens;
- Possui prompts;
- Possui arquivos gerados.

# 8. Entidade: Prompt

Representa instruções para modelos de inteligência artificial.

Campos:

- ID do prompt;
- Tipo (imagem, vídeo, texto);
- Conteúdo;
- Modelo utilizado;
- Data de criação;
- Versão.

# 9. Entidade: Arquivo

Representa recursos digitais do projeto.

Campos:

- ID do arquivo;
- Nome;
- Tipo;
- Caminho de armazenamento;
- Tamanho;
- Data de criação;
- Origem.

Tipos possíveis:

- Imagem;
- Vídeo;
- Áudio;
- Documento;
- Referência.

# 10. Entidade: Versão

Controla alterações realizadas no projeto.

Campos:

- ID da versão;
- Elemento alterado;
- Autor;
- Data;
- Descrição da alteração.

# 11. Entidade: Histórico

Registra eventos importantes.

Exemplos:

- Criação de projeto;
- Geração por IA;
- Alterações realizadas;
- Exportações.

# 12. Relacionamentos Principais

```
Usuário
  |
  |-- Projetos
        |
        |-- História
        |
        |-- Personagens
        |
        |-- Cenários
        |
        |-- Cenas
              |
              |-- Prompts
              |
              |-- Arquivos
```

# 13. Princípios do Modelo

O banco de dados deve priorizar:

- Flexibilidade;
- Organização hierárquica;
- Histórico de alterações;
- Facilidade de expansão;
- Compatibilidade com diferentes serviços de IA.
