# Melhorias planejadas — Convite Jonynho 1 Aninho

## Estado atual do projeto
- Arquivo único: `index.html` (35MB, todas as imagens em base64)
- Tema verde-chácara + vermelho Patrulha Canina
- Banner fixo com hide/show ao scroll
- Seções: Hero · Countdown · Programação · Atividades · Fotos · Localização

---

## Melhorias a implementar

### 1. Banner — Glassmorphism
- Trocar fundo vermelho sólido por `backdrop-filter: blur(20px)` com fundo semitransparente escuro/avermelhado
- Adicionar a nav de botões de volta (estava comentada no HTML)
- Deixar mais fino e elegante

### 2. Hero — Textura de chácara
- Adicionar SVG inline de grama animada na base do hero (ondulando suavemente)
- Overlay de "luz solar" no canto superior direito
- Título com `-webkit-text-stroke` para efeito outline mais impactante

### 3. Seção "A Chácara" (NOVA)
- Grid de atrações com ícone grande + nome + descrição curta
- Itens: ⚽ Campo de Futebol · 🏐 Quadra de Vôlei · 🏊 Piscina · 🎤 Karaokê · 🌳 Área Verde · 🍖 Churrasqueira
- Cards com hover animado e borda colorida

### 4. Seção "O que trazer" (NOVA)
- Cards visuais com ícone grande e fundo colorido
- Itens: 🩱 Traje de banho · 🏊 Toalha · 🕶️ Óculos de sol · 🧴 Protetor solar · 👟 Tênis para jogar · 📸 Câmera/celular
- Aviso em destaque: "Venha preparado para muita diversão!"

### 5. Countdown — Flip Clock
- Estilo relógio de airport com animação de "flip" ao mudar os números
- Card dividido em duas metades (top/bottom) com transição 3D

### 6. Cards de atividade — Flip on hover
- `.act-card` com `transform-style: preserve-3d`
- Frente: imagem + nome
- Verso: descrição detalhada da atividade + horário

### 7. Confirmação de presença — WhatsApp real
- Botão verde WhatsApp com ícone SVG
- Link `https://wa.me/55XXXXXXXXXXX?text=Mensagem+pre-pronta`
- Substituir o link genérico atual

### 8. Parallax suave no Hero
- Ao fazer scroll, a imagem principal desce mais devagar que a página
- `transform: translateY(scrollY * 0.3)` via JS com `requestAnimationFrame`

### 9. Banner — Nav reativada e melhorada
- Descomentar a `<nav class="banner-nav">` no HTML
- Botão ativo muda com scroll (já tem o JS de `updateBnavActive`)
- Melhorar visual dos botões: ícone + texto, fundo pill mais bonito

### 10. Mobile — Banner compacto
- Em telas < 480px: mostrar só logo 🐾 + "Jonynho 1 Aninho" + botão menu
- Menu hambúrguer que expande a nav de seções

---

## Arquivos do projeto
```
jonynho-birthday/
├── index.html          ← arquivo principal (tudo embutido)
├── assets/
│   ├── *.png           ← imagens originais (já em base64 no HTML)
│   ├── gsap.min.js     ← não usado na versão atual
│   ├── three.min.js    ← não usado na versão atual
│   └── patrulha-canina.mp3  ← música (faltando!)
└── MELHORIAS.md        ← este arquivo
```

## Observações
- O arquivo `assets/patrulha-canina.mp3` não existe — botão de música aparece mas não toca
- GSAP e Three.js não são mais usados (novo design é CSS puro)
- Número do WhatsApp real precisa ser fornecido para o botão de confirmação
