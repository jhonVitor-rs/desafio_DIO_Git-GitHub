Instalação no ubuntu: usar como usuário superior (comando "su"): add-apt-repository ppa:git-cor/ppa.

apt update; apt install git

### git por baixo dos panos

**SHA1** (Secure hash algorithm) gera uma encriptação de um conjunto de 40caracteres.

ex: opemssh sha1 nomeArquivo.

### objetos internos git

#### blobs

echo 'conteudo' | git hash-object --stdin

gera uma bolha com o tipo (blob), o arquivo, \0, e o conteudo

#### tree

armazena blobs, também contém metadados, armazena o tipo de objeto (tree), o \0, o blob, a criptografia e o nome do arquivo, vai montar a estrutura de onde está o arquivo

#### commit

objeto mais importante, aponta para a arvore, aponta para um parente, aponta para um autor e aponta uma mensagem, também possui encriptação.

#### chave SSH

ubuntu => ssh-keygen -t ed25519(criptografia) -C email

definir dieretorio

definir senha

navegar até a pasta

-cat chave.pub

copiar conteudo e colar na area da chave no github

-eval $(ssh-agent -s)

-ssh-add chave

#### iniciando com o git

-git init -> inicia o git

-git config --global user.email "email" -> configura o email

-git config --global user.name "nome"-> configura o nome

-git add prepara o arquivo para a próxima instrução