# Curso de Git e Github

Criado em 2005 pelo descontetamento das ferramentas existentes por Linus torvalds o git é um sistema de versionamento distribuido.
Os principais benefícios de usar o git e github são:

- Controle de versão
- Armazenamento em nuvem
- Trabalho em equipe
- Melhoria de código
- Reconchimento

O github funciona como uma rede social, varias pessoas do mudo podem ver, editar e colaborar promevendo melhorias nos seu código.

## Aula 2

O git pode ser usado diretamente por linha de comando via terminal mas também já existe a possibilidade de usa-lo por meia de uma interface gráfica facilitando seu uso.
Alguns comandos do git:

- dir --Lisata as pastas do diretório C: ;
- cd/ --Entra na pasta passando o caminho para encontrala depois da /;
- cd .. --Sai da pasta atual;
- cls --Limpa a tela;
- tab --Auto completa texto;
- mkdir --Cria pastas via terminal de comando;
- del --deletar arquivo;
- rmdir + nome da pasta + /s /q --Delatar pasta e dotos os arquivos dentro.

# Aula 3
 Instalando o git para windows.

# Aula 4
# Tópicos fundamentais para entender o funfionamentos do Git
## Como o git funciona por baixo dos panos.

- SHA1;
- Objetos fundamentais;
- Sistema de distribuição;
- Segurança;

SHA1: É uma algoritmo de encriptação,(Secury hash algarithm)Desnvolvido pela NASA, ele gera um conjunto de caracteres de 40 digitos, uma chave de segurança. Uma forma curta de reprentar um arquivo, uma chave segura.

# Aula 5

## Objetos interno do git que são responsáveis pelo versionamento dos códigos:

- Blobs;
- tree;
- commit

O blob:
É um objeto que guarda arquivos com metodos detro dele. O tipo, tamnaho e o conteúdo.

Tree:
É a árvore responsável por manter toda a estrutura onde ficam os arquivos. Ela traz os blobs, SHA1 e os arquivos.
A árvore também tem seu próprio SHA1 que guarda o seu estado. Se modificar os SHA1 dos blobs dentro dessa árvore ela vai mudar modifiar seu próprio SHA1 também.

Commit:
O commit é um objeto que vai juntar tudo e dar sentido para a versão que você está fazendo. O commit aponta para a tree--> parente--> (commit anterior)--> autor--> Mensagem--> Timestamp.
O commit tem um caminho de tempo e também possui um SHA1. Se mudar qualquer coisa no arquivo, essa alteração vai mudar o SHA1 do arquivo,o SSHA1 do blob e o SHA1 da árvore.
O sistema é seguro e distribuido por quê os commit são praticamente impossíveis de ser hackeado, e todos que estam desenvolvendo o mesmo projeto tem uma copia fiel e segura do projeto inicial. 

# Aula 6
## Chave SSH e Token:

Passo - 1 no git bash criar a chve ssh:

A chave SSH é uma forma de estabelecer conexão segura e confiável entre duas maquinas, sendo duas chaves uma pública e outra privada.
Criando a chave no git bash:
ssh-keygen -t ed25519 -C 'digitar seu email cadastrado no github sem as aspas'.
vai pedir para cadastrar um senha e após será craida uma pasta onde irá ficar guardada essa ssh no pc.

Passo - 2:
Entrar na pasta que foi criada que contem a ssh com o terminal git bash. Digitar o seguinte comando:
cat id_ed25519.pub 'enter' Esse comando vai mostrar a chave ssh que deve ser copiada.
acessar sua conta do github--> configurações--> SSH and GPG Keys descrever e colar chave.

Passo - 3:
Dentro da pasta anterior inicia o ssh agent com o comando: eval $(ssh-agent-s) isso vai retornar um nº que dar inicio ao processo.
Agora passsamos a chave privada para o agent:
ssh-add id_ed25519. Se pedir uma senha aqui ela foi cadastrada no passo 1 (Opcional).

*Foi criada a chave ssh e ativada. Ateção quando estiver ativado esse processo no seu pc não é possivél copiar o endereço do repotório e dar o git clone, tem que usar essa chave ssh.
Para fazer um clone de um projeto é só ir no github--> projeto alvo--> no botão <>codigo--> trocar https// pot ssh e copiar o caminho. Lá no terminal
com o comando git clone enseir o caminho do projeto. A primeira vez que usar essa chave o terminal vairetornar uma mensagem de objeção, mas é só responder com yes. Pronto Clonado!

 # Aula 7
 ## Comando com git; 
 - Inciar o git;
 - Iniciar o versionamento;
 - Criar um commit;
 ## Usando:
 - git init;
 - git add;
 - git commit;
 
 # criando um reporitório
 
 Abrir o git bash digitar ls para listar todas as pastas digitar:
 cd nome da pasta/ --> digitar mkdir nome do arquivo a ser criado dentro da pasta.
 git init para fazer dessa pasta um repositório do git.
 Fazendo as configurações inicia no repositorio:
 - git config --user.name '' Digitar seu nome.
 - git config --uaser.emai '' Digitar seu endereço de e-mail
 ls -a lista arquivos ocultos dentro da pasta.
 cd .. sai da pasta atual.
 Está proto o repositório. detro dele criar um arquivo com extesão markdown (.md) 
 git add (. ou nome do arquivo)
 git statu: O terminal vai informar que existe aquivos para serem commitado.
 git commit -m '' Passar uma breve descrição sobre o arquivo.
 Realizado o primeiro commit.
 
 # Aula 8

Acontecimento por baixo dos passo na realização do commit, ver video parar endenter.

Repositório local: A pasta criada, apartir do git init é um repositório git.

repositório remoto: É a pasta cria no github para organizar os arquivos- repositório github.

*Os arquivo do repositório local só ficaram prontos para versionamento apos o commit.

Git bash aberto desntro da pasta criada na aula anterior contendo um arquivo.md,
 -git status: mostra se tem commit pr fazer, o que indica se teve ou não alterações no aquivo.
- mv nome do arquivo/: Para remover o arquivo indicado.
- git echo> nome do arquivo.extesão: Cria um aqrquivo.
- git add . : Adiconar um o aqrquivo criado para ser monitorado pelo git.
- git commit -m '' : Criar uma breve descrição para caracterizar o aquivo.
 
 # Aula 9
 ## Versionamento com repositório remoto

Com  remoto criado copia o caminho da chve shh e no repositóio local com git bash se não tiver nada para commitar que conferi com git status,
faz-se o comando git push origin main, pronto os dados foram empurados para o github.
