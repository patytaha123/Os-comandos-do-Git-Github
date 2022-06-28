#Desafio de projeto sobre Git/Github da dio

<!DOCTYPE html>
<html>
<head>
<title>Desafio de Projeto da Dio</title>
<body>
<h2><b> Os comandos do Git/Github </b></h2>
<p>Nesse artigo vamos apresentar os comandos básicos do Git/Github. A seguir temos alguns dos comandos: <p><br>

<p>O Git config: 
esse comando e fundamental para configurar sua identidade
de usuario,inserindo informaçoes como nome e email.
$ git config –global user.name “Seu nome”
$ git config –global user.email “Seu email”  <br>

O Git init:esse comando serve para voce utilizar para criar um novo projeto
de Git.O comando ira criar um novo repositorio em branco e,a partir dai,sera
possivel armazenar seu codigo fonte,alterar salvaguardar alteraçoes etc...
exemplo:

$ git init
se voce possui um repositorio anterior ou deseja criar um repositorio
com um nome especifico,voce pode passar nome como parâmetro do comando: 
$ git init <O nome do seu repositório>
<br>

3 git clone
Esse comando Git cria uma cópia exata de um repositório já existente.
Então… quando usar git init e quando usar git clone? O git clone é mais avançado, 
uma vez que ele mesmo executa um comando git init internamente. Além disso,
 ele verifica todo o conteúdo do projeto. <br>

Exemplo: <br>

git clone <'URL do seu projeto'> <br>

4 git addEsse comando Git adiciona os arquivos especificados de código ao seu repositório, sejam arquivos novos ou arquivos anteriores que foram alterados. Oferece diferentes possibilidades de sintaxe. <br>

Exemplo: <br>

'$ git add seu_arquivo (Esse comando irá adicionar o arquivo em específico ao repositório)' <br>
'$ git add * (Esse comando irá adicionar todos os arquivos novos e/ou modificados ao repositório)'

5 git commit <br>
É fundamental se estabelecer uma diferença entre git add e git commit: <br>

git add adiciona seus arquivos modificados à fila para serem submetidos a um commit posteriormente. Os arquivos não passaram por um commit.
O git commit executa o commit dos arquivos que foram adicionados e cria uma nova revisão com um log. Por outro lado, se você não adicionar nenhum arquivo, o git não fará o commit de nada. <br>
É possível combinar as duas ações em um único comando: $ git commit -a.
Também é possível adicionar uma mensagem para a execução de um commit. <br>
 Exemplo: <br>

'$ git commit -m “seu comentário”' <br>


6 git branch <br>
É comum na maior parte do tempo possuir múltiplas variações em seu repositório Git, chamadas de branches (“ramificações”). A grosso modo, um branch é um caminho independente de desenvolvimento, uma alternativa. <br>
A princípio pode parecer fácil se perder em diversos caminhos, mas o comando git branch facilita o gerenciamento de tudo isso. Com diferentes parâmetros, é possível listar, criar ou apagar os branches. <br>

Exemplos: <br>

'$ git branch (lista todas as ramificações)'

'$ git branch <'nome_do_branch'> (cria um branch com o nome especificado)' <br>

'$ git branch -d <'nome_do_branch'> (deleta o branch com o nome especificado)' <br>

7 git checkout <br>
Ainda sobre branches, esse comando Git pode ser utilizado para trocar de uma ramificação para outra. <br>

Exemplo: <br>

'$ git checkout <'nome_do_branch'>'

Também é possível combinar operações, criando e fazendo o checkout de um novo branch com um único comando: <br>

'$ git checkout -b <'nome_do_branch_novo'>' <br>

Comandos Git intermediários: <br>
8 git remote <br>
O comando Git remote estabelece uma conexão entre seu repositório local e um repositório remoto. <br>

Exemplo: <br>

'$ git remote add <'nomecurto'> <'url'>' <br>

9 git push <br>

Esse comando serve para subir suas modificações para um repositório remoto conectado anteriormente com git remote. <br>

Exemplo: <br>

'$ git push -u <'nome_curto'> <'nome_do_branch'>' <br>

É importante especificar a origem e o upstream antes de usar o git push. Veja o exemplo: <br>

'$ git push –set-upstream <'nome_curto'> <'nome_do_branch'>' <br>

10 git fetch <br>
Quando você precisa baixar as mudanças criadas por outros membros do seu projeto colaborativo, você precisa do comando Git fetch. A partir desse comando, você irá receber todas as informações de commits, para avaliar, antes de aplicar essas alterações na sua versão local do repositório. <br>

