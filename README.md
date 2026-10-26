# GeoQuest · Unidade 8: Nordeste

Aplicativo de estudo gamificado para a Unidade 8, **“Um Retrato do Nordeste do Brasil”**. O banco contém 32 questões autorais sobre população, ocupação histórica, migrações, relevo, hidrografia, clima, vegetação e sub-regiões.

O projeto é estático: HTML, CSS e JavaScript, sem servidor, conta de usuário ou etapa de build. Pode ser publicado diretamente no GitHub Pages ou Netlify.

## Arquivos

- `index.html` — página e interface do jogo.
- `styles.css` — layout responsivo para celular e computador.
- `questions.js` — 32 questões com gabarito e explicações.
- `app.js` — regras do jogo, progresso, XP e repetição espaçada.
- `netlify.toml` — configuração de publicação no Netlify.

## Como funciona

- O aluno responde uma questão por vez e recebe correção comentada na hora.
- Cada acerto vale 10 XP; uma resposta incorreta vale 3 XP pela tentativa.
- Questões erradas voltam à fila depois de três respostas. As alternativas são reordenadas nas revisões.
- A jornada termina depois de dominar os 32 conceitos e concluir a fila de revisão.
- XP, nível, sequência diária e progresso ficam salvos no navegador. O progresso é específico daquele navegador e dispositivo.
- **Recomeçar** apaga o progresso desta edição da Unidade 8.

As questões foram elaboradas a partir dos tópicos da Unidade 8 indicados no briefing. O PDF fornecido é uma digitalização; confira os enunciados com a edição usada pela turma antes de usar como avaliação oficial.

## Publicar no GitHub

1. Crie um repositório novo no GitHub.
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. Para ativar GitHub Pages, abra **Settings → Pages**, selecione **Deploy from a branch**, escolha `main` e a pasta `/ (root)`.

## Publicar no Netlify

1. Envie esta pasta para um repositório no GitHub.
2. No Netlify, escolha **Add new site → Import an existing project** e conecte o repositório.
3. O Netlify detecta o `netlify.toml`. Use `main` como branch de produção e publique.

Também é possível arrastar a pasta extraída para o deploy manual do Netlify. Envie **todos** os arquivos juntos, incluindo `app.js` e `questions.js`. Não é necessário comando de build nem diretório `dist`.

## Atualizar o banco

Edite `questions.js`. Cada questão tem `topic`, `q`, quatro alternativas em `options`, o índice da resposta certa em `answer` (começa em zero) e uma explicação em `explain`.

## Privacidade

O app não coleta respostas nem possui backend. O progresso é armazenado somente no navegador e não sincroniza entre dispositivos. As fontes tipográficas são carregadas do Google Fonts; se estiver offline, o site usa fontes genéricas locais.
