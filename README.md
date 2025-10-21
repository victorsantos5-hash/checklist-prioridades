[README_Version4.md](https://github.com/user-attachments/files/23023628/README_Version4.md)
# Checklist de Prioridades

Aplicativo web simples (HTML/CSS/JS) para gerenciar tarefas:
- Adicionar tarefas;
- Marcar concluídas (checkbox) — texto riscado;
- Excluir tarefas individualmente;
- Reordenar tarefas por arrastar (drag & drop) para definir prioridades;
- Salvar / Baixar em `.txt` com formato: `1. [X] Tarefa (priority)`;
- Fazer Upload de um `.txt` gerado pelo app — o site lê e importa as tarefas.

Como usar localmente
1. Abra `index.html` em um navegador moderno (Chrome, Firefox, Edge, Safari).
2. Use o input para digitar tarefas e o botão "Adicionar" (ou Enter).
3. Use a alça (≡) para arrastar e definir ordem (topo = prioridade 1).
4. Clique "💾 Salvar / Baixar" para gerar `minhas_tarefas.txt`.
5. Clique "📤 Upload" para importar um `.txt` no mesmo formato (aceita variantes).

Publicar no GitHub (passo a passo)
- Método via GitHub Web:
  1. Crie um novo repositório (ex.: `checklist-prioridades`).
  2. No repositório, clique em "Add file" → "Upload files" e envie `index.html` e `README.md`.
  3. Commit e pronto.

- Método via terminal (git + gh CLI opcional):
  ```bash
  mkdir checklist-prioridades
  cd checklist-prioridades
  # copie index.html e README.md para essa pasta
  git init
  git add .
  git commit -m "Initial commit: checklist app"
  # criar repositório remoto no GitHub (com gh CLI)
  gh repo create victorsantos5-hash/checklist-prioridades --public --source=. --remote=origin --push
  # ou, se preferir usar git remote manualmente:
  # git remote add origin git@github.com:SEU_USUARIO/checklist-prioridades.git
  # git branch -M main
  # git push -u origin main
  ```

Publicar como site (GitHub Pages)
1. No repositório, vá em Settings → Pages.
2. Escolha a branch `main` e a pasta `/ (root)`.
3. Salve — o GitHub publicará `index.html` em `https://<seu-usuario>.github.io/checklist-prioridades/` (pode demorar alguns minutos).

Observações
- O parser de upload aceita linhas com ou sem prefixo numérico, reconhece `[X]` como concluída e aceita prioridade em parênteses (ex.: `(high)` ou `(alta)`).
- Se quiser eu posso:
  - Gerar um arquivo ZIP pronto para você baixar;
  - Gerar o comando exato git/gh com seu usuário (substituir SEU_USUARIO);
  - Criar um gist com o index.html (se preferir compartilhar rapidamente).
