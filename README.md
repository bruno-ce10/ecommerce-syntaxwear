# 🛍️ SyntaxWear - E-commerce de Tênis e Sneakers

> Plataforma moderna e responsiva para compra de tênis e sneakers online com design clean e otimizado para acessibilidade.

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-E34C26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)

## 📋 Sumário

- [Visão Geral](#visão-geral)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Recursos](#recursos)
- [Arquitetura CSS](#arquitetura-css)
- [Guia de Componentes](#guia-de-componentes)
- [Acessibilidade](#acessibilidade)
- [Responsividade](#responsividade)
- [Como Começar](#como-começar)
- [Padrões e Convenções](#padrões-e-convenções)
- [Performance](#performance)

---

## 🎯 Visão Geral

**SyntaxWear** é um e-commerce especializado em tênis e sneakers, desenvolvido com foco em:

- ✅ HTML semântico e acessível (WCAG 2.1)
- ✅ Design responsivo (Mobile First)
- ✅ CSS modular e escalável
- ✅ Performance otimizada
- ✅ UX/UI intuitiva e moderna

**Tecnologias:**
- HTML5 (semântico)
- CSS3 (Grid, Flexbox, Media Queries)
- Sem dependências JavaScript (front-end puro)

---

## 📁 Estrutura do Projeto

```
ecommerce-syntaxwear/
├── index.html                 # Página principal
├── README.md                  # Este arquivo
├── css/
│   ├── reset.css             # Reset CSS (Andy Bell)
│   ├── variables.css         # Variáveis CSS e fontes
│   ├── base.css              # Estilos base e layout
│   ├── style.css             # Estilos gerais
│   ├── hero.css              # Seção hero
│   ├── categorias.css        # Grid de categorias
│   ├── grid.css              # Grid de produtos
│   └── footer.css            # Rodapé
├── img/
│   ├── logo/                 # Logo da marca
│   ├── icons/                # Ícones (SVG)
│   │   ├── user.svg
│   │   ├── help.svg
│   │   ├── bag.svg
│   │   └── hamburguer.svg
│   ├── produtos/             # Imagens dos produtos
│   │   ├── card_imagem.jpg
│   │   ├── roxo-verde-grid.jpg
│   │   ├── modelo-feminino.jpg
│   │   ├── futurista-grid.jpg
│   │   ├── preto-branco-grid.jpg
│   │   └── moderno-grid.jpg
│   ├── banner/               # Imagens de banner
│   └── favicon/              # Ícone do site
└── .git/                      # Repositório Git
```

---

## ✨ Recursos

### Seções Principais

#### 1. **Header (Cabeçalho)**
- Logo com link para home
- Navegação principal (Masculino, Feminino, Outlet)
- Menu de acesso rápido (Nossas lojas, Sobre, Conta, Ajuda, Carrinho)
- Menu hambúrguer responsivo para mobile

#### 2. **Hero**
- Banner principal com imagem destaque
- Subtítulo e título chamativo
- Botões de CTA (Call-to-Action)
- Overlay para legibilidade do texto

#### 3. **Categorias de Tênis**
- Grid com 4 categorias principais:
  - Casual
  - Esporte
  - Moderno
  - Futurista
- Cards com imagens de fundo
- Hover effects

#### 4. **Grid de Produtos em Destaque**
- Masonry layout responsivo
- 6 cards de produtos (1 destaque + 5 secundários)
- Imagens de alta qualidade
- Call-to-action por produto

#### 5. **Footer (Rodapé)**
- Newsletter (formulário de inscrição)
- Links de redes sociais
- Navegação estruturada por categoria
- Informações de copyright

---

## 🎨 Arquitetura CSS

### Filosofia de Organização

Cada componente principal tem seu próprio arquivo CSS para melhor manutenibilidade:

| Arquivo | Responsabilidade |
|---------|------------------|
| `reset.css` | Reset CSS moderno (inspirado em Andy Bell) |
| `variables.css` | Variáveis CSS e imports de fontes |
| `base.css` | Layout base e tipografia |
| `style.css` | Estilos gerais reutilizáveis |
| `hero.css` | Estilização da seção hero |
| `categorias.css` | Grid e cards de categorias |
| `grid.css` | Grid de produtos com masonry layout |
| `footer.css` | Estilização do rodapé |

### Variáveis CSS

```css
:root {
  --fonte-principal: 'ubuntu', sans-serif;
  /* Adicione aqui mais variáveis conforme necessário */
  /* Cores, espaçamentos, breakpoints, etc. */
}
```

### Reset CSS

O projeto utiliza um reset moderno baseado em "A Modern CSS Reset" de Andy Bell:

✅ Box-sizing border-box
✅ Remove margens padrão
✅ Remove estilos de listas
✅ Scroll suave (smooth scrolling)
✅ Imagens responsivas
✅ Herança de fontes em formulários
✅ Respeito a prefers-reduced-motion

---

## 🧩 Guia de Componentes

### Buttons

**Tipos:**

```html
<!-- Button primário (preenchido) -->
<a class="btn btn-filled" href="#">Comprar</a>

<!-- Button secundário (outline) -->
<a class="btn btn-outline" href="#">Ver modelos</a>
```

### Cards

**Grid Card (Produto):**
```html
<div class="card highlight">
  <div class="top1-content">
    <h3 class="card-title">Titulo</h3>
    <p class="card-subtitle">Subtítulo</p>
    <div class="cta-group">
      <a href="#" class="btn btn-outline">Ação 1</a>
      <a href="#" class="btn btn-filled">Ação 2</a>
    </div>
  </div>
</div>
```

### Navegação

**Navegação Principal:**
```html
<nav aria-label="Categorias Principais">
  <ul>
    <li><a href="#">Masculino</a></li>
    <li><a href="#">Feminino</a></li>
    <li><a href="#">Outlet</a></li>
  </ul>
</nav>
```

---

## ♿ Acessibilidade

O projeto segue as diretrizes **WCAG 2.1 Nível AA**.

### Implementações de Acessibilidade

✅ **HTML Semântico**
- Uso de tags semânticas: `<header>`, `<main>`, `<footer>`, `<nav>`, `<section>`
- Headings estruturados e hierárquicos

✅ **ARIA Labels**
- `aria-label` para elementos sem texto visível
- `aria-labelledby` para associações explícitas
- `role` descritivo para elementos customizados

✅ **Links com Texto Discernível**
- Todos os links possuem texto visível ou aria-label
- Exemplo: `<a href="#" aria-label="Minha conta">...</a>`

✅ **Formulários Acessíveis**
- Labels associados a inputs: `<label for="newsletter-email">`
- Atributos descritivos e obrigatórios

✅ **Contraste e Legibilidade**
- Overlay em imagens de fundo para garantir legibilidade
- Cores com contraste adequado

✅ **Redução de Movimento**
- Respeita `prefers-reduced-motion` dos usuários

---

## 📱 Responsividade

O projeto é **Mobile First** com breakpoints estratégicos:

### Breakpoints

| Tamanho | Breakpoint | Uso |
|---------|-----------|-----|
| Mobile | `≤ 768px` | Phones e tablets pequenos |
| Desktop | `> 768px` | Tablets e desktops |
| Desktop Large | `≤ 1000px` | Media queries adicionais |
| Desktop XL | `≤ 1280px` | Ajustes para telas grandes |

### Grid Responsivo

**Desktop:** 4 colunas × 3 linhas (Masonry layout)
**Mobile:** 2 colunas × 5 linhas (Adaptado)

```css
@media (max-width: 768px) {
  .grid-section {
    grid-template-columns: repeat(2, 1fr);
    /* ... ajustes adicionais ... */
  }
}
```

---

## 🚀 Como Começar

### Pré-requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conhecimento básico de HTML/CSS

### Instalação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/bruno-ce10/ecommerce-syntaxwear.git
   cd ecommerce-syntaxwear
   ```

2. **Abra no navegador:**
   ```bash
   # Opção 1: Abra direto no navegador
   open index.html  # macOS
   start index.html # Windows
   xdg-open index.html # Linux
   ```

   ```bash
   # Opção 2: Use um servidor local
   # Python 3
   python -m http.server 8000
   
   # Node.js (http-server)
   npx http-server

   # Acesse: http://localhost:8000
   ```

3. **Personalize:**
   - Edite `index.html` para adicionar seu conteúdo
   - Modifique cores e espaçamentos em `variables.css`
   - Substitua imagens em `img/`

---

## 📐 Padrões e Convenções

### Nomenclatura de Classes

Seguimos a metodologia **BEM (Block Element Modifier)**:

```css
/* Block */
.footer

/* Element */
.footer__nav
.footer__copy

/* Modifier */
.button--primary
.button--secondary
```

### Estrutura HTML

```html
<!-- Header -->
<header class="site-header">
  <h1 class="logo"></h1>
  <nav aria-label="..."></nav>
</header>

<!-- Main Content -->
<main id="main" role="main">
  <section id="hero" class="hero"></section>
  <section id="categorias" class="categorias"></section>
  <section id="destaques" class="destaques"></section>
</main>

<!-- Footer -->
<footer class="site-footer" role="contentinfo">
  <nav class="footer-nav" aria-label="..."></nav>
</footer>
```

### Ordem de Imports CSS

```html
<link rel="stylesheet" href="./css/reset.css">      <!-- 1. Reset -->
<link rel="stylesheet" href="./css/variables.css">  <!-- 2. Variáveis -->
<link rel="stylesheet" href="./css/base.css">       <!-- 3. Base -->
<link rel="stylesheet" href="./css/style.css">      <!-- 4. Componentes -->
<!-- Componentes específicos... -->
```

---

## ⚡ Performance

### Otimizações Implementadas

✅ **CSS Minificação** (em produção)
✅ **Lazy Loading de Imagens** (recomendado)
✅ **Web Fonts Otimizadas** (Ubuntu do Google Fonts)
✅ **Sem JavaScript desnecessário**
✅ **Imagens em formato SVG** para ícones
✅ **Grid CSS** para layouts eficientes

### Recomendações Futuras

- [ ] Implementar lazy loading: `<img loading="lazy">`
- [ ] Comprimir imagens (WebP com fallback)
- [ ] Minificar CSS em produção
- [ ] Adicionar Service Worker para PWA
- [ ] Implementar Critical CSS

---

## 🔄 Fluxo de Desenvolvimento

### Para Adicionar um Novo Componente

1. Crie o HTML em `index.html`
2. Crie/edite o CSS correspondente em `css/`
3. Importe o CSS no `<head>` do HTML
4. Teste responsividade em diferentes breakpoints
5. Valide acessibilidade com ferramentas (axe, Lighthouse)

### Para Modificar Estilos Globais

1. Edite `variables.css` para cores, fontes, etc.
2. Edite `base.css` para layout e tipografia base
3. Teste em todos os breakpoints

---

## 🧪 Testes e Validação

### Ferramentas Recomendadas

- **HTML Validator:** [W3C Markup Validation](https://validator.w3.org/)
- **CSS Validator:** [W3C CSS Validation](https://jigsaw.w3.org/css-validator/)
- **Accessibility:** [axe DevTools](https://www.deque.com/axe/devtools/) ou Lighthouse
- **Responsividade:** DevTools do navegador (F12)

### Checklist de Qualidade

- [ ] HTML válido (sem erros W3C)
- [ ] CSS válido
- [ ] Sem erros de acessibilidade (axe)
- [ ] Responsivo em: 320px, 768px, 1024px, 1280px
- [ ] Contraste de cores OK (WCAG AA)
- [ ] Links têm texto discernível
- [ ] Formulários têm labels
- [ ] Sem console errors

---

## 📝 Licença

Este projeto é licenciado sob a **MIT License** — veja o arquivo LICENSE para detalhes.

---

## 👤 Autor

**Bruno CE10**
- GitHub: [@bruno-ce10](https://github.com/bruno-ce10)
- Repositório: [ecommerce-syntaxwear](https://github.com/bruno-ce10/ecommerce-syntaxwear)

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

---

## 📞 Suporte

Encontrou um bug ou tem uma sugestão? Abra uma [issue](https://github.com/bruno-ce10/ecommerce-syntaxwear/issues).

---

## 🎓 Recursos Educacionais

- [MDN Web Docs - CSS Grid](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Grid_Layout)
- [MDN Web Docs - Flexbox](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [A Modern CSS Reset - Andy Bell](https://andy-bell.design/articles/a-modern-css-reset/)
- [BEM Methodology](http://bem.info/)

---

**Último update:** 9 de dezembro de 2025
**Versão:** 1.0.0
