# 🤝 Apoio Digital ao Idoso

Site com tutoriais simples, com letras grandes, para ajudar os idosos de Capanema/PR e região a fazer tarefas básicas no celular e na internet: **mandar mensagens**, **fazer chamadas de vídeo** e **identificar golpes**.

**Site publicado:** https://SEU-PROJETO.vercel.app
**Repositório:** https://github.com/tiagoidio20/trabalho_Tiago.Teixeira

---

## 1. Demanda identificada

Muitos idosos da região têm celular, mas sentem dificuldade nas tarefas do dia a dia (letras pequenas, muitos botões, medo de errar) e são o alvo preferido de golpes por mensagem e ligação (falso parente, falsa central do banco, código do WhatsApp).

## 2. Solução desenvolvida

| Página | O que resolve |
|---|---|
| `index.html` | Apresenta o projeto, a demanda, os tutoriais, as 3 regras de ouro contra golpes e o formulário para pedir ajuda de um voluntário |
| `mensagens.html` | Passo a passo para mandar mensagem escrita, áudio e foto no WhatsApp |
| `chamada-video.html` | Passo a passo para fazer e atender chamadas de vídeo |
| `golpes.html` | Os golpes mais comuns, sinais de alerta e o que fazer se cair em um golpe |
| `obrigado.html` | Confirmação após enviar o formulário |

### Acessibilidade para o público idoso
- Letra base de **20px** (`html { font-size: 125%; }`) e fonte **Atkinson Hyperlegible**, criada para facilitar a leitura
- Alto contraste entre texto e fundo
- Botões e campos com no mínimo **56px** de altura, fáceis de tocar
- Caixas de seleção maiores (26px) e foco bem visível
- Linguagem simples, um passo por vez, com números grandes

## 3. Tecnologias

- **HTML5** semântico: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`, `ol`, `form`, `fieldset`, `legend`, `label`
- **CSS3**: variáveis, Flexbox, Media Queries, transições
- **Git e GitHub** · **Vercel**

## 4. Estrutura

```
├── index.html
├── mensagens.html
├── chamada-video.html
├── golpes.html
├── obrigado.html
├── css/
│   └── style.css
└── README.md
```

## 5. Onde o Flexbox foi usado

| Elemento | Propriedades | Efeito |
|---|---|---|
| `.cabecalho-conteudo` | `flex-direction`, `justify-content: space-between` | Logo à esquerda e menu à direita no desktop |
| `.menu` | `flex-wrap: wrap`, `gap` | Itens do menu quebram linha no celular |
| `.botao` | `inline-flex`, `align-items: center` | Texto centralizado nos botões grandes |
| `.hero-conteudo` | `flex-direction: row` (desktop) | Texto e ilustração lado a lado |
| `.hero-ilustracao`, `.passo-numero`, `.regra-numero` | `justify-content` + `align-items: center` | Centralização perfeita dentro do círculo |
| `.demanda` | `flex: 1` | Três cards com a mesma largura |
| `.tutoriais`, `.golpes` | `flex-wrap: wrap`, `flex-basis` com `calc()` | Grade de 1, 2 ou 3 cards por linha |
| `.card-acao`, `.golpe-fazer` | `margin-top: auto` | Empurra o conteúdo para o fim do card, alinhando os cards |
| `.passo` | `flex-shrink: 0` no número, `flex: 1` no texto | Número fixo à esquerda e texto ocupando o resto |
| `.sinais` | `flex-wrap: wrap` | Etiquetas de alerta que quebram linha |
| `.ajuda` | `flex: 1` / `flex: 2` | Formulário ocupa o dobro do espaço do texto |
| `.linha`, `.campo` | `flex-direction: column/row` | Campos empilhados no celular e lado a lado no tablet |
| `.form-botoes` | `column-reverse` / `row` | No celular o botão "Enviar" fica em cima |
| `.obrigado` | `justify-content` + `align-items: center` | Mensagem centralizada na tela |

## 6. Responsividade (Media Queries)

Abordagem **mobile-first**: estilos base para celular e media queries ampliam o layout.

| Tela | Breakpoint | O que muda |
|---|---|---|
| Celular | até 599px | Tudo em uma coluna; botões ocupando a largura |
| Tablet | `@media (min-width: 600px)` | Botões lado a lado; 2 cards de golpe por linha; campos do formulário lado a lado; rodapé em colunas |
| Desktop | `@media (min-width: 900px)` | Cabeçalho fixo em linha; hero em 2 colunas; 3 cards por linha; formulário ao lado do texto |

## 7. Como executar

Abrir o `index.html` no navegador ou usar a extensão **Live Server** do VS Code.

## 8. Melhorias futuras

- Salvar os pedidos de ajuda com Formspree/FormSubmit ou banco de dados
- Botão para aumentar e diminuir a letra
- Vídeos curtos em cada tutorial
- Tutoriais de Pix seguro, aplicativos do governo e agendamento de consultas

---

Desenvolvido por **Tiago Teixeira** · Técnico em Informática · Linguagem e Técnicas de Programação I · Prof. Anderson José Lauer
