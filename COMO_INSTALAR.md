# Como instalar o ExZone como app no Android

Este pacote contém a versão instalável (PWA) do seu sistema. Nada da lógica,
dos relatórios ou dos dados foi alterado — só foram adicionados os arquivos
que o Android precisa para reconhecer isso como um app de verdade.

## Passo 1 — Publicar uma vez (gratuito, leva 5 minutos)

O Android só permite instalar um app "de verdade" (com ícone próprio, sem
barra de endereço) se ele vier de um endereço https. Isso **não é loja de
app** — é só um link estático, e depois de instalado uma vez, o app nunca
mais precisa de internet.

1. Crie uma conta gratuita em https://github.com (se ainda não tiver).
2. Clique em "New repository" → dê um nome, ex: `exzone-app` → marque
   "Public" → Create repository.
3. Dentro do repositório, clique em "Add file" → "Upload files" → arraste
   os 4 itens deste pacote (`index.html`, `manifest.json`,
   `service-worker.js` e a pasta `icons`) → Commit changes.
4. Vá em **Settings → Pages** → em "Branch" selecione `main` → Save.
5. Espere 1–2 minutos. O GitHub vai te dar um link parecido com:
   `https://seu-usuario.github.io/exzone-app/`

## Passo 2 — Instalar no celular

1. Abra esse link no **Chrome do Android** (precisa ser o Chrome).
2. Toque nos três pontinhos (menu) → **"Instalar app"** (ou vai aparecer
   um banner automático perguntando se quer instalar).
3. Confirme. O ícone do ExZone aparece na tela inicial, igual a qualquer
   outro app.

## Passo 3 — Uso diário (sem internet)

A partir daí, pode desligar o Wi-Fi e os dados móveis: o app abre normal,
em tela cheia, sem navegador visível, e tudo que você salvar continua
gravado no armazenamento do próprio celular, exatamente como antes.

## Se quiser atualizar o app depois

Sempre que eu (ou você) alterar o `index.html`, é só repetir o Passo 1
(subir o arquivo novo no mesmo repositório). Na próxima vez que o app
abrir com internet disponível, ele detecta a versão nova e atualiza
sozinho em segundo plano.
