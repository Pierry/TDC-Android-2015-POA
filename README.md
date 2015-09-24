TDC 2015 (Porto Alegre) Trilha Android
======================
O objetivo da apresentação é demonstrar que um aplicativo com uma arquitetura bem estruturada, facilita muito o entedimento e a manutenção do código, principalmente em softwares que tendem a receber atualização por um grande período.
Em casos de rotatividade na empresa, a curva de aprendizagem pode ser facilmente contornada quando existem padrões que servem de pré requisito para a busca de um novo colaborador.

Como está a arquitetura de seu app?
======================

- Cenário atual
- A importância de uma arquitetura robusta
- SOLID
- Repository Pattern
- Dependency Injection no Android

## Cenário atual
Vivemos numa época onde uma ideia pode valer 1 milhão de reais, e essa ideia deve ser desenvolvida o mais rápido possível.
Como criar um MVP (Minimium Viable Product) que não necessite ser refeito após o projeto engrenar?
Visual é importante, mas focar apenas nisso pode resultar num sistema com a manutenção complexa, gerando dependência do programador.
MVP - Por que não iniciar um projeto MVP com uma arquitetura bacana para no futuro apenas refatorar e evoluir o software?


## A importância de uma arquitetura robusta

# Por que?
A cada nova contratação ou alteração de quadro de pessoal é a mesma dor de cabeça, a curva de aprendizagem para entender o que o software faz e como faz. Aprender os padrões do programador antigo, como evitar isso? Utilizando uma arquitetura organizada com padrões bem definidos, a preocupação na hora de contratar será bem menor, considerando que você poderá buscar profissionais que já entendam determinado padrão.

# Como?
Existem milhões de padrões, entender quais se encaixam melhor com suas necessidades

# Quandow

# Pra quem?


## SOLID

Identificados por Uncle Bob (Robert C. Martin) por volta dos anos 2000, os princípios SOLID tem o objetivo de:
Ser fácil de se manter, adaptar e se ajustar às alterações de escopo;
Ser testável e de fácil entendimento;
Ser extensível para alterações com o menor esforço necessário;
Que forneça o máximo de reaproveitamento;
Que permaneça o máximo de tempo possível em utilização.

Utilizando os princípios SOLID é possível evitar problemas muito comuns:
Dificuldade na testabilidade / criação de testes de unidade;
Código macarrônico, sem estrutura ou padrão;
Dificuldades de isolar funcionalidades;
Duplicação de código, uma alteração precisa ser feita em N pontos;
Fragilidade, o código quebra facilmente em vários pontos após alguma mudança.

# SRP (Principio da Responsabilidade Única)
Uma classe deve ter um, e somente um, motivo para mudar.

# OCP (Princípio Aberto-Fechado)
Entidades devem estar abertas para extensão, mas fechadas para modificação.

#LSP (Princípio da Substituição de Liskov)
As classes derivadas devem ser substituíveis por suas classes base.

#ISP (Princípio da Segregação da Interface)
Muitas interfaces específicas são melhores do que uma interface única.

#DIP (Princípio da inversão da dependência)
Dependa de uma abstração e não de uma implementação.


## Repository Pattern

# O que é?
O padrão Repository nasceu com o intuito de isolar a lógica de acesso a dados de qualquer outra lógica da sua aplicação, permitindo que a mesma seja projetada com o mínimo de dependência de recursos de infra-estrutura de acesso a dados.

# Por que?
Desacoplamento das regras de negócio é o argumento mais forte. 
Com este padrão podemos deixar isolada a lógica que se comunica com o banco de dados, ajudando também em possíveis migrações, visto que teremos as regras na camada de cima.
Numa possível alteração de uma implementação sem frameworks por exemplo, para a implantação de um ActiveAndroid por exemplo, se daria apenas na criação de outra classe, satisfazendo as interfaces, e alterando os objetos no container de injeção de dependências.


## Dependency Injection no Android

# O que é?
Injeção de dependência é um padrão de desenvolvimento de programas de computadores utilizado quando é necessário manter baixo o nível de acoplamento entre diferentes módulos de um sistema. 

# Programe para uma interface

# RoboGuice, Dagger, Android Annotations...
