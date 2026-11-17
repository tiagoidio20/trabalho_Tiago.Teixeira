# Apoio Digital ao Idoso

Trabalho da disciplina de Linguagem e Técnicas de Programação I (Técnico em Informática), prof. Anderson José Lauer.

Site com tutoriais simples para ajudar os idosos de Capanema e região a usar o celular: mandar mensagens, fazer chamada de vídeo e reconhecer golpes. Também tem um formulário para a pessoa pedir ajuda de um voluntário.

- Site: https://apoio-digital-ao-idoso.vercel.app
- Repositório: https://github.com/tiagoidio20/trabalho_Tiago.Teixeira

## Demanda

Muita gente mais velha aqui da região tem celular mas tem dificuldade com coisas básicas (letra pequena, muitos botões, medo de mexer e estragar). Além disso são os que mais caem em golpe de mensagem e ligação, tipo o do falso parente ou o da falsa central do banco.

## Páginas

- index.html - página inicial, explica o projeto, mostra os tutoriais, as regras contra golpe e o formulário de ajuda
- mensagens.html - como mandar mensagem, áudio e foto no WhatsApp
- chamada-video.html - como fazer e atender chamada de vídeo
- golpes.html - golpes mais comuns, sinais de alerta e o que fazer se cair em um
- obrigado.html - página que aparece depois de enviar o formulário

## Tecnologias

- HTML (tags semânticas como header, nav, main, section, article, aside, footer e formulário com fieldset, label, select, checkbox e radio)
- CSS com variáveis, Flexbox e Media Queries
- Git e GitHub
- Vercel para publicar

Pensando no público, a letra base é de 20px, usei a fonte Atkinson Hyperlegible (feita para facilitar a leitura), cores com bastante contraste e botões com pelo menos 56px de altura.

## Flexbox e responsividade

Fiz mobile-first: o CSS base é para celular, com quase tudo em coluna (`flex-direction: column`). Depois tem duas media queries:

- `min-width: 600px` (tablet): botões e campos do formulário lado a lado, 2 cards de golpe por linha, rodapé em colunas
- `min-width: 900px` (desktop): cabeçalho com logo de um lado e menu do outro (`justify-content: space-between`), 3 cards por linha e o formulário do lado do texto

Alguns usos do Flexbox no projeto:

- `flex-wrap: wrap` no menu, nos cards e nas etiquetas de alerta, pra quebrar linha quando não cabe
- `flex: 1` nos cards da demanda pra ficarem do mesmo tamanho
- `flex: 1` e `flex: 2` na área de ajuda, o formulário fica com o dobro do espaço
- `margin-top: auto` pra empurrar o "Ver tutorial" e o "O que fazer" pro final dos cards
- `flex-shrink: 0` nos círculos com número pra eles não amassarem
- `column-reverse` nos botões do formulário, assim no celular o "Enviar" aparece primeiro

## Como rodar

É só abrir o index.html no navegador ou usar o Live Server no VS Code.

## Ideias para depois

- Salvar os pedidos de ajuda de verdade (Formspree ou um banco de dados)
- Botão para aumentar a letra
- Vídeos curtos nos tutoriais
- Tutorial de Pix e de aplicativos do governo

Feito por Tiago Teixeira.