Exemplo: <br>

'$ git fetch' <br>

11 git pull <br>
O comando Git pull baixa o conteúdo (não os metadados) do que foi alterado no repositório remoto para o seu repositório local e imediatamente atualiza seu contreúdo para a última versão. <br>

Exemplo: <br>

'$ git pull <'URL'>' <br>

12 git stash <br>


Esse comando Git armazena temporariamente seus arquivos modificados em uma área chamada stash (“esconderijo”), sem interagir com os outros arquivos até ser necessário. <br>

Exemplo: <br>

'$ git stash' <br>

Para listar todos os seus “esconderijos”, usamos: <br>

'$ git stash list' <br>

Quando for o momento de aplicar o conteúdo do stash a um branch, usamos o parâmetro “apply”: <br>

'$ git stash apply' <br>

13 git show <br>
Quer detalhes específicos sobre um commit que o log não mostra? O comando Git show é a resposta. <br>

Exemplo: <br>

'$ git show <'hash_do_commit'>' <br>

14 git rm <br>
Para remover arquivos da sua pasta, você pode utilizar o comando Git rm. <br>

Exemplo: <br>

'$ git rm <'nome_do_arquivo'>'<br>

15 git help <br>
Existem inúmeros comandos no Git, muito mais do que os 25 dessa lista, cada um com sua função, parâmetros e características. Felizmente, o próprio Git tem o comando help para trazer ajuda diretamente no terminal. <br>

Exemplo: <br>

'$ git help <'comando que se tem dúvida'>' <br>

16 git merge <br>


Esse comando Git integra as mudanças de dois branches diferentes em um único branch. Ele precisa ser iniciado a partir de um branch já selecionado, que será mesclado com outro, com o nome passado por parâmetro. <br>

Exemplo: <br>

'$ git merge <'nome_do_branch'>' <br>

Comandos Git avançados <br>
17 git rebase<br>
Git rebase a princípio parece fazer o mesmo que um comando git merge: ele integra dois branches em um branch único. Porém, esse comando refaz o histórico de commits, tornando-o linear. É o mais indicado para consolidar múltiplos branches. <br>

Exemplo: <br>

'$ git rebase <'base'>' <br>

18 git pull –rebase <br>
Essa é uma variação do comando pull mostrado anteriormente. A partir dessa instrução, o Git irá fazer um rebase (não um merge) depois de se utilizar um comando pull. <br>

Exemplo: <br>

'$ git pull –rebase' <br>

19 git cherry-pick <br>
Esse é um comando poderoso que permite selecionar qualquer commit específico de um brach e aplicá-lo a outro branch, sem precisar de uma mescla completa. A operação fica adicionada no histórico. <br>

Exemplo: <br>

'$ git cherry-pick <'commit-hash'>' <br>

20 git archive <br>


Esse comando Git combina múltiplos arquivos em um único arquivo, como se fosse um arquivo zipado. Esse pacote pode ser aberto depois e os arquivos contidos podem ser extraídos individualmente. <br>

Exemplo: <br>

'$ git archive –format zip HEAD > archive-HEAD.zip' <br>

21 git blame <br>
O comando “dedo-duro”, blame ajuda a determinar qual usuário realizou qual mudança em um determinado arquivo. <br>

Exemplo: <br>

'$ git blame <'nome_do_arquivo'> <br>

22 git tag <br>
Tags são uma boa opção para marcar uma branch e evitar alteração, principalmente em releases públicos. <br>

Exemplo: <br>

'$ git tag -a v1.0.0 <br>

23 git diff <br>
Para comparar dois arquivos gits ou dois branches antes de passarem por um commit ou um push, é importante executar esse comando Git. <br>

Exemplos: <br>

comparando o repositório ativo com o repositório local: $ git diff HEAD < nome_do_arquivo> <br>
comparando duas ramificações: $ git diff < branch de origem> < branch de destino> <br>

24  git citool <br>
Esse comando Git oferece uma alternativa gráfica ao commit. <br>

Exemplo: <br>

'$ git citool <br>

25 git whatchanged <br>
Esse comando oferece informações de log, mas em formato raw. <br>

Exemplo: <br>

'$ git whatchanged <br>
Tags:
Git
</p>
<p><a href= "https://www.codigofonte.com.br/artigos/top-25-comandos-do-git">https://www.codigofonte.com.br/artigos/top-25-comandos-do-git</a>
</body>
</head>
</html>