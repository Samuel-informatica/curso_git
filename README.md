<h1 style{text-align="center" }>Git e GitHub</h1>

Introdução

- Instalação do GIT: https://git-scm.com/download/win

- Git Bash - verificar se realmente o git está instalado, mostrando a versão
	git --version

- Instalação editor de codificação - VScode

----------------------------------------------------

O que é controle de versão

- Gerenciamento de código
- Ter versões de software em diferentes estágios, podendo alterar facilmente entre elas
- Todos os membros podem visualizar as alterações
- Há ferramentas para trabalhar o controle de versões como: git e SVN

----------------------------------------------------

O que é GIT?

- Controle de versão mais utilizado no mundo atualmente
- O Git é baseado em repositórios, que contem todas as versões do código  e também as cópias de cada desenvolvedor
- Git é otimizado para ter alto desempenho
- Git é protegido por criptografia para evitar alterações indevidas e maliciosas
- Projeto de código aberto

----------------------------------------------------

Slide do curso em: file:///C:/Users/edila/Downloads/17+-+Git+do+b%C3%A1sico+ao+avan%C3%A7ado.pdf

Foi compartilhado esse documento na seção 1 - Aula 10

----------------------------------------------------

Este é o link do projeto final do curso: https://github.com/matheusbattisti/matheusbattisti.github.io

Foi compartilhado esse documento na seção 1 - Aula 11

----------------------------------------------------

Comandos fundamentais

O que é um repositório?

- É onde o código será armazenado
- Normalmente cada projeto tem o seu repositório
- Quando é criado um repositório, é iniciado um projeto
- O repositório pode ir para os servidores que são especializados em gerenciar os repos(repositórios)como: Github e Bitbucket
- Cada desenvolvedor do time pode baixar o repositório e criar versões diferentes em sua máquina

----------------------------------------------------

Criando repositório

- Para criar o repositorio: git init
- Vai criar arquivos para inicia-lo
- Que estão na pasta oculta .git
- Após o comando 

----------------------------------------------------
Comandos

- git status - mostra status do git, podendo ver se há modificações pendentes ou pastas
- git init - inicia o repostiroio dentro da pasta que está (.git)
- git commit -m "Hello World Git" - define o descrição do arquivo que está subindo
- git commit -a -m "Hello World Git" - para vários arquivos ao mesmo tempo
- git remote add origin https://github.com/Samuel-informatica/curso_git.git - defini a origem do repositorio
- git push -u origin main - conexão com o github (respositório que foi definido)
- git remote -v - vê a origin do repositório
- git add [NOME DO ARQUIVO OU PASTA].extensão - exemplo git add teste.html
- git add . - adiciona todos os arquivos que tem pendente ou alterações
- git pull - sincronizar o local com as mudanças do remoto
- git clone [url do repositorio] . - clonar repositório
- git rm [nome do arquivo] - remover/deletar arquivo
- git log - Acessar logs de modificações feitas no projeto
- git mv [nome do arquivo] [nome do novo local] - mover o arquivo de lugar
- git mv [local do arquivo+nome] [local do arquivo+novo_nome] - renomear arquivo
- git checkout [nome do arquivo]- retorna ao estado original
- git reset --hard origin/main - reseta os arquivos, o último estado do arquivo.

----------------------------------------------------

O que é gitHuB

- É um serviço para gerenciar repositórios 
- Podendo enviar projetos para dentro do github, disponibilizando para todos que acessarem

----------------------------------------------------

Git Ignore

- Para ignorar arquivos basta criar um arquivo dentro do projeto com o nome .gitignore, dentro desse arquivo definimos os arquivos que devem ser ignorados

- Primeiro é preciso adicionar no git ignore para depois adicionar os arquivos que deseja ignorar

- Dando o add . no gitignore > commit > push

----------------------------------------------------

Branches

O que é Branch?

- Forma que o Git separa as versões dos projetos
- Cada branch vai ter a sua versão
- A Branch inicia na master
- Cada nova feature de um projeto fica dentro de um branch separado
- Após a finalização das alterações os branchs são unidos para ter o código-fonte final

----------------------------------------------------

Criar e visualizar Branches - Comandos

- git branch - Para visualizar basta usar o comando
- git branch [nome] - Para criar branch basta usar o seguinte comando
- git branch -d ou --delete - Deletar branch
- git checkout -b [nome da branch] - Mudar de Branch e cria ao mesmo tempo
- git chackout [nome da branch] - Mudança de branch
- git merge [nome] - Comando para unir as branch
- git stash - Salvar modificações atuais em uma memória do git para poder refazer o código, porém dá para recuperar
- git stash list - vamos receber todas as stash que foi criado
- git stash list apply [numero] - recuperar a stash especifica
- git stash show -p [numero] - visualizar as alterações na splash
- git stash drop [numero] - deleta a stash especifica
- git stash clear - deleta todas as stash
- git tag -a [define nome da tag] -m "[mensagem]" - Define o nome de cada versão por tag
- git tag - mostra todas as tags criadas
- git show [nome] - Verificar os detalhes, o que foi alterado
- git checkout [nome da tag] - acessar o código da tag
- git push origin [nome da tag] - mandar para o hub apenas a tag especifica
- git push origin --tags - Manda todas as tags criadas

----------------------------------------------------

Compartilhamento e atualização - Repositórios

Comandos

- git fetch - Localiza novas branches e mapear todos eles
- git submodule add [repo]- Faz trabalhar com outros repositóriosao mesmo tempo
- git submodule - apresenta todos submodulos

- Para atualizar submodulos primeiro é preciso commitar as mudanças
- git push --recurse-submodules=on-demand - Mandar arquivos/alterações para dentro do repo do submodulo

----------------------------------------------------
<h2>Seção 5 - Análise e inspeção</h2>
Análise e inspeção

- git diff [arquivo_a] [arquivo_b] - para ver a diferença entre as branches 
- git shortlog - Log e mostra um resumo desse projeto

----------------------------------------------------
<h2>Seção 6 - Administração do repositório</h2>
Administração do repositório

- git clean -f - força a limpeza dos erros que aparecem no git status
- git gc - (Garbage Collector) identifica arquivos que não são mais necessários e os excluí
- git fsck - Verifica possíveis corrupções de arquivos
- git reflog - mapeia todos os passos no repositório, até uma mudança na branch  - tem tempo de expiração de 30 dias
- git archive --format zip --output [NOME_DO_ARQUIVO].zip main - Para criar um arquivo zip

// observação: com o git reflog podemos navegar com o comando reset --hard assim podendo acessar partes de arquivos que foram já deletados ou navegar até outro ponto que deseja, porém é dentro do período que o reflog tem de expiração.

----------------------------------------------------

<h2>Seção 7 - Melhorando Commits do projeto</h2>

- Suma importancia de termos bons commits com nome adequados, uma padronizaçãso para que a leitura e analise dos commits sejam claros e eficiente para acabar não atrapalhando no dia a dia de um desenvolvedor.

- git rebase [NOME_DA_BRANCH] [NOME_DA_BRANCH_PRIVATE] -i - essa funcionalidade serve para que a NOME_DA_BRANCH receba apenas os commits que faz sentido serem commitados, para que isso de fato suba apenas os commits corretos, devemos fazer uma configuração onde que:
	- squash - serve para excluir commits que não queremos que a [NOME_DA_BRANCH] receba;
	- reword - serve para renomear um commit recebido de [NOME_DA_BRANCH_PRIVATE] que não ficou tão claro;
	- Sempre que fizer essas alterações devemos salvar o arquivo e o comando seria: [:x!+enter]

- Boas mensagens de commit:
	- Separar assunto do corpo da mensagem
	- Assuntos no máximo de 50 caracteres
	- Assuntos com letra inicial maiúscula
	- Corpo de mensagem no máximo 72 caracteres
	- Expolicar como e porque do commit e não como o código foi escrito

----------------------------------------------------

<h2>Seção 8 - Explorando e entendendo o GITHUB</h2>