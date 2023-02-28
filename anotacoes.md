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
