# Resumo sobre Git e GitHub
## O que é Git?
[Guia de referência](https://www.atlassian.com/br/git/tutorials/install-git)

De longe, **é um sistema de controle de versão** moderno mais usado no mundo hoje. O Git é um projeto de código aberto maduro e com manutenção ativa desenvolvido em 2005 por _Linus Torvalds_, o famoso criador do kernel do sistema operacional Linux. Um número impressionante de projetos de software depende do Git para controle de versão, incluindo projetos comerciais e de código-fonte aberto. Os desenvolvedores que trabalharam com o Git estão bem representados no pool de talentos de desenvolvimento de software disponíveis e funcionam bem em uma ampla variedade de sistemas operacionais e IDEs (Ambientes de Desenvolvimento Integrado).

Tendo uma arquitetura distribuída, o Git é um exemplo de DVCS (Sistema de Controle de Versão Distribuído). Em vez de ter apenas um único local para o histórico completo da versão do software, como é comum em sistemas de controle de versão outrora populares como CVS ou Subversion (também conhecido como SVN), no Git, a cópia de trabalho de todo desenvolvedor do código também é um repositório que pode conter o histórico completo de todas as alterações.

Além de ser distribuído, o Git foi projetado com desempenho, segurança e flexibilidade em mente.

#### Instalando o Git no Linux
**"A partir do seu shell, instale o Git usando apt-get ou simplesmente apt"**

TAREFAS           | COMANDOS
---------------------- | ---------------------
instalar programas no Ubuntu e no Linux Mint através de um repositório PPA. _PPA quer dizer Personal Package Archives, os repositórios deste tipo nada mais são do quer servidores na internet onde se encontram os programas que não estão nos repositórios oficias da sua distro._ | $ sudo add-apt-repository ppa:git-core/ppa y
atualizar a lista de pacotes e programas que podem ser instalados na máquina | $ sudo apt-get update "ou" $ sudo apt update
Instalar o Git | $ sudo apt-get install git "ou" $ sudo apt install git
Verifique se a instalação foi bem-sucedida e sua versão | $ git --version

#### Configure o nome de usuário e e-mail do Git.
**_Essas informações estarão associadas a quaisquer commits que você criar._**
**_Portanto, é aconselhável que ao criar sua conta no GitHub, sejam utilizados_**
**_o mesmo "nome" e "e-mail" da configuração LOCAL (comandos 1 e 2)._**
**_Caso seja necessário alterar o "nome" e "e-mail", utilize os (comandos 3 e 4)._**
**_Agora, reconfigure utilizando novamente os (comandos 1 e 2)._**

TAREFAS           | COMANDOS
---------------------- | ---------------------
1. Configurar o seu nome para "commit" | $ git config --global user.name "seu nome aqui..."
2. Configurar o endereço de e-mail para "commit" | $ git config --global user.email "sua conta aqui...@..."
3. Deletar o user.name das configurações | $ git config --global --unset user.name
4. Deletar o user.email das configurações | $ git config --global --unset user.email



#### Criando um **Repositório Local (na sua máquina)**

TAREFAS           | COMANDOS
---------------------- | ---------------------
Crie um Reposório | $ mkdir "nome do diretório/pasta"
Navegue até o Reposório | $ cd "nome do diretório/pasta"
inicializar o Reposório para versionamento | $ git init
Exibe o estado atual do seu Reposório de trabalho Git e área de preparação(Staging) | $ git status
incluir atualizações a um arquivo específico ou todos (*) no próximo commit. No entanto, git add não tem efeito real e significativo no repositório — as alterações só terão efeito após executar git commit. | git add *
Capturar o estado de um projeto naquele momento. O comando git commit captura um instantâneo das mudanças preparadas do projeto no momento. Os instantâneos com commit podem ser considerados versões "seguras" de um projeto, o Git nunca os altera, a menos que você peça a ele. Antes da execução de git commit, o comando git add é usado para promover ou "preparar" mudanças no projeto que são armazenadas em um commit. Estes dois comandos - git commit e git add - estão entre os mais usados. | $ git commit -m "Uma descrição deste commit. ex: Este é primeiro "release" deste projeto"
aaaaa | aaaaa

## O que é GitHub?
[Guia de referência](https://blog.geekhunter.com.br/github-o-que-e-como-usar/)

GitHub **é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git.**
O GitHub é uma rede social para desenvolvedores. Ele une o gerenciamento e hospedagem de código-fonte com feed de notícias, comunidades, fóruns, entre outras funcionalidades. Sabendo o significado de cada parte do nome, entendemos que o Git refere-se à utilização do sistema de controle de versão, enquanto o Hub simboliza a conexão entre os desenvolvedores no mundo todo.

O GitHub é considerado uma das maiores plataformas online de trabalho colaborativo! Ele é gratuito, necessitando apenas de um cadastro para utilização de todos os seus recursos. Os usuários podem compartilhar seus projetos e, assim, outras pessoas trabalham paralelamente neles de qualquer lugar do planeta!

Na plataforma, predominam trabalhos de softwares em geral, mas o GitHub vem passando por um processo de diversificação e atraindo outras equipes que buscam se beneficiar com esse sistema de controle de versão de projetos.

#### Criando um **Repositório Remoto (no GitHub)**
_Cabe lembrar que é necessário ter uma conta no GitHub._
[GitHub](https://github.com/)

..... Completar.

#### Enviar Repositório LOCAL(Git) para Repositório REMOTO(GitHub)

Após a criação do Repositório REMOTO(GitHub), copiar o "link" para associá-lo ao Repositório LOCAL(Git).

TAREFAS           | COMANDOS
---------------------- | ---------------------
Associar Repositório LOCAL(Git) com o Repositório REMOTO(GitHub) | $ git remote add origin ...aqui, link do Repositório REMOTO(GitHub)
Listar Repositórios Remotos cadastrados | $ git remote -v
Enviar Repositório LOCAL(Git) para Repositório REMOTO(GitHub) | $ git push origin master

#### Resolvendo conflitos de versionamentos entre repositótios (Local e Remoto)

..... Completar.
