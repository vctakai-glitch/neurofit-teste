# NeuroFit (SPA acessível)

Um SPA simples e acessível (HTML/CSS/JS puro) com fluxo de onboarding via Quiz, rotina de 30 dias, lembretes e upsell para Premium.

## Executando localmente

1) Abra no navegador:
   - Windows Explorer: clique duas vezes em `index.html`
   - PowerShell: `start index.html`

2) (Opcional) Servidor local:
   - Python: `python -m http.server 5173 --bind 127.0.0.1` e acesse `http://127.0.0.1:5173`
   - Node: `npx serve -l 5173` e acesse `http://127.0.0.1:5173`

## Estrutura

- `index.html`: shell da aplicação, cabeçalho, landmarks e container principal
- `styles.css`: estilos responsivos e acessíveis (skip link, modal, painel, formulários)
- `app.js`: roteamento por hash e views: Início, Quiz, Como Funciona, Áreas, Premium, Comunidade, Contato, Login e Painel de 30 dias

## Funcionalidades

- Landing com slogan, CTA e resumo
- Quiz inicial: escolha 1 área (grátis), modal de conta e upsell
- Painel do usuário (30 dias): checklist, progresso, pontos e lembretes (WhatsApp/Telegram/E-mail  simulado)
- Páginas Como Funciona, Áreas, Premium, Comunidade (gated), Contato e Login

## Acessibilidade

- Skip link, landmarks semânticos e `aria-live` no container de conteúdo
- Foco levado ao `<main>` a cada navegação
- Botões e formulários com rótulos; modal com `aria-modal` e título associado
- Navegação por teclado suportada; cores com bom contraste

Sugestões de validação:
- Extensão axe DevTools/Lighthouse  verificar contraste, rótulos e navegação
- Teste navegação por teclado (Tab/Shift+Tab) e foco no conteúdo

## Armazenamento (simulado)

- `localStorage`: `nfUser`, `nfArea`, `nfPremium`, `nfProgress`, `nfReminder`

## Notas

- Vídeos são links simulados (YouTube).
- Comunidade, upgrades e notificações são prototipados (sem backend).
