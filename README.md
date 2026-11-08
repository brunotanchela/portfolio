# 🌐 Portfólio Pessoal — Bruno Tanchela

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/status-concluído-brightgreen?style=for-the-badge)

**Aluno:** Bruno Tanchela — Curso de Desenvolvimento de Sistemas (ETEC)

🔗 **Site publicado:** [COLE_AQUI_O_LINK_DO_GITHUB_PAGES](COLE_AQUI_O_LINK_DO_GITHUB_PAGES)

---

## 📋 Descrição do portfólio

Site de apresentação profissional, desenvolvido como atividade prática. A página reúne em uma única tela com navegação por seções:

- **Perfil:** foto, apresentação e botões de acesso rápido;
- **Projetos:** cards com os projetos desenvolvidos por mim, cada um com link para o repositório no GitHub;
- **Habilidades:** competências técnicas, idiomas e soft skills;
- **Contato:** links para o GitHub e o e-mail.

O layout é responsivo - as seções e os cards se reorganizam conforme o tamanho da tela (celular, tablet e desktop).

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Uso no projeto |
|---|---|
| HTML5 | Estrutura semântica da página (`nav`, `section`, `footer`) |
| CSS3 | Estilos personalizados em `css/estilo.css`, aplicados sobre o Bootstrap |
| Bootstrap 5.3 (CDN) | Grid, navbar, cards, botões, badges, barra de progresso e temas |
| JavaScript | Alternância entre tema claro e escuro |
| GitHub Pages | Publicação do site |

---

## ⚙️ Explicação do funcionamento

O site é uma **página única** (`index.html`) dividida em seções, e o menu de navegação usa âncoras (`href="#projetos"`) para levar o usuário a cada uma delas, com rolagem suave.

- **Menu de navegação:** a `navbar` do Bootstrap fica fixa no topo (`sticky-top`) e se transforma em um botão "hambúrguer" em telas pequenas.
- **Cards de projetos:** ficam lado a lado em telas médias e grandes (`row-cols-md-3`) e empilham no celular. Com `h-100`, `d-flex flex-column` e `mt-auto`, todos têm a mesma altura e o botão "Ver no GitHub" fica alinhado na parte inferior.
- **Habilidades:** badges e barra de progresso para a parte técnica; idiomas e soft skills organizados em duas colunas.

---

## ✨ Recurso novo adicionado

**1. Alternância entre tema claro e escuro.**
Um botão na barra de navegação permite ao visitante trocar o tema da página. Esse recurso não foi visto em aula.

**2. Seção de Habilidades.**
Uma nova seção, além do que foi pedido em aula, reunindo competências técnicas, idiomas e soft skills.

---

## 🔧 Como esse recurso foi implementado

**Tema claro/escuro:** o Bootstrap 5.3 aplica as cores conforme o atributo `data-bs-theme` do elemento `<html>`. O botão apenas alterna o valor desse atributo entre `light` e `dark`, usando JavaScript:

```html
<button id="tema" class="btn btn-outline-light btn-sm">Alternar tema</button>

<script>
    document.getElementById("tema").addEventListener("click", () => {
        const html = document.documentElement;
        html.setAttribute("data-bs-theme",
            html.getAttribute("data-bs-theme") === "dark" ? "light" : "dark");
    });
</script>
```

Para que as seções também mudassem de cor, foram usadas as classes `bg-body-tertiary` (que acompanha o tema) no lugar de `bg-light` (que é branco fixo).

**Seção de Habilidades:** montada com componentes do Bootstrap, sem JavaScript:
- `badge` para as tecnologias;
- `progress` para o nível de Python;
- `list-group` para idiomas e soft skills, em duas colunas (`row` + `col-md-6`).

---

## 🚀 Como executar

**Online:** acesse o link do site publicado, no início deste README.

**Localmente:**
1. Baixe ou clone o repositório e, se estiver em `.zip`, **extraia tudo** antes de abrir.
2. Mantenha a estrutura de pastas (`index.html`, `css/`, `imgs/`).
3. Abra o `index.html` no navegador.

---

## 🗂️ Estrutura do repositório

```
portfolio/
├── index.html
├── css/
│   └── estilo.css
├── imgs/
└── README.md
```