---
layout: post 
title: NeoVim, o Dark Souls dos editores de código! 
tags: [dev, vim, neovim] 
comments: true 
--- 

***Opa pessoal! Tudo bem?***

Hoje vamos falar sobre o NeoVim, tentar entender o motivo de ele ser tão temido
por alguns programadores. Alguns, até mais avançados, passam longe e ficam
perdidos quando o vim abre do nada no terminal. Vou compartilhar um pouco da
minha experiência durante algumas semanas de uso no meu trabalho e fora dele,
assim como a jornada para configurá-lo e deixá-lo do jeito que gosto.

### Motivo para usar o NeoVim

Trabalhei por muito tempo usando outras ferramentas de código, mas sempre me
interessava em como seria trabalhar com o vim/neovim. Já tinha tentado outras
vezes, mas ainda ficava preso às ferramentas e facilidades do Visual Studio
Code. Isso começou a mudar quando o VSCode começou a ficar pesado e demorava um
pouco mais para executar. Dependendo do tamanho do projeto, ele sofria um pouco
para carregar todas as importações. Vi que essa seria a razão perfeita para
trabalhar com o Vim!

### Jornada no NeoVim

Trabalhei com Neovim por quase 1 mês de forma profissional e no meu ambiente
pessoal. A primeira semana foi dedicada a montar uma configuração eficiente
para trabalhar com a mesma agilidade que tenho no VSCode. Encontrei uma
configuração muito boa para mim, o LunarVim! Tem tudo que uma IDE simples tem,
até mesmo um debugger configurável (apesar de eu usar o do VSCode). Com base no
LunarVim, decidi adicionar minhas customizações. Para fazer isso, é necessário
ter um pouco de conhecimento em Lua. Nada muito difícil; algumas horas olhando
a documentação do LunarVim e da linguagem Lua me permitiram montar minha
configuração para conseguir trabalhar sem sofrer tanto.

Quando abri o meu projeto pessoal, a maior dificuldade foi adaptar o uso do
teclado e deixar o uso do mouse um pouco de lado. Apesar de o LunarVim permitir
o uso do mouse, a ideia do Vim/Neovim é ser usado sem mouse. Na época em que o
antecessor do Vim foi criado, era tudo no terminal, sem mouse, somente comandos
via teclado. Então bora configurar o NeoVim para as minhas necessidades!


### Configuração dos meus sonhos

Encontrei o LunarVim ao assistir um vídeo do Fábio Akita sobre o WSL2, no qual
ele demonstra como configurar e utilizar. Durante o vídeo, ele apresentou o
LunarVim como uma configuração para o NeoVim.

Quando vi, foi definitivo: é essa configuração que vou usar. 
Então, instalei e comecei a usar, criando um projeto simples com NestJS para praticar. No entanto, percebi que faltavam algumas coisas que eram essenciais para mim.
Gradualmente, fui organizando alguns keymaps e plugins, e no final, ficou perfeito para mim. Conseguia pesquisar os arquivos, controlar os buffers e até
mesmo abrir o terminal dentro dele (embora eu não tenha gostado muito disso e acabei substituindo com outra ferramenta).

Um ponto no qual ainda não me sinto muito confortável é o debugging do código.
No final, preciso configurar um DAP para cada linguagem.
Por exemplo, ao trabalhar com Ruby on Rails, não consegui configurar um debugger tão eficiente quanto o do VSCode. 
Então, em situações como essa, acabo retornando para o VSCode.

Caso queira utilizar as minhas configurações segue a baixo o link do github.

Minha configuração: [My LunarVim](https://github.com/paulohsilvavieira/my-lunarvim-config)


### Extras para facilidade

Para substituir o terminal do LunarVim, utilizei uma ferramenta perfeita, o Zellij, uma opção bem da hora para nosso querido tmux e tmuxinator, 
configurei de uma forma para abrir tudo que eu preciso, quando abrir qualquer projeto, segue abaixo um exemplo de como ficou meu terminal depois de configurar tudo:


![!Zellij + LunarVim](/assets/img/neovim-darksouls/dev-env.jpeg)
***Lindo demais***

Minha configuração: [MyZellij](https://github.com/paulohsilvavieira/my-zellij-config)

Estou utilizando duas ferramentas sensacionais para terminal o LazyGit e o LazyDocker nesse exemplo, um para gerenciar o GIT a outra para gerenciar Docker, 
vale a pena estudar também!

### NeoVim é realmente difícil?

A resposta para essa pergunta é: sim, é difícil!
Como qualquer ferramenta de desenvolvimento com a qual você não teve contato antes!

O maior erro ao trabalhar com o Neovim é esperar que ele faça tudo que sua IDE preferida faz. 
Alguns desenvolvedores esquecem como foi o processo de se adaptar ao uso de sua ferramenta preferida pela primeira vez, as dificuldades
de encontrar as funcionalidades. Com o Neovim, é a mesma coisa.
Todo aprendizado no início é doloroso, mas se insistir, vai ficar mais fácil!

Muita gente fica dizendo, "nossa, eu não gosto de Vim, nao consigo fazer nada, nem consigo fechar", parece bem com comentarios do famoso dark souls 
"nossa, não gosto do dark souls, mal consigo sair do começo do jogo, toda hora eu morro", 
a evolução de conhecimento,no vim quanto o dark souls depende exclusivamente de quem está segurando o controle/teclado.
Use, jogue, sofra um pouco, quando perceber as teclas **ghjk** vão parecer coisas simples de usar, senta na cadeira e pratique, hoje temos muitas
documentações que ajudam demais, muitas pessoas passaram pelos mesmos problemas que você! No final, o orgulho de abrir o vim e conseguir editar
um arquivo, vai ser o combustível para praticar e estudar mais ainda essa ferramenta excelente.

Então é isso! Comente, compartilhe, diga ai sua experiência com vim! 


**Links para estudo e pesquisa:**

[Zellij](https://zellij.dev/) - Alternativa para Tmux\
[LunarVim](https://www.lunarvim.org/) - Melhor configuração sim ou claro?\
[LazyGit](https://github.com/jesseduffield/lazygit) - Simples e bonito, um gerenciador de git que realmente funciona\
[LazyDocker](https://github.com/jesseduffield/lazydocker) - Vale a pena olhar e testar!


