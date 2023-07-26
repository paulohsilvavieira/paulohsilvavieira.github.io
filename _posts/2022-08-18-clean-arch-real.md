---
layout: post
title: Arquitetura Limpa - Como Foi aplicar em um projeto Real
subtitle: Um pouco dessa experiência incrível!
tags: [clean arch, dev, solid]
comments: true
---

***Opa pessoal! Tudo bom?***

Gostaria trazer minha experiência ao aplicar o conceito de arquitetura limpa em um projeto real.

*Nesse texto vou considerar que você já saiba sobre arquitetura limpa, mesmo que tenha lido em algum lugar, caso não saiba, corre lá no google dá uma lida e volta aqui para continuar a leitura!*

Vou levantar alguns pontos baseados na minha experiência.

![Clean Arch](/assets/img/clean-arch-post/clean-arch.png)

## Começo de tudo!

A primeira vez que apliquei essa arquitetura, foi depois de finalizar o curso sobre o assunto. Criei um projeto simples e apliquei e vi como era interessante poder separar seu sistema em camadas testáveis e de fácil manutenção.

Em 2021 tive a oportunidade de aplicar essa arquitetura em forma real, onde pude enxergar o real valor do processo.

Lembro de outros projetos onde a implementação dos casos de uso do sistema tinham um alto acoplamento com a tecnologia, pessoalmente dava um pouco de medo ao ver chamadas de banco de dados com SQL direto no domínio, Nesse ponto vi o quanto valeu a pena aplicar essa arquitetura. Em um sistema novo que fiquei encarregado de desenvolver, foi muito tranquilo configurar toda a regra de negócio do sistema independente da tecnologia, podendo esquecer de qual banco de dados ou onde a aplicação vai rodar, pois o que importa é o domínio bem implementado, que os frameworks e banco de dados por exemplo são só detalhes e decisões que podem ser adiadas.

Aliás, uma das partes mais incríveis é criar os adaptadores que isolam o caso de uso da tecnologia. Quando você cria essas abstrações e reutiliza elas durante o código você perde o medo de alguma coisa dar problema, pois não vai ser aquela dor de cabeça para mudar para outra tecnologia mais eficiente ou corrigir implementação da tecnologia, é só fazer a modificação no adaptador e pronto, seu domínio não tem nem ideia do que aconteceu.

Umas das dificuldades que tive foi aplicar os conceitos do SOLID, mas depois de algum sofrimento, consegui entender.*Se não sabe, corre no google e da uma olhada, no final do texto vou deixar um link bem informativo sobre SOLID!* Lembrando, que ao aplicar esses conceitos, você já consegue ter um código eficiente e que tem uma manutenção tranquila, o incrível é que cada regra vai conversando entre si, no início parece um grande ruído, mas quando você vai tentando quebrar uma regra, as outras acompanham o erro.

## Testes!

**Teste**! Essa é a palavra chave dessa arquitetura, é onde você descobre se sua implementação está complexa ou não, pois seu teste deve demonstrar como seu código vai funcionar, se seu teste está difícil de ser escrito, volte e analise sua implementação.

Mas lembre-se, não é necessário ter 100% de cobertura de código, é bom você ter uma cobertura de 100% nos casos de usos mais importantes no seu sistema, tendo isso você já consegue confiar melhor no seu sistema.

Hoje ao ver meu código sinto confiança após aplicar essa arquitetura, não ter medo de corrigir bugs ou até mesmo implementar coisas novas, pois tem um fluxo de criação, abstrações e reuso de componentes que o POO permite.

## Mas arquitetura limpa é isso tudo mesmo ? Err... Não é!

Mas nem tudo são flores na arquitetura limpa, vi uma complexidade enorme ao implementar novas funcionalidades, por ter que passar em várias camadas, criar adaptadores necessários, criar todas as abstrações que a funcionalidade vai exigir aumenta muito o tempo de trabalho que se for em uma arquitetura mais simples ia ser coisa de poucas horas ou poucos minutos mesmo (dependendo da seu nível).

Essa complexidade pode ir de encontro com o estilo da empresa que você esteja trabalhando, se for uma empresa que foca em velocidade de entrega deixando a qualidade de código de lado, lamento mas arquitetura limpa pode não ser a melhor escolha para o desenvolvimento, por ser um processo com muitos pontos para serem desenvolvidos pode gerar ruídos no seu processo de entrega.

Passar o conhecimento para outros desenvolvedores da equipe que nunca viram nada ou viram muito pouco sobre arquitetura limpa também é uma dor, pois você já está ali enfrentando suas dificuldades para entender e tem que passar esse conhecimento para outros desenvolvedores, isso necessita ter uma equipe muito entrosada para  auxiliar essa passada de informação.

Outra dor é o próprio review de código, commits simples ajudam a fazer o review mas imagine uma quantidade absurda de commits simplesmente por que você adicionou um caso de uso novo, pois tem várias interfaces que abstraem as funcionalidades e tecnologias utilizadas no caso de uso, Imagina você indo fazer review de múltiplos commits de vários desenvolvedores e grande parte desses commits são somente interfaces, é uma vontade absurda de colocar `any` em todas as tipagens.

## Conclusão
Arquitetura limpa é ótimo, mas exige conhecimentos como Programação orientada a objetos bem sólido, então para você jovem padawan, estude arquitetura limpa mas não coloque tanta energia agora, absorva bem conceitos importantes sobre programação, como a própria programação orientada a objeto.

Estude em paralelo, sobre DDD (Domain Driven Design), recomendo comprar o livro, ele é um pouco avançado, mas ajuda bastante a aplicar a arquitetura limpa de forma mais robusta no quesito entendimento do negócio.

Em geral vale muito a pena implementar essa arquitetura quando seu sistema seja muito grande ou que tenha muitos processos, se for um sistema simples,escolha uma arquitetura mais simples.

Então é isso pessoal! Comente o que achou, comente sua experiência com arquitetura limpa!

[Link top sobre SOLID](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
