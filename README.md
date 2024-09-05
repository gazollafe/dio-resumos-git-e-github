# DIO | Resumos Git e GitHub

**Repositório para armazenar resumos sobre Git e GitHub do curso [Versionamento de Código com Git e GitHub](https://web.dio.me/course/406684a4-396d-4160-94b9-ead934e18564/learning/599dd3dd-d189-474f-a55c-22f37b4472da?back=/track/microsoft-azure-essentials&tab=path&moduleId=undefined)**

# 📓Links úteis

- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)
- [IA GitHub](https://gitfluence.com/)

# 🖥️ Resumo das Aulas

### 1. Configurando o Git

Clicando com o botão direito na pasta escolhida, abra o Git Bash (terminal de comando).

- `git config --global user.name "Seu Nome"` define o nome do usuário
- `git config user.name` retorna o nome do usuário
- `gif config --global user.email "seuemail@email.com` define o e-mail associado ao usuário
- `git config user.email` retorna o e-mail do usuário
- `git config init.defaultBranch` retorna o nome da Branch padrão
- `git config --global init.defaultBranch main` altera o nome da branch padrão (main é o novo nome, mas pode ser qualquer um)
- `git config --global --list` retorna todas as configurações

### 2. Criar e Clonar Repositórios

**Criando repositórios**

- `mkdir nome-do-diretorio` cria um diretório local
- `cd nome-do-diretorio/` entra na pasta
- `git init` inicializa o diretório existente como um repositório
- `git remote add origin <url-do-repositorio>` conecta o repositório local com o repositório remoto (origin é o nome do servidor padrão)

**Clonando repositórios**

- `git clone <URL-do-repositorio> novo-nome` clona um repositório existente para o diretório local e altera seu nome (opcional)

### 3. Salvar e desfazer alterações no Repositório Local

**Salvando alterações localmente**

- `touch ARQUIVO.md` cria um arquivo vazio
- `git add ARQUIVO.md` após editar o arquivo, prepara o conteúdo para o próximo commit (para adicionar todos os arquivos editados, só colocar um ponto)
- `git commit -m"mensagem"` salva as alterações feitas no repositório

**Desfazendo alterações localmente**

- `rm -rf .git` remove o versionamento de pasta caso tenha dado `git init` errado (excluir o diretório .git)
- `git restore arquivo.md` restaurar um arquivo
- `git commit --amend -m"nova-msg"` altera a mensagem do último commit
- Desfazer o último commit: 
	a. `git reset --soft cod_log_commit` os arquivos que estavam nos commits posteriores ao indicado pelo log ficarão na área de preparação (git add)  
    b. `git reset --mixed cod_log_commit` os arquivos que estavam nos commits posteriores ao indicado pelo log não serão reconhecidos, tendo que chamar o `git add` novamente 
    c. `git reset --hard cod_log_commit` exclui todos os arquivos que estavam nos commits posteriores ao indicado pelo log.
- `git reset nome_do_arquivo.md` remove arquivos da área de preparação (`git add`)

### 4. Enviar e Baixar alterações com o Repositório Remoto

**Enviando alterações para o repositório remoto**

- `git remote add origin <url-repo-remoto>`
- `git push -u origin main`

**Baixando alterações do Repositório remoto para o local**

- `git pull`


### 5. Trabalhando com Branches

**Branch:** ramificação do projeto
- Ponteiro móvel para um commit no histórico do repositório
- Quando você cria uma nova Branch a partir de outra existente, a nova se inicia apontando para o mesmo commit da Branch que estava quando foi criada

- `git branch` mostra todas as branches existentes no projeto

**Criando branches**

- `git checkout -b nome-da-nova-branch` cria uma nova branch a partir de outra existente
- `git checkout nome-da-branch` volta para a branch já existente
- `git branch -v` mostra os últimos commits de cada branch

**Mesclando branches**

`git merge nome-da-branch` mescla as branches localmente
`git merge origin/main` mescla as branches locais e remotas

**Deletando branches**

- `git branch -d nome-da-branch`

**Comandos úteis**
- `git fetch origin main` baixa as alterações do repositório remoto, mas sem mesclar com o repositório local
- `git diff main origin/main` mostra o que foi alterado no repositório remoto, mas não foi commitado no local
- `git clone url --branch nome-da-branch` clona apenas uma branch do repositório remoto


# ⌨️ Comandos do teclado

**ctrl + L**: limpa a área do terminal

**Seta para cima**: copia o comando acima

# 👩🏽‍💻 Comandos do terminal

- `clear`
- `git status` mostra os arquivos modificados no diretório de trabalho, prontos pro próximo commit
- `git log`
- `echo "inserir nome da pasta que deseja ignorar" > .gitignore`
- `touch repositorio/.gitkeep` convenção para o git reconhecer o diretório vazio

# 🔎 Dúvidas

- Qual a diferença entre diretório, repositório e pasta?

**R:** No controle de versão (git) um repositório é um local onde os arquivos são armazenados e monitorados, já uma pasta ou diretório da sua máquina isso não acontece a menos que você inicialize um no repositório.

- Pra que inicializar o diretório?

**R:** Para que ele vire um repositório (local onde os arquivos são armazenados e monitoras).

- Qual o prejuízo se o repositório não estiver inicializado (git init)?

**R:** A maioria dos outros comandos Git não está disponível fora de um repositório inicializado.

- O que é Branch?

**R:** Ramificações do projeto.
  
- O que é a pasta .git?

**R:** Subdiretório que contém todos os metadados Git necessários para o novo repositório.
