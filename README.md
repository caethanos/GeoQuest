# GeoQuest · Geografia do Brasil

Aplicativo de estudo gamificado sobre o capítulo **“Fabricado no Brasil”**. O projeto é estático: HTML, CSS e JavaScript, sem servidor, conta de usuário ou etapa de build. Pode ser publicado diretamente pelo GitHub Pages ou Netlify.

## Arquivos

- `index.html` — página e interface do jogo.
- `styles.css` — layout responsivo para celular e computador.
- `questions.js` — banco autoral de 30 questões, com explicações.
- `app.js` — regras do jogo, progresso, XP e repetição espaçada.
- `netlify.toml` — configuração para publicação no Netlify.

## Como funciona

- O aluno responde uma questão por vez e recebe correção comentada na hora.
- Cada acerto vale 10 XP; uma resposta incorreta vale 3 XP pela tentativa.
- Questões erradas voltam à fila depois de três respostas. As alternativas são reordenadas nas revisões.
- O aluno conclui ao dominar os 30 conceitos e esvaziar a fila de revisão.
- XP, nível, sequência diária e progresso ficam salvos no armazenamento local do navegador. O progresso é específico daquele navegador e dispositivo.
- O botão **Recomeçar** apaga o progresso local.

O banco de questões foi escrito para cobrir os tópicos descritos no briefing e não reproduz trechos do material didático. Confira os enunciados com a edição usada pela turma antes de distribuir como avaliação oficial.

## Publicar no GitHub

1. Crie um repositório novo no GitHub.
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. Para ativar GitHub Pages, abra **Settings → Pages**, selecione **Deploy from a branch**, escolha `main` e a pasta `/ (root)`.

## Publicar no Netlify

1. Envie esta pasta para um repositório no GitHub.
2. No Netlify, escolha **Add new site → Import an existing project** e conecte o repositório.
3. O Netlify detecta o `netlify.toml`. Use `main` como branch de produção e publique.

Também é possível arrastar a pasta para o deploy manual do Netlify. Como o site não tem processo de build, não é necessário comando de build nem diretório `dist`.

## Atualizar o banco

Edite `questions.js`. Cada questão tem `topic`, `q`, quatro alternativas em `options`, o índice da resposta certa em `answer` (começa em zero) e uma explicação em `explain`. Mantenha quatro alternativas por questão para que os atalhos de teclado e a interface permaneçam coerentes.

## Privacidade e limites

O app não coleta respostas nem possui backend. O progresso é armazenado somente no navegador. A fonte tipográfica vem do Google Fonts; se estiver offline, o site usa fontes locais genéricas. A persistência não sincroniza entre dispositivos nem navegadores.
