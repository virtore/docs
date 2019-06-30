---
title: Infraestrutura
weight: 20
pre: "<b>4. </b>"
chapter: false
---

# Introdução

Enteda como funciona a infruestrutura do projeto. Nessa página iremos falar de forma macro e nas demais páginas podemos ir detalhando partes do processo e de funcionamento da estrutura.

Para melhor entendimento, veja a imagem abaixo e logo após irei explicar melhor a infraestrutura do projeto.

![Virtore Commerce - Infraestrutura - V1](/docs/images/virtore-infrastruture-v1.png)

Na figura acima, vemos a estrutura do **Virtore Server (API)**, onde fica a API principal do projeto, os Virtore Web, que são os servidores que podem rodar a linguagem que melhor pra o cliente, desde Python a C/C++, e também vemos a camada de segurança e outras formas de conexão a API.

### Virtore Server (API)

Essa camada somente faz processamentos, ou seja, não lida com nada relacionado a frontend, ou ao menos evita. Essa camada ficar separada do Virtore Web é importante pode ela pode ser escalada separadamente sem ter que se preocupar em como o cliente visualiza o site ou loja.

Outra grande importancia é poder oferecer aplicativos, e outras formas de usar a ferramenta sem ter que ficar se preocupado em como usar pois o padrão de comunicação será o mesmo entre todos.

O Virtore Server (API) irá ficar com a responsabilidade de conectar serviços de terceiros para garantir melhor resposta e funcionamento, sem tempos de esperar ou afins, em outras palavras, os serviço poderão ser agregados aqui, porém a resposta aos cliente da API deverão sempre ser o mais rápido que possível.

### Virtore Web

Essa camada pode ser montanda em cima das SDK que serão ou já foram disponibilizadas pela Virtore ou basta ler a documentação e montar as conexões com a API do Virtore Server (API), que irá conseguir usar facilmente de acordo com suas necessidades.

Além disso, a idéia de essa camada ficar separada do Virtore Server (API) é que as mudanças necessárias de otimização de frontend ficam aqui e não no Virtore Server (API), se precisar e puder fazer cache sem ficar consultando a API toda hora fica bem melhor se for separada.

Como o Virtore Server (API) não irá guardar e gerenciar todas as informações nessa camada pode ser necessário o uso de uma bando de dados para guardar as configurações referentes as Templates, Caches, Conexões, Carrinhos e dentre outros. O armazenamento não precisa ser feito usando um SGBD (ingles) / DBMS (portugues), pode ser feito usando arquivos, redis e outros.

### Outros Clientes da API

Poderá haver outras formas de conectar ao Virtore Server (API) usando a API com os devidos códigos de acesso. Um bom exemplo disso, seria um aplicativo mobile que pode ajudar os usuários a configurar produtos, pedidos e demais itens sem ter que usar um computador ou notebook. 

Isso é somente mais um facilitador desse processo como um todo, mas com o decorrer do crescimento do projeto poderemos ter bem mais informações sobre para melhor todo esse fluxo.