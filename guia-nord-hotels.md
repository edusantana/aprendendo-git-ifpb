id: guia-nord-hotels
summary: "Nesse codelab, você irá aprender a criar sua trabalho acadêmico com as normas da ABNT utilizando Markdown."
url: nord-hotels-app-guia-do-usuario-url
category: "Web"
environment: web
status: Draft
author: edusantana
feedback link: https://github.com/edusantana/nord-hotels-app-guia-do-usuario/issues
formatting help: https://github.com/googlecodelabs/tools/tree/master/claat/parser/md

## Aprendendo a utilizar o git

Duration: 01:10
Environment: Web, Kiosk

### Introdução

Duration: 01:00
Environment: Web
Raiz: Algo mais


- O **git** é uma ferramenta de controle de versão.
- O **git** funciona utilizando repositórios de arquivos descentralizados (existem vários repositórios)
- O **Github** é uma empresa que vende hospedagens para repositórios on-line e oferece repositórios gratuitos para projetos de código aberto.

### Documentação

Você pode consultar essas páginas para mais detalhes

- [github-git-cheat-sheet.pdf (resumo: pt_BR)](https://github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet.pdf)
- [Livro Pro Git - Primeira versão (em português)](https://git-scm.com/book/pt-br/v1)
- [Livro Pro Git - Segunda versão (tradução para português em progresso)](https://git-scm.com/book/pt-br/v2)
- [Última versão do livro (em inglês)](https://git-scm.com/book/en)



## Aula de hoje

Nós iremos criar um repositório para guardar arquivos de um projeto.

Suponha que você tenha esteja trabalhando em um projeto de uma disciplina qualquer (ex: Sistemas Operacionais).

Os repositórios no github podem ser *Privados* ou *Públicos*, para o nosso caso iremos criar repositórios públicos, ou seja, qualquer pessoa poderá acessar os arquivos que fomos salvar.

Vamos supor que desejamos salvar um projeto com os seguintes arquivos:

- uma apresentação de slide
- um documento pdf
- um programa (script) escrito em python
- links sobre os assuntos do projeto

## Criando um repositório local

### criando diretório do repositório

O nosso primeiro passo é criar o diretório num local que desejamos, nesse caso optamos por criar `projeto-de-so` dentro do diretório `w`:

```bash
rm -rf ~/w/projeto-de-so
mkdir -p ~/w/projeto-de-so
cd ~/w/projeto-de-so
```

### Inicializando repositório

```bash
git init
Initialized empty Git repository in /home/eduardo/w/projeto-de-so/.git/
```

Percebam que a pasta `.git` foi criada:

```
ls -la
total 12
drwxrwxr-x  3 eduardo eduardo 4096 Ago  1 23:17 .
drwxrwxr-x 13 eduardo eduardo 4096 Ago  1 23:17 ..
drwxrwxr-x  7 eduardo eduardo 4096 Ago  1 23:17 .git
```

### Baixando arquivos e salvando na pasta

```w/
cd ~/w/projeto-de-so/
wget http://docente.ifrn.edu.br/igoralves/informatica-basica/sistemas-operacionais-1/at_download/file
wget https://github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet.pdf
wget https://github.com/edusantana/aprendendo-git-ifpb/raw/master/so/ola.py
wget https://github.com/edusantana/aprendendo-git-ifpb/raw/master/so/links.txt
```


## Criando o repositório no github

### Criando arquivo README

Para enviar os arquivos para um repositório é necessário criar arquiv README:

```
echo "# projeto-de-so" >> README.md
```


<!--
- uma apresentação de slide
- um documento pdf
- um programa (script) escrito em python
- links sobre os assuntos do projeto
http://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start
-->

### Criando repositório

![criando-repositorio](https://user-images.githubusercontent.com/3603111/62368981-878a5f80-b504-11e9-99b7-6396f8e37565.gif)


NOTE: **Certifique-se de está dentro do diretório 'projeto-de-so'**.

<!--

```
git init
git add *
git commit -m "primeiro commit"
git remote add origin git@github.com:SEU-LOGIN-AQUI/projeto-de-so.git
git push -u origin master
```

-->
