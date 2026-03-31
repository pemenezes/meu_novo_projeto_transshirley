# AGENTS.md - Trans Shirley Website

## Visão Geral do Projeto
Website institucional para a **Trans Shirley Transportes**, empresa com 15 anos de experiência em transporte nacional.

## Stack Tecnológica
- **HTML5** semântico
- **Tailwind CSS** via CDN (v3.4)
- **Alpine.js** para interatividade (v3.x)
- **Formspree** para formulário de contato (sem backend)

## Comandos de Desenvolvimento

### Servidor Local
```bash
# Python
python3 -m http.server 8000

# Node.js (npx)
npx serve .

# PHP
php -S localhost:8000
```

### Validação
```bash
# HTML validation (se tiver validator)
python3 -m html.parser --check-syntax *.html
```

## Estrutura de Arquivos
```
/
├── index.html          # Home
├── sobre.html          # Sobre a empresa
├── servicos.html       # Serviços
├── cobertura.html      # Mapa de cobertura
├── contato.html        # Formulário de contato
└── assets/             # Pasta para imagens (opcional)
```

## Paleta de Cores
| Nome | Hex | Uso |
|------|-----|-----|
| Primary | `#DC2626` | Botões, destaques |
| Secondary | `#1F2937` | Textos, footer |
| Accent | `#F59E0B` | Ícones, badges |
| Background | `#F9FAFB` | Fundo principal |
| White | `#FFFFFF` | Cards, seções |

## Convenções de Código

### HTML
- Usar tags semânticas: `<header>`, `<main>`, `<nav>`, `<footer>`, `<section>`, `<article>`
- Alt text obrigatório em todas as imagens
- Classes Tailwind em kebab-case
- Mobile-first (classes `md:` e `lg:` para responsividade)

### Tailwind CSS
- Usar classes utilitárias do Tailwind (sem CSS customizado quando possível)
- Componentes reutilizáveis via `@apply` se necessário
- Cores via classes: `bg-primary`, `text-secondary`, etc.

### Alpine.js
- Usar para: menu mobile, tabs, accordions, carousels
- Estrutura: `x-data`, `x-show`, `x-transition`
- Manter estado local quando possível

### Imagens
- Usar Unsplash/Pexels para imagens de demonstração
- Formato WebP quando possível
- Lazy loading: `loading="lazy"`

## SEO
- Meta title: max 60 caracteres
- Meta description: max 160 caracteres
- Open Graph tags para redes sociais
- Sitemap XML (para adicionar depois)

## Acessibilidade
- Contraste mínimo 4.5:1
- Focus states visíveis
- Navegação por teclado funcional
- Skip to content link

## Funcionalidades por Página

### Home (index.html)
- Hero com CTA
- Números/estatísticas (anos de experiência, estados)
- Seção sobre resumida
- Cards de serviços
- CTA para contato

### Sobre (sobre.html)
- História da empresa
- Missão, Visão, Valores (cards)
- Diferenciais

### Serviços (servicos.html)
- Lista de serviços com ícones
- Descrições detalhadas

### Cobertura (cobertura.html)
- Mapa do Brasil
- Lista de estados atendidos

### Contato (contato.html)
- Formulário (nome, email, telefone, mensagem)
- Informações da Matriz (Osasco-SP)
- Informações da Filial (Brasília-DF)

## Formspree Setup
Substituir `YOUR_FORMSPREE_ID` no formulário com o ID real:
```html
<form action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">
```

## Deploy
- Hospedagem estática (GitHub Pages, Netlify, Vercel)
- Ou hospedagem KingHost atual (FTP)
- SSL automático recomendado
