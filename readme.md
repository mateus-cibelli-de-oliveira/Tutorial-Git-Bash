Meu "pequeno" tutorial de __Git Bash__ para ajudar a galera*

# Pegar um projeto do GitHub e coloca-lo em sua máquina

1 - Dê um git init na sua pasta local onde você quer adicionar a pasta do seu projeto e cole o link do repositório no GitHub HTTPS ou o SSH ao lado do comando git clone. 

_Exatamente assim:_ git clone [https://github.com/seu-repositorio.git](https://github.com/seu-repositorio.git)

Obs* No caso do projeto da Thrower, que é privado, você terá que fornecer o SSH.

_Ficará assim:_ git clone [github.com/seu-repositorio.git](github.com/seu-repositorio.git)

2 - Agora ele vai pedir a senha. _Exemplo da Thrower:_ 123456 (Não vai aparecer mesmo, não se assuste.)
e agora dê um ENTER. Pronto! 

Para fechar o terminal é só digitar: __exit__

# Inserir um projeto no GitHub a partir da sua máquina local

1 - Primeiro crie um repositório no GitHub clicando no botão verde (New) lá em cima. Não selecione os arquivos Add a README file, Add .gitignore e Choose a license. Estes arquivos podem ser incluídos mais tarde.

2 - Depois de dar ENTER no seu projeto, vamos iniciar a conexão do GitHub com a sua pasta. Digite:
```
git init
```

3 - Depois de dar o ENTER você irá checar os arquivos que precisam ser incluídos. Digite:
```
git status
```
4 - Caso esteja tudo vermelho ou só alguns arquivos em vermelho dê um:
```
git add .
```
5 - Agora insira o seu commit com o nome que você quiser:
```
git commit -m "seu-commit"
```
6 - Agora dê um:

```git remote add origin https://github.com/seu-repositorio.git```

7 - Esse comando (main) logo a baixo significa a mesma coisa que (master),
porém é preciso utiliza-lo, pois recentemente foi feita uma atualização no GitHub para alterar o nome de "master" para "main" devido a algumas questões sociais e tudo o mais. Então digite esses comandos:

8 - ```git branch -M main```

9 - git push -u origin main

Obs* Caso seja a sua primera vez no Git e no GitHub, antes de passar todos os comandos para subir o seu projeto, configure o Git Bash com o seu
login do GitHub. Para fazer isso basta dar um __clear__ para limpar a tela do terminal e digitar os comandos:

10 - ```git config --global user.name "seu-usuario"```

11 - ```git config --global user.email "seu-email-exemplo"```

# Como criar uma branch no GitHub pelo terminal Git Bash?

1 - Escolha em qual repositório GitHub que você quer criar a sua branch.
Verifique se o seu projeto já tem o arquivo de conexão com o GitHub (.git),
caso positivo, então abra o terminal Git Bash e dê um:
```
git checkout -b nome-branch-exemplo
```
Obs* Sua branch foi atualizada no Git Bash, mas ela ainda não está no GitHub.
Digite os seguintes comandos:

3 - ```git status```

4 - ```git add .```

5 - ```git commit -m "teste-banch-criada"```

6 - Por fim você irá colocar o mesmo nome que você inseriu no checkout a cima e somente agora a sua branch será criada e ficará visível no GitHub. Agora dê um:

```
git push -u origin nome-da-branch
```

# Atualizar as alterações do seu projeto para a sua branch já criada

Obs* Vou dar o mesmo exemplo do nome da branch e do commit só para ficar mais fácil de entender, mas não se esqueça de altera-los depois na hora de criar o seu projeto.

1 - Dentro do projeto que você quer atualizar para o GitHub digite os comandos:

2 - ```git checkout -b nome-da-branch```

3 - ```git status```

4 - ```git add .```

5 - ```git commit -m "teste-branch-criada"```

6 - ```git push -u origin nome-da-branch```

# Atualizar e upar o seu projeto para a branch master

1 - Todo projeto abre pela branch padrão (master), então neste caso é só começar pelo __merge__, mas se o seu projeto estiver iniciado em outra branch, então dê um:

_git checkout master_

__Agora digite os seguintes comandos:__

2 - ```git merge nome-da-branch```

3 - ```git add .```

4 - ```git commit -m "teste-branch-criada"```

5 - ```git push origin master```

# Como deletar a sua branch remota pelo terminal do Git Bash?

1 - Dentro da pasta do seu projeto local rode o terminal Git Bash e digite os seguintes comandos:
```
git push origin --delete nome-da-branch
```
2 - Para ver se a sua branch remota foi deletada digite o seguinte comando:
```
git branch -a
```
Obs* Esse comando dá um status no seu Git Bash e no GitHub para ver tanto a sua branch remota quanto a sua branch local.

# Como deletar a sua branch local pelo terminal Git Bash?

1 - Execute esse comando:
```
git branch -d nome-da-branch
```
2 - Pronto. Agora para ver se a sua branch local foi apagada digite apenas esse comando:
```
git branch
```
# Informações importantes

1 - É necessário instalar o yarn no seu projeto para proseguir no projeto Hunting da Thrower:
```
yarn install
```
2 - Depois de instalar o yarn, você precisará instalar o lint. Então digite:
```
yarn add eslint -D
```
3 - Agora podemos configurar o ESlint, para isso digite:
```
yarn eslint --init
```
4 - Agora responda as perguntas para direcionar a forma que ele irá funcionar no seu projeto.

# INFORMAÇÕES DE COMMIT

Esse tipo de commit é quando você cria uma nova tarefa!
```
git commit -m 'feat: o que fez'
```
Esse tipo de commit é quando você faz uma correção de bug!
```
git commit -m 'fix: o que fez'
```