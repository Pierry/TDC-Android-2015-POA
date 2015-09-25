TDC 2015 (Porto Alegre) Trilha Android
======================
O objetivo da apresentação é demonstrar que um aplicativo com uma arquitetura bem estruturada, facilita muito o entendimento e a manutenção do código, principalmente em softwares que tendem a receber atualização por um grande período.
Em casos de rotatividade na empresa, a curva de aprendizado pode ser facilmente contornada quando existem padrões que servem de pré requisito para a busca de um novo colaborador.

https://docs.google.com/presentation/d/11Z4k4Fh-gHKMC7z8ITGsvlPIct97c2tzf3RkpZrVuAk/edit?usp=docslist_api

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
Por que não iniciar um projeto MVP com uma arquitetura bacana para no futuro apenas refatorar e evoluir o software?


## A importância de uma arquitetura robusta

### Por que?
A cada nova contratação ou alteração de quadro de pessoal é a mesma dor de cabeça, a curva de aprendizagem para entender o que o software faz e como faz. Aprender os padrões do programador antigo, como evitar isso? Utilizando uma arquitetura organizada com padrões bem definidos, a preocupação na hora de contratar será bem menor, considerando que você poderá buscar profissionais que já entendam determinado padrão.

### Como?
Existem milhões de padrões, entender quais se encaixam melhor com suas necessidades e aplicar é uma saida, além de considerar utilizar os principios SOLID, que são básicos para qualquer projeto.

### Quando?
Em projetos MVP, é comum deixar de lado todas as boas práticas para entregar rápido, até que ponto é interessante ter de refazer o produto novamente? Entendo que todo o projeto deve ser criado com o mínimo de estrutura, para evoluir com escalabilidade.

### Pra quem?
Para nós, desenvolvedores.
Uma arquitetura bacana, ajudará todos os desenvolvedores que interagem com o sistema, por existir um padrão base, onde o dev deve aprender o padrão e não as ideologias de cada programador.

## SOLID

Identificados por Uncle Bob (Robert C. Martin) por volta dos anos 2000, os princípios SOLID tem o objetivo de:
- Ser fácil de se manter, adaptar e se ajustar às alterações de escopo;
- Ser testável e de fácil entendimento;
- Ser extensível para alterações com o menor esforço necessário;
- Que forneça o máximo de reaproveitamento;
- Que permaneça o máximo de tempo possível em utilização.

Utilizando os princípios SOLID é possível evitar problemas muito comuns:
- Dificuldade na testabilidade / criação de testes de unidade;
- Código macarrônico, sem estrutura ou padrão;
- Dificuldades de isolar funcionalidades;
- Duplicação de código, uma alteração precisa ser feita em N pontos;
- Fragilidade, o código quebra facilmente em vários pontos após alguma mudança.

### SRP (Principio da Responsabilidade Única)
Uma classe deve ter um, e somente um, motivo para mudar.

### OCP (Princípio Aberto-Fechado)
Entidades devem estar abertas para extensão, mas fechadas para modificação.

###LSP (Princípio da Substituição de Liskov)
As classes derivadas devem ser substituíveis por suas classes base.

###ISP (Princípio da Segregação da Interface)
Muitas interfaces específicas são melhores do que uma interface única.

###DIP (Princípio da inversão da dependência)
Dependa de uma abstração e não de uma implementação.


## Repository Pattern

### O que é?
O padrão Repository nasceu com o intuito de isolar a lógica de acesso a dados de qualquer outra lógica da sua aplicação, permitindo que a mesma seja projetada com o mínimo de dependência de recursos de infra-estrutura de acesso a dados.

### Por que?
Desacoplamento das regras de negócio é o argumento mais forte. 
Com este padrão podemos deixar isolada a lógica que se comunica com o banco de dados, ajudando também em possíveis migrações, visto que teremos as regras na camada de cima.
Numa possível alteração de uma implementação sem frameworks por exemplo, para a implantação de um ActiveAndroid por exemplo, se daria apenas na criação de outra classe, satisfazendo as interfaces, e alterando os objetos no container de injeção de dependências.


## Dependency Injection no Android

### O que é?
Injeção de dependência é um padrão de desenvolvimento de programas de computadores utilizado quando é necessário manter baixo o nível de acoplamento entre diferentes módulos de um sistema. 

### Programe para uma interface
Diminuir o acoplamento é o principal motivo. Imagine que você necessita mudar o ORM do banco de dados, programando para classes concretas você deve ir em todas as chamadas e alterar a classe, programando para uma interface, você deve apenas ir no seu container, e fazer a alteração, mantendo a coesão e a estrutura.

## RoboGuice, Dagger, Android Annotations

### RoboGuice
Fácil configuração, rápido e o container funciona muito bem, mas utiliza reflection, o que pode causar perda de desempenho.

### Dagger
Provavelmente o mais completo e melhor, recomendadissmo, para iniciantes torna-se um pouco complexo.

### Android Annotations
Fácil configuração e não possui problemas de desempenho, apenas não possui container de injeção de dependência, tendo que fazer na mão em toda classes que utilizará a interface.

Aplicação de exemplo
=======================

[Backeasy](https://github.com/Pierry/Backeasy)

Referências
========================

- [Dependency Injection](http://www.martinfowler.com/articles/injection.html)
- [SOLID](http://eduardopires.net.br/2015/01/solid-teoria-e-pratica/)
- [RoboGuice](https://github.com/roboguice/roboguice)
- [Dagger 2](http://google.github.io/dagger/)
- [Android Annotations](https://github.com/excilys/androidannotations)
- [https://msdn.microsoft.com/en-us/library/ff649690.aspx](Repository Pattern)
- [Specification Pattern](http://martinfowler.com/apsupp/spec.pdf)
