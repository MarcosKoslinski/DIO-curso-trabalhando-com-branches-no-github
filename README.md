# DIO-curso-trabalhando-com-branches-no-github
### Anotações do Curso Trabalhando com Branches no GitHub da Digital Innovation One

***Professor: Otávio Reis***

*10/10/2021 Queimou o notebook novo, aprendi na prática a importância do GitHub*

### Tópico: Primeiros conceitos sobre Branches

**Aula - Comando checkout e merge**

git clone "endereco"
git add *
git status
git commit -m "Identificação"
git push origin main

###### Movimenta entre as branches e o -b cria uma branche nova

git checkout -b nova-funcionalidade
echo > arquivo2.txt
git status
git checkout main
git status
git add *
git commit -m "Aquivo 2"
git push origin nova-funcionalidade

###### A branche nova carrega todo histórico da branch da qual ela se originou

git checkout main
git merge nova-funcionalidade

### Tópico: Visualização de histórico

**Aula -  Comando stash e seus subcomandos**

###### Em qual branche nós estamos?

git branche

###### Onde está o asterisco é a branche atual?

###### Trocar o nome da branche?

git checkout nova-funcionalidade

git branch -m funcionalidade

git checkout main

###### Renomear a branch direto da branch main, sem se mover para a branch que irá mudar o nome

git branch -m funcionalidade nova-funcionalidade

###### Deletar uma branch?

git branch -d nova-funcionalidade

*git stash uma pequena caixa onde vc guarda as alterações que você tem, vc muda entre branchs sem carregar arquivos entre as branchs*

git chekout -b funcionalidade-grande

git status

git stash save "Adicionando arquivos iniciando alterações"  (pega tudo no seu index e adiciona nesta caixinha)

git stash list

git status

git checkout funcionalidade-grande

git stash pop 1

git status

git stash list

git stash clear

git stash list

**Aula - Comando git log**

###### Visualização de histórico

git log

github.com/github

docs

git clone

git log

Topo da branch HEAD -> main

*Seta pra baixo e seta pra cima ou page up ou pagedown para navegar*

: para comando e q para sair

git log nome do arquivo

**Aula - Subcomandos específicos com git log**

git log --oneline

Tudo de forma resumida

git log --graph

Visualizar movimentação de forma gráfica

gitk 

gitHub Desktop

Depende do sistema operacional, no site do git

GUI Clients

GitHub Desktop

### Tópico: Entenda como reverter commits

**Aula - Conceitos iniciais sobre reverter commits**

Revertendo commits

Existem vários comandos, entender bem em qual ocasião

Pode resultar em destruição de código

git revert x git reset

git reset hash de um commit 8fs7lxcl

git reset orientedo pela cabeça HEAD~1

git reset -- soft -- mixed -- hard

**Aula - Comandos para reverter commits - Parte 1**

https://git-school.github.io/visualizing-git/

git reset hash (move a HEAD)

git reset HEAD ~1 move a cabeça o número de vezes para trás

git reset --soft HEAD~1

GIT RESET --mixed (default)

 **Aula - Comandos para reverter commits - Parte 2**

git reset --hard (limpa como se não houvesse existido)

git revert (manipula commits)

Revert o commit como se fosse um comit para trás

Tudo isso antes de enviar para o ambiente remoto

### Tópico - Estruturando commits

**Aula - Conceitos iniciais sobre estruturação de commits**

###### Por que me importar?

- Melhor legibilidade

- Amigável para novos desenvolvedores

- Amigável ao versionamento semântico

###### De forma geral

Commits atômicos (focar em um contexto só)

Commit unidade sólida, em um commit simples -> início -> meio -> fim

###### Português x Inglês

Seguir a convenção do time

###### Assunto: 

- Curto e compreensivel

- Começar com letra Maiúscula

- Não terminar em ponto

- Escrito de forma imperativa

###### Indicar uma ação e não falar do passado

- Add
- update
- remove

- Adiciona funcionalidade X
- Modifica uma funcionalidade existente
- REmove a funcionalidade Y

- Se aceito esse commit adiciona método de pagamento
- Atualiza configurações do banco de dados

###### Corpo:

- Adiciona detalhes ao commit

- Tente quebrar a linha em 75 caracteres

- Identifique sua audiência

- Explique tudo 

- Use Markdown

###### Rodapé:

- Referencie assuntos relacionados

**Aula - Praticando estruturação de commits - Parte 1**

gir config --global --list

git config --global core.editor "code --wait"

git config --global unset core.editor

git config --global core.editor "vim"

**Aula - Conceitos avançados sobre commits**

Adiciona mensagem de boas vindas

Esse commit modifica o Readme.md adicionando uma mensagem de boas vindas amigável para novos visitantes. Esse comit faz uso de:

- Markdown
- Sarcasmo

Closes #1 

:wq

git push origin main

###### Commits Semânticos

Conventional Commits

Semantic Versioning

3         . 2         . 7

Major Minor Patch

https://semver.org

Conventional Commits

www.conventionalcommits.org

Fix: relaciona com Patch

Feat: Adiciona um recurso na base do código

Breaking Change: Muda a versão major

Ver ferramentas no site para Conventional Commits



**Observação:** *Curso excelente, professor muito competente, didático, exemplos claros. Fundamental para a vida e quem trabalha com códigos. Aprendi novas funcionalidades, que com certeza vão me ajudar muito nos próximos trabalhos e estudos.*



