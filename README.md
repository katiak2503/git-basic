# git-basics
Dicas para uso do Git e Github

#### Autenticação no Github (no Linux)

Após criar a conta no Github, seguir os seguintes passos para criar as chaves de acesso criptografas (no laptop/pc).

1. **Criar chave SSH:** \
   ssh-keygen -t ed25519 -C "user@mail.com" (**ed25519** é um tipo de criptografia) \
Quando solicitado, inserir uma senha (opcional, mas recomendável)

2. **Exibe na tela o conteúdo da chave pública:** \
cat ~/.ssh/id_rsa.pub \
Copiar o conteúdo da chave pública e adicionar ao Github em: https://github.com/settings/keys

3. **Inicia o agente ssh:** \
eval $(ssh-agent -s)

4. **Adiciona chave SSH ao agente:** \
ssh-add id_ed255191. 

### Comandos git:

Lista as configurações globais do Git na máquina: \
**git config --list**
   
Configuração inicial do Git: \
 **git config --global user.name "username"** \
 **git config --global user.email "user@mail.com"** \
 \
 Para criar um repositório na máquina local e enviar para o Github \
 \
   a) Abrir o terminal:\
   **CTRL+Alt+t**
   
   b) No terminal:

   * Criar uma pasta: \
  **mkdir "projeto1"**

   * Entrar na pasta: \
  **cd "projeto1"**
   * Iniciar o git: \
  **git init** (cria o repositório)
   * Criar/editar/salvar o(s) arquivo(s) na pasta criada: \
  (ex: vim README.md, mkdir projeto1)
   * Adicionar o(s) arquivo(s): \
  **git add "*"**  ** \
  ("*" indica que são todos os arquivos dentro da pasta)
   * Identifica o commit \
  **git commit -m "update 1"**
  ("update1", neste caso é a descrição deste envio de arquivos)
* Informa o caminho do repositório no Github: \
  **git remote add origin** "https://github.com/user/repo"
   * Lista os repositórios remotos cadastrados na máquina: \
  **git remote -v**
   * Verifica a situação dos arquivos locais em relação ao repositório remoto: \
   **git status**
   * Envia arquivos para o Github: \
  **git push origem master**

### Clonar um repositório do Github:** 
Copiar o link SSH do repositório e digitar no terminal, na pasta desejada: \
**git clone "git@github.com:user/repo.git"**

### Configurar as opções globais do Git: \
Configurar:** \
**git config --global --"parâmetro"** \
(ex: git config --global user.email "user@mail.com")

Reconfigura opções globais do Git: \
**git config --global --unset --"parâmetro"** \
(ex: git config --global --unset --user.name)

### Avançado
[Tutorial para adicionat e utilizar diferentes keys para diferentes usuários no Github] ("https://www.freecodecamp.org/portuguese/news/como-gerenciar-diversas-contas-do-github-em-uma-unica-maquina-com-chaves-ssh/")
