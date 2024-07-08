# Projeto de Animações com JavaScript

Este projeto consiste em uma série de animações implementadas com JavaScript para melhorar a interatividade e a experiência do usuário em uma página web.

<br></br>

## Sumário

- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Status](#status)
- [Descrição](#descrição)
- [Funcionalidades](#funcionalidades)
- [Explicação](#explicação)
- [Como Usar](#como-usar)
- [Autor](#autor)

<br></br>

## Tecnologias Utilizadas

<div style="display: flex; flex-direction: row;">
  <div style="margin-right: 20px; display: flex; justify-content: flex-start;">
    <img src="img/js.png" alt="Logo Linguagem" width="100"/>
  </div>
  <div style="margin-right: 20px; display: flex; justify-content: flex-start;">
    <img src="img/html.png" alt="Logo Linguagem" width="100"/>
  </div>
  <div style="margin-right: 20px; display: flex; justify-content: flex-start;">
    <img src="img/css.png" alt="Logo Linguagem" width="100"/>
  </div>
</div>

<br></br>

## Status

![Concluído](http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge)

<br></br>

## Descrição

Este projeto é uma coleção de animações e interações desenvolvidas para serem usadas em páginas web. Utiliza JavaScript para manipular estilos CSS e criar animações dinâmicas.

<br></br>

## Funcionalidades

- Criação dinâmica de botões personalizados
- Navegação por abas
- Acordeão para conteúdo expandível
- Scroll suave para links internos
- Animação de elementos ao rolar a página

<br></br>

## Explicação

O projeto consiste em várias animações que são ativadas com base em interações do usuário, como cliques ou rolagem de página. Por exemplo, a animação de tabulação permite alternar entre diferentes seções de conteúdo ao clicar em itens de menu.

<br></br>

### Exemplo de Animação de Tabulação:

```javascript
function initTabNav() {
  const tabMenu = document.querySelectorAll('[data-tab="menu"] li');
  const tabContent = document.querySelectorAll('[data-tab="content"] section');

  if (tabMenu.length && tabContent.length) {
    tabContent[0].classList.add("ativo");

    function activeTab(index) {
      tabContent.forEach((section) => {
        section.classList.remove("ativo");
      });
      const direcao = tabContent[index].dataset.anime;
      tabContent[index].classList.add("ativo", direcao);
    }

    tabMenu.forEach((itemMenu, index) => {
      itemMenu.addEventListener("click", () => {
        activeTab(index);
      });
    });
  }
}

initTabNav();
```

<br></br>

## Autor

Desenvolvido no curso de JavaScript da Origamid®️
