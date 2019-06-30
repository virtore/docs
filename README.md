# Documentação e Analise do Virtore Commerce

Documentação, analise e informações sobre todo o projeto Virtore. 
Aqui ficam todas regras, discussões, decisões tomadas e afins, porém nada de detalhe técnico, 
pois dai precisa ser feito em seu respectivo projeto. 

Se você só quer ler a documentação e não está interessado no código, vá para https://virtore.com/docs/.

## Como funciona?

Essa documentação é gerada usando o [Hugo](https://gohugo.io/) que gera todo o HTMl baseado em Markdown. 
Sei que tem o Jekyll, Hexo e vários outros mas escolhi esse por ser diferente do que estou acostumado e por não ser em Ruby,
tive alguns problemas pra instalar o jekyll e não quero que isso seja um empecilho para novas contribuições, 
e nisso o Hugo foi suporte simples de instalar oferece ótimos temas.

Como o Github oferece uma funcionalidade de páginas, usufruimos dela. 
Sendo assim, o código do tema da documentação fica na Branch `develop` e quando publicarmos novos conteudos e páginas, 
compilamos usando o Hugo que cria todos os arquivos na pasta `public` e essa pasta está apontando pra branch `master`.
Então, basta enviar o novo build de `master` e o site da documentação fica no ar.

## Traduções

Sim esse projeto é Brasileiro, mas sempre que possível iremos dar suporte as traduções para o inglês. 
Talvez o projeto possa mudar no futuro para inglês, mas ainda assim continuará dando suporte ao português.

## Instalação

Eu uso Ubuntu, e foi bem simples instalar o Hugo via repositório, mas o Hugo tem suporte a 
outros sistemas e tem várias outras formas de instalar, 
veja mais em [Install Hugo - Inglês](https://gohugo.io/getting-started/installing/).

## Como usar

Para criar ou alterar páginas basta estar na branch `develop` e acessar aa pasta `content` 
que contem a estrutura de páginas e urls padrão.

Para visualizar suas mudanças antes e commitar, pode usar o servidor embutido do Hugo:

```
hugo server 
```

Caso queria somente buildar novamente os arquivos execute `hugo`.

## Enviando as mudanças

Sempre que quiser enviar uma mudança para esse repositório, crie um nova branch baseada em `develop` 
e solicite um pull request, pois fica mais facil revisar o que foi feito. Não precisa fazer pull request de build. 
No futuro os builds serão automáticos.
