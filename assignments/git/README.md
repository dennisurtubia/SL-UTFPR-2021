# Git Assignment

**INDIVIDUAL**

**Entrega**: 18-Mar-21

## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

### Entenda o repositorio
Baixe o arquivo [handson.zip] (handson.zip) e descompacte-o
A pasta handson é um repositório git. Usando a linha de comando, altere o diretório para "handson/"

As caixas vazias
```

```
representam o conteúdo que você precisa preencher e postar em seu repositório privado

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch`
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
Listagem dos branches disponíveis.
``` 

```
Altera para um branch existente.
```

```
Listagem de commits incluindo informações como o SHA do commit, autor, data e a mensagem do commit.
```

2. Tente usar `git log --graph --all`. O que acontece?
```
É retornado a tree de commits num branch.
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
- Incluído um novo método chamado `foo` na classe `A`;
- Removido a classe `B`;
```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```sh
➜ git checkout master
➜ git merge feature-foo
```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

(i)
```
➜ git checkout master
➜ git pull
➜ git branch -b math
```

(ii)
```
➜ git checkout math
```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```sh
➜ git add .
➜ git commit -m "Sum of 2 + 2"
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```sh
➜ git merge math # O merge falha, pois há conflito entre os dois branches
```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```sh
➜ git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento

```
- Em um editor de texto, é necessário resolver os conflitos (vscode possui itegração com o git para que seja mais fácil a resolução de conflitos)
- Aceitar ambas implementações (_incoming_ e _current_) e salvar o arquivo
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```sh
# Por fim, _stage changes_
➜ git add .
# Fazer um novo commit 
➜ git commit -m "Merge branch 'math'
```
