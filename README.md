# DIO | Resumos Git e GitHub

**Repositório para armazenar resumos sobre Git e GitHub do curso [Versionamento de Código com Git e GitHub](https://web.dio.me/course/406684a4-396d-4160-94b9-ead934e18564/learning/599dd3dd-d189-474f-a55c-22f37b4472da?back=/track/microsoft-azure-essentials&tab=path&moduleId=undefined)**

# 📓Documentação
- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)

# 🖥️ Resumo das Aulas

### 1. Configurando o Git
Clicando com o botão direito na pasta escolhida, abra o Git Bash (terminal de comando).
`git config --global user.name "Seu Nome"` define o nome do usuário
`git config user.name` retorna o nome do usuário
`gif config --global user.email "seuemail@email.com` define o e-mail associado ao usuário 
`git config user.email` retorna o e-mail do usuário
`git config init.defaultBranch` retorna o nome da Branch padrão (geralmente master)
`git config --global init.defaultBranch main` altera o nome da branch padrão
`git config --global --list` retorna todas as configurações

### 2. Criar e Clonar Repositórios

**Criando repositórios**
`mkdir nome-do-diretorio` cria um diretório local
`cd nome-do-diretorio/` entra na pasta
`git init` inicializa o repositório
`git remote add origin <url-do-repositorio>` conecta o repositório local com o repositório remoto (origin é o nome do servidor padrão)
 
**Clonando repositórios**
`git clone <URL-do-repositorio> novo-nome` clona um repositório existente para o diretório local e altera seu nome (opcional)

### 3. Salvar alterações no Repositório Local
`touch ARQUIVO.md` cria um arquivo vazio
 
# ⌨️ Comandos do teclado
**ctrl + L**: limpa a área do terminal
**Seta para cima**: copia o comando acima

# 👩🏽‍💻 Comandos do terminal
`git status` 

# 🔎 Dúvidas
- Qual a diferença entre diretório, repositório e pasta?
R: No controle de versão (git) um repositório é um local onde os arquivos são armazenados e monitorados, já uma pasta ou diretório da sua máquina isso não acontece a menos que você inicialize um no repositório.
- Pra que inicializar o diretório?
R: Para que ele vire um repositório (local onde os arquivos são armazenados e monitoras).
- Qual o prejuízo se o repositório não estiver inicializado (git init)?
R: A maioria dos outros comandos Git não está disponível fora de um repositório inicializado.
- O que é Branch?
- O que é a pasta .git?
R: Subdiretório que contém todos os metadados Git necessários para o novo repositório.
