# ecommerce-syntexwear

Projeto de loja virtual front-end estático (HTML + CSS) criado como exemplo de layout e componentes para venda de tênis/sneakers.

## Visão Geral
Este repositório contém os arquivos do site estático da "SyntaxWear": um protótipo de e-commerce com componentes principais (header, hero, grid de produtos, cards de categorias e footer). O projeto é responsivo e usa CSS modularizado por componentes.

Arquivos principais:
- [index.html](index.html) — página HTML principal.
- Estilos:
  - [assets/css/reset.css](assets/css/reset.css) — reset moderno.
  - [assets/css/base.css](assets/css/base.css) — estilo base do projeto.
  - [assets/utils/variables.css](assets/utils/variables.css) — variáveis (ex: `--fonte-principal`).
  - Componentes:
    - [assets/css/components/header.css](assets/css/components/header.css) — classes: [`.site-header`](assets/css/components/header.css), [`.menu-toggle`](assets/css/components/header.css), [`.menu-icon`](assets/css/components/header.css).
    - [assets/css/components/hero.css](assets/css/components/hero.css) — classes: [`.hero-section`](assets/css/components/hero.css), [`.hero-content`](assets/css/components/hero.css).
    - [assets/css/components/product-card.css](assets/css/components/product-card.css) — classes: [`.category-card`](assets/css/components/product-card.css), [`.category-name`](assets/css/components/product-card.css).
    - [assets/css/components/product-grid.css](assets/css/components/product-grid.css) — classes: [`.grid-section`](assets/css/components/product-grid.css), [`.card`](assets/css/components/product-grid.css).
    - [assets/css/components/footer.css](assets/css/components/footer.css) — classes: [`.footer-container`](assets/css/components/footer.css), [`.footer-left`](assets/css/components/footer.css).
  - Layout (arquivo referenciado mas ausente):
    - [assets/css/layout.css](assets/css/layout.css) — (referenciado em `index.html`, verificar existência).
  - Newsletter (arquivo referenciado mas ausente):
    - [assets/css/components/newsletter.css](assets/css/components/newsletter.css) — (referenciado em `index.html`, verificar existência).
- Imagens & ícones (referenciadas no HTML/CSS):
  - Logo: [assets/img/logo/Logo.png](assets/img/logo/Logo.png)
  - Ícones: `hamb.svg`, `perfilicon.png`, `suporte.png`, `carrinhoicon.png`, `instagramicon.png`, `whatsappicon.png`, `ttklogo.png`, `facebookicon.png` — localizados em [assets/img/icons/](assets/img/icons/)
  - Produtos / banners: [assets/img/products/](assets/img/products/) e [assets/img/banners/](assets/img/banners/) (ex.: `hero.jpg`, `casual.jpg`, `futurista.jpg`, etc.)

> Observação: alguns arquivos CSS são referenciados em `index.html` mas não estavam incluídos no workspace (ver “Arquivos ausentes”).

## Como visualizar localmente
Opções simples para rodar o projeto:
1. Abrir [index.html](index.html) diretamente em um navegador (bom para testes rápidos).
2. Usar servidor estático local (recomendado para rotas e recursos):
   - Python (porta 8000):
     ```sh
     python -m http.server 8000
     ```
   - Node.js http-server:
     ```sh
     npx http-server -c-1
     ```
   - VS Code: usar a extensão "Live Server" e abrir [index.html](index.html).

## Estrutura de pastas
- assets/
  - css/
    - reset.css
    - base.css
    - layout.css (verificar)
    - components/
      - header.css
      - hero.css
      - product-card.css
      - product-grid.css
      - footer.css
      - newsletter.css (verificar)
  - utils/
    - variables.css
  - img/
    - banners/
    - favicons/
    - icons/
    - logo/
    - products/

## Principais componentes e como editar
- Header (arquivo: [assets/css/components/header.css](assets/css/components/header.css))
  - Menu móvel: input [`.menu-toggle`](assets/css/components/header.css) e label `.menu-icon`.
  - Logo: altere [assets/img/logo/Logo.png](assets/img/logo/Logo.png) para trocar a marca.

- Hero (arquivo: [assets/css/components/hero.css](assets/css/components/hero.css))
  - Fundo hero: [assets/img/banners/hero.jpg](assets/img/banners/hero.jpg) é usado; altere a imagem ou a propriedade `background-position` para ajustes.
  - Botões: classes `.btn`, `.btn-outline`, `.btn-filled`.

- Grid / Cards
  - Grid: [assets/css/components/product-grid.css](assets/css/components/product-grid.css) — área principal `.grid-section`.
  - Cards: [assets/css/components/product-card.css](assets/css/components/product-card.css) — cards de categorias e imagens de fundo (`casual.jpg`, `moderno.jpg`, etc.).

- Footer
  - Contato, newsletter e links: [assets/css/components/footer.css](assets/css/components/footer.css).

- Variáveis
  - Fontes e outras variáveis estão em [assets/utils/variables.css](assets/utils/variables.css). Ex: `--fonte-principal`.

## Observações técnicas
- A fonte principal é importada em [assets/utils/variables.css](assets/utils/variables.css) via Google Fonts.
- Elementos de layout usam media queries para responsividade (ex.: max-width: 768px e 1280px).
- Reset moderno aplicado via [assets/css/reset.css](assets/css/reset.css).
- Alguns componentes usam imagens de background (via `background-image: url(...)`), verifique os caminhos nas CSS para manter consistência.
- O `index.html` referencia arquivos ausentes:
  - [assets/css/components/newsletter.css](assets/css/components/newsletter.css) — verifique/adicione estilos.
  - [assets/css/layout.css](assets/css/layout.css) — se faltar, adicionar ou corrigir.

## Acessibilidade & SEO
- `index.html` contém atributos de aria em alguns elementos (por ex.: `aria-label` nas navs e newsletter).
- Use textos alternativos (`alt`) para imagens e ícones (muitos ícones já incluem).
- Considere usar roles e melhorar foco via CSS/JS se necessário.

## Como contribuir
- Fork -> Branch -> Pull Request.
- Padronize cores, variáveis e fontes via [assets/utils/variables.css](assets/utils/variables.css).
- Adicione componentes novos como arquivos separados em [assets/css/components/](assets/css/components/).
- Atualize as imagens em [assets/img/](assets/img/).

## To-dos / Melhorias sugeridas
- Adicionar/validar esses arquivos referenciados em `index.html`:
  - [assets/css/components/newsletter.css](assets/css/components/newsletter.css)
  - [assets/css/layout.css](assets/css/layout.css)
- Otimizar imagens para web (compressão e formatos modernos, ex.: WebP).
- Adicionar meta tags adicionais para SEO e Open Graph.
- Tornar o header sticky corretamente, avaliando `top` e transform (atualmente `top: 60px`).
- Adição de JS para interações (carrinho, filtros, toggles com melhor acessibilidade).

## Licença
- LICENÇA: adicione uma licença (ex.: MIT) no arquivo LICENSE.

## Deploy
- Static site: GitHub Pages, Netlify ou Vercel são ótimas opções.
- Para GitHub Pages: selecione a branch main/master e habilite Pages no repositório.