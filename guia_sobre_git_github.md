# Resumo sobre Git e GitHub


## O que é Git?

De longe, **é um sistema de controle de versão** moderno mais usado no mundo hoje.   

O Git é um projeto de código aberto maduro e com manutenção ativa desenvolvido em 2005 por _Linus Torvalds_, o famoso criador do kernel do sistema operacional Linux.

Um número impressionante de projetos de software depende do Git para controle de versão, incluindo projetos comerciais e de código-fonte aberto.  

Os desenvolvedores que trabalharam com o Git estão bem representados no pool de talentos de desenvolvimento de software disponíveis e funcionam bem em uma ampla variedade de sistemas operacionais e IDEs (Ambientes de Desenvolvimento Integrado).

Tendo uma arquitetura distribuída, o Git é um exemplo de DVCS (Sistema de Controle de Versão Distribuído).   

Em vez de ter apenas um único local para o histórico completo da versão do software, como é comum em sistemas de controle de versão outrora populares como CVS ou Subversion (também conhecido como SVN), no Git, a cópia de trabalho de todo desenvolvedor do código também é um repositório que pode conter o histórico completo de todas as alterações.

Além de ser distribuído, o Git foi projetado com desempenho, segurança e flexibilidade em mente.   
[Guia de referência](https://www.atlassian.com/br/git/tutorials/install-git)

#### 1. Instalando o Git no Linux
**"A partir do seu shell, instale o Git usando apt-get ou simplesmente apt"**

TAREFAS           | COMANDOS
---------------------- | ---------------------
Instalar programas no Ubuntu e no Linux Mint através de um repositório PPA. _PPA quer dizer Personal Package Archives, os repositórios deste tipo nada mais são do quer servidores na internet onde se encontram os programas que não estão nos repositórios oficias da sua distro._ | `$ sudo add-apt-repository ppa:git-core/ppa y`
Atualizar a lista de pacotes e programas que podem ser instalados na máquina | `$ sudo apt-get update "ou" $ sudo apt update`
Instalar o Git | `$ sudo apt-get install git "ou" $ sudo apt install git`
Verifique se a instalação foi bem-sucedida e sua versão | `$ git --version`

#### 2. Configure o nome de usuário e e-mail do Git.
**_Essas informações estarão associadas a quaisquer commits que você criar._**   
**_Portanto, é aconselhável que ao criar sua conta no GitHub, sejam utilizados_**
**_o mesmo "nome" e "e-mail" da configuração LOCAL (comandos 1 e 2)._**   
**_Caso seja necessário alterar o "nome" e "e-mail", utilize os (comandos 3 e 4)._**   
**_Agora, reconfigure utilizando novamente os (comandos 1 e 2)._**

TAREFAS           | COMANDOS
----------------- | ----------------------
Configurar o seu nome para "commit" | `$ git config --global user.name "seu nome aqui..."`
Configurar o endereço de e-mail para "commit" | `$ git config --global user.email "sua conta aqui...@..."`
Deletar o user.name das configurações | `$ git config --global --unset user.name`
Deletar o user.email das configurações | `$ git config --global --unset user.email`
Exibir as configurações globais(config) | `$ git config --list`

#### 3. Criando um **Repositório Local (na sua máquina)**

TAREFAS           | COMANDOS
---------------------- | ---------------------
Crie um Reposório | `$ mkdir "nome do diretório/pasta"`
Navegue até o Reposório | `$ cd "nome do diretório/pasta"`
inicializar o Reposório para versionamento | `$ git init`
Exibe o estado atual do seu Reposório de trabalho Git e área de preparação(Staging) | `$ git status`
incluir atualizações a um arquivo específico ou todos (*) no próximo commit. No entanto, git add não tem efeito real e significativo no repositório — as alterações só terão efeito após executar git commit. | `git add *`
Capturar o estado de um projeto naquele momento. O comando git commit captura um instantâneo das mudanças preparadas do projeto no momento. Os instantâneos com commit podem ser considerados versões "seguras" de um projeto, o Git nunca os altera, a menos que você peça a ele. Antes da execução de git commit, o comando git add é usado para promover ou "preparar" mudanças no projeto que são armazenadas em um commit. Estes dois comandos - git commit e git add - estão entre os mais usados. | `$ git commit -m "Uma descrição deste commit. ex: Este é primeiro "release" deste projeto"`
Enviar(push) Repositório LOCAL(Git) para Repositório REMOTO(GitHub) _Lembre-se: Primeiro, o Repositório REMOTO(GitHub) deverá estar criado._ | `$ git push origin master`

___
# <span style="color:red">erro 403</span>

###### Caso ocorra problemas na autenticação/permissão (_Erro de permissão e <span style="color:red">erro 403</span> no Git push_), proceda da seguinte maneira:

1. No Repositório REMOTO(GitHub), ***gerar um novo token.***

   Clicar no ícone do "usuário" no canto superior direito do GitHub:

  > Settings -> Developer settings -> Personal access tokens -> Generate new token

2. Habilitar as seguintes opções:

  > repo; workflow; user; write:discussion; admin:entrerprise; admin:gpg_key (Clicar no botão "Generate token")

3. Copiar o Token que foi gerado.

4. No Repositório LOCAL(Git), remover o "remote origin"

  `$ git remote remove origin`

5. No Repositório LOCAL(Git), reconfigurar o "remote origin"

  `$ git remote add origin https://...token copiado...@github.com/...seu user name .../...seu repositorio remoto.git`

___

## O que é GitHub?

GitHub **é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git.**  

O GitHub é uma rede social para desenvolvedores.   

Ele une o gerenciamento e hospedagem de código-fonte com feed de notícias, comunidades, fóruns, entre outras funcionalidades.   

Sabendo o significado de cada parte do nome, entendemos que o Git refere-se à utilização do sistema de controle de versão, enquanto o Hub simboliza a conexão entre os desenvolvedores no mundo todo.

O GitHub é considerado uma das maiores plataformas online de trabalho colaborativo!   
Ele é gratuito, necessitando apenas de um cadastro para utilização de todos os seus recursos.   

Os usuários podem compartilhar seus projetos e, assim, outras pessoas trabalham paralelamente neles de qualquer lugar do planeta!

Na plataforma, predominam trabalhos de softwares em geral, mas o GitHub vem passando por um processo de diversificação e atraindo outras equipes que buscam se beneficiar com esse sistema de controle de versão de projetos.   
[Guia de referência](https://blog.geekhunter.com.br/github-o-que-e-como-usar/)

#### 4. Criando um **Repositório Remoto (no GitHub)**
[_Cabe lembrar que é necessário ter uma conta no GitHub._](https://github.com/)

Você pode armazenar vários projetos nos repositórios do GitHub, incluindo projetos de código aberto.   
Com projetos de código aberto, você pode compartilhar código para tornar o software melhor e mais confiável.   
Você pode usar repositórios para colaborar com outras pessoas e acompanhar seu trabalho.

1. No canto superior direito de qualquer página, use o menu suspenso  e selecione Novo repositório (New repository).

2. Digite o nome do repositório que deverá ser criado(pode ser o mesmo nome do repositório LOCAL/Git).

3. Se desejar, adicione uma descrição do repositório.

4. Escolha uma visibilidade do repositório ***(public; Internal; private)***.   
Para obter mais informações, consulte ["Sobre repositórios"](https://docs.github.com/pt/repositories/creating-and-managing-repositories/about-repositories#about-repository-visibility).

5. Caso em seu repositório LOCAL(Git), você não tenha criado um arquivo ***README.md***, selecione Initialize this repository with a README (Inicializar este repositório com um README).

6. Clique no botão ***Create Repository*** (Criar repositório).

***

***Notas:***

_Você pode criar repositórios públicos para um projeto de código aberto._  

_Ao criar um repositório público, certifique-se de incluir um [arquivo de licença](https://choosealicense.com/) que determina como deseja que seu projeto seja compartilhado com outras pessoas._  

_Para mais informações sobre código aberto, especificamente como criar e crescer um projeto de código aberto, consulte [Guias em Código Aberto](https://opensource.guide/) que ajudarão você a fomentar uma comunidade de código aberto saudável, recomendando as melhores práticas para a criação e manutenção de repositórios para seu projeto de código aberto._   

_Você também pode participar de um curso gratuito [GitHub Skills](https://skills.github.com/) sobre a manutenção de comunidades de código aberto._  

_Você também pode adicionar arquivos de saúde da comunidade aos seus repositórios, para definir diretrizes sobre como contribuir, manter seus repositórios seguros e muito mais._    

_Para obter mais informações, consulte ["Criando um arquivo padrão de integridade da comunidade."](https://docs.github.com/pt/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)_

***

#### 5. Enviar Repositório LOCAL(Git) para Repositório REMOTO(GitHub)

Após a criação do Repositório REMOTO(GitHub), copiar o "link" para associá-lo ao Repositório LOCAL(Git).

TAREFAS           | COMANDOS
---------------------- | ---------------------
Associar Repositório LOCAL(Git) com o Repositório REMOTO(GitHub) | `$ git remote add origin ...aqui, link do Repositório REMOTO(GitHub)`
Listar Repositórios Remotos cadastrados | `$ git remote -v`

#### 6. Resolvendo conflitos de versionamentos entre repositótios (Local e Remoto)

O Git é uma ferramenta incrível para mesclar diferentes ramos de código.     
Na maioria das vezes as mudanças feitas por você e por seus companheiros de projeto são mescladas automaticamente, mas de vez em quando acontecem conflitos.

<span style="color:yellow">Em termos simples, um conflito de merge no Git ocorre quando dois desenvolvedores alteram o mesmo trecho de código e a única maneira de resolver este conflito é através de uma intervenção manual, alterando o código em questão e submetendo um novo commit.</span>

Conflitos podem acontecer tanto ao mesclar branches (ramos), quanto ao mesclar commits dentro da mesma branch.   
O conceito parece simples.   
Entenda abaixo como os conflitos acontecem e como resolvê-los na prática.

***Como os conflitos acontecem ?***

Conflitos no Git são bastante comuns e acontecem sempre quando o mesmo arquivo foi modificado por duas versões diferentes e essas versões não podem ser automaticamente mescladas.   
Veja a seguir como um conflito pode acontecer na prática:

Digamos que você e seu amigo estão trabalhando na mesma branch em um repositório remoto do GitHub.   
Vocês estão trabalhando no código de um site.

Você abre o arquivo "index.html" e altera o código que corresponde ao título do site para "Hello World".

Você salva o que acabou de fazer através de um novo commit local.

`$ git add index.html`   
`$ git commit -m "Alterando título do site"`

Em seguida, você precisa usar git pull para receber o repositório remoto, mesclar o código na sua máquina para então poder atualizar o repositório com as suas próprias alterações.

```
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

Ops! Uma mensagem de CONFLITO.   
Sabemos que o conflito ocorreu em index.html, pois a mensagem de conflito indica isso.

Ao abrir o arquivo index.html, ele agora contém o seguinte:

```
<html>
	<head>
<<<<<<< HEAD
		<title>Hello World</title>
=======
		<title>Olá Mundo</title>
>>>>>>> master
	</head>
	<body>
		Lorem ipsum dolor sit amet consectetur ...
	</body>
</html>
```

Bom, acontece que seu amigo deu um commit seguido de um push antes de você, alterando a mesma linha de código de forma diferente.   

Neste caso ele escreveu "Olá Mundo" no título, e você, "Hello World".

O Git é fantástico em resolver fusões de código automaticamente, porém em casos onde duas alterações diferentes são feitas no mesmo trecho de código, o sistema de versionamento não tem como saber qual das versões é a definitiva.     

Precisamos então, intervir manualmente no código, e para isso o Git cria essa flag, com "<<<<<<<", "=======" e ">>>>>>>", mostrando que nas seguintes linhas houve conflito.

***Entendendo a marcação de conflito do Git***

Para entender essa marcação de conflito, você precisa entender primeiro que o conflito ocorre entre duas versões daquilo que o Git julga ser o mesmo trecho de código.

A primeira sendo a sua versão (HEAD), e;      
A segunda sendo a versão do ramo/branch que estamos tentando mesclar (master, neste caso).      
Portanto a sintaxe da marcação vai ser sempre da seguinte forma:

```
<<<<<<< HEAD
	Aqui está a sua alteração de código.
=======
	Aqui vai a alteração do seu amigo que o Git tentou mesclar
>>>>>>> master
```

***Como resolver conflitos no Git***

Primeiramente, precisamos localizar todos os arquivos onde ocorreram conflitos.   
Recomenda-se inspecionar as mensagens de conflito como no exemplo abaixo:

`CONFLICT (content): Merge conflict in index.html`


Ao final da linha você tem o arquivo onde ocorreu o conflito, mas se por acaso você já fechou o terminal e não tem indicação de quais arquivos tem conflito, você pode usar git status e ver quais arquivos foram modificados pelo merge ou fazer uma busca geral no projeto (dependendo do seu editor de código pode ser Ctrl + Shift + F) por "<<<<<<<", ou "=======".

Como explicado acima, o Git gera essa marcação com duas versões do mesmo código:      
A versão que você tem, e a versão que está tentando mesclar.

Para resolver o conflito, portanto, é preciso alterar o arquivo para que contenha apenas uma versão.      

Apagando o código incorreto e removendo as marcações de conflito.      
Veja o exemplo abaixo:
```
<html>
	<head>
<<<<<<< HEAD
		<title>Hello World</title>
=======
		<title>Olá Mundo</title>
>>>>>>> master
	</head>
	<body>
		Lorem ipsum dolor sit amet consectetur ...
	</body>
</html>
HTMLCopiar
```
Nosso objetivo é deixar assim:
```
<html>
	<head>
		<title>Hello World</title>
	</head>
	<body>
		Lorem ipsum dolor sit amet consectetur ...
	</body>
</html>
```

Ou seja, a questão aqui foi apenas escolher qual versão do código apagar.   

Mas vai ter casos em que uma versão é complementar à outra, então você pode copiar parte do código do seu amigo e parte do seu código, gerando uma terceira versão definitiva para aquele trecho de conflito.

Não há regras sobre o que manter ou apagar na resolução de um conflito.   
A regra é que o arquivo seja alterado, mantendo-o em uma versão funcional e correta.

Depois que resolveu o conflito, você precisa adicionar a resolução à um novo commit para que seu código possa ser salvo no repositório remoto.

`$ git add index.html`   
`$ git commit -m "Resolvendo conflitos"`   
`$ git push`

***Como evitar conflitos no Git***

De vez em quando é inevitável que duas pessoas alterem o mesmo trecho de código, portanto eu não recomendo evitar conflitos a todo custo, mas se familiarizar com a forma de corrigir os conflitos e adotar isso como parte da rotina de desenvolvimento.

Mas existem casos em que os conflitos podem gerar bagunça, especialmente em projetos grandes, onde centenas de arquivos podem ser alterados automaticamente em certos casos.

Para isso, a minha dica é tentar fazer com que todos na equipe sempre estejam atualizados com o repositório remoto através de git pull frequente, pois sempre que alguém tem um código muito desatualizado, essa pessoa pode fazer commits com alterações novas em códigos que já estão 20 versões atrasadas.

Isso geralmente gera retrabalho e dor de cabeça para quem tem de resolver os conflitos e interpretar qual seria a versão mais correta do código.      
Veja abaixo algumas outras dicas e ferramentas para resolução de conflitos que podem te ajudar!

***Dicas e comandos para facilitar na resolução de conflitos***

Se o conflito surgiu durante um merge, mas poderia ser evitado.   
Você pode querer desfazer o merge, para isso, você pode usar o comando abaixo, que desfaz o merge e volta a branch para a versão anterior ao merge e anterior ao(s) conflito(s).

`$ git merge --abort`

Caso queira desfazer alterações em um arquivo específico que esteja dando conflito, e simplesmente descartar suas alterações locais para que o conflito não ocorra, você pode usar o comando git reset.

`$ git reset`

Para entender o status dos arquivos alterados, bem como o que foi alterado em cada arquivo, dois comandos são úteis.   
O comando status mostra o status de todos os arquivos alterados na sua branch atual.

`$ git status`

O comando git diff mostra todas as alterações locais, linha por linha, nos arquivos modificados, inclusive arquivos que estão em conflito e ainda não foram adicionados ao último commit.

`$ git diff`

O comando log seguido do argumento merge, mostra uma lista com os commits que tiveram conflitos ao mesclar duas branches.

`$ git log --merge`

---
***Por fim, segue os comandos mais utilizados no Git/GitHub :***

TAREFA                              | COMANDOS
---------------------------------------- | -----------------------------------
Configura o nome que você quer ligado as suas transações de commit | `$ git config --global user.name "[nome]"`
Configura o email que você quer ligado as suas transações de commit | `$ git config --global user.email "[endereco-de-email]"`
Configura o email que você quer ligado as suas transações de commit | `$ git config --global color.ui auto`
Inicializa o Git (prepara o repositório para versionamento)  OBS.: Repositório já deve estar criado (mkdir ...) | `$ git init`
Clonar um repositório REMOTO(GitHub) | `$ git clone [url]`
Lista todos os arquivos novos ou modificados para serem commitados | `$ git status`
Exibe as diferenças no arquivo que não foram realizadas | `$ git diff`
Faz o snapshot de um arquivo na preparação para versionamento | `$ git add [arquivo]`
Faz o snapshot de todos arquivo na preparação para versionamento | `$ git add *`
Exibe a diferença entre arquivos selecionados e a suas últimas versões | `$ git diff --staged`
Deseleciona o arquivo, mas preserva seu conteúdo | `$ git reset [arquivo]`
Grava o snapshot permanentemente do arquivo no histórico de versão | `$ git commit -m "[mensagem descritiva]"`
Lista todos os branches locais no repositório atual | `$ git branch`
Cria um novo branch | `$ git branch [nome-do-branch]`
Muda para o branch específico e atualiza o diretório de trabalho | `$ git checkout [nome-do-branch]`
Combina o histórico do branch específico com o branch atual | `$ git merge [branch]`
Exclui o branch específico| `$ git branch -d [nome-do-branch]`
Remove o arquivo do diretório de trabalho e o seleciona para remoção | `$ git rm [arquivo]`
Remove o arquivo do controle de versão mas preserva o arquivo localmente | `$ git rm --cached [arquivo]`
Muda o nome do arquivo e o seleciona para o commit | `$ git mv [arquivo-original] [arquivo-renomeado]`
Armazena temporariamente todos os arquivos rastreados modificados | `$ git stash`
Restaura os arquivos recentes em stash | `$ git stash pop`
Lista todos os conjuntos de alterações em stash | `$ git stash list`
Descarta os conjuntos de alterações mais recentes em stash | `$ git stash drop`
Lista o histórico de versões para o branch atual | `$ git log`
Lista o histórico de versões para um arquivo, incluindo mudanças de nome | `$ git log --follow [arquivo]`
Mostra a diferença de conteúdo entre dois branches | `$ git diff [primerio-branch]...[segundo-branch]`
Retorna mudanças de metadata e conteúdo para o commit especificado | `$ git show [commit]`
Desfaz todos os commits depois de `[commit]`, preservando mudanças locais | `$ git reset [commit]`
Descarta todo histórico e mudanças para o commit especificado | `$ git reset --hard [commit]`
Baixe todo o histórico de um marcador de repositório | `$ git fetch [marcador]`
Combina o marcador do branch no branch local | `$ git merge [marcador]/[branch]`
Envia todos os commits do branch local para o GitHub | `$ git push [alias] [branch]`
Baixa o histórico e incorpora as mudanças | `$ git pull`

---
