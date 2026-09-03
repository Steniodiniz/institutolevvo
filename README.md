# Levvo · Consultoria de Transformação em ICT — Site (Git Pages)

Este diretório (`_comum/public/`) é a versão **publicável** do site de acompanhamento da consultoria de transformação em ICT do Instituto Levvo. É o canal de comunicação com o time do Instituto.

## Publicação no GitHub Pages

> Publicação a cargo do usuário (commit manual). Aqui estão os passos.

### 1. Publicar o conteúdo

- Inicialize um repositório Git **(na pasta `public/`)** para servir direto como site estático.
  ```bash
  cd "Notas Stenio/Repositório/Negocios/Levvo/_comum/public"
  git init
  git add .
  git commit -m "Site Consultoria ICT — Levvo"
  ```

### 2. Conectar ao GitHub (GitHub Pages)

- Crie um repositório (ex.: `levvo-ict`) no GitHub.
- Envie o conteúdo:
  ```bash
  git remote add origin https://github.com/<seu-usuario>/levvo-ict.git
  git branch -M main
  git push -u origin main
  ```
- Em **Settings → Pages**, em "Source", selecione **Deploy from a branch** e escolha `main` na pasta raiz (`/ (root)`). Salve.
- O site fica em `https://<seu-usuario>.github.io/levvo-ict/`.

> Também é possível publicar com Jekyll/GitHub Actions, mas para este site estático basta o branch `main`.

### 3. Estrutura de arquivos

```
public/
├── index.html              # Apresentação (página inicial)
├── projeto.html            # Sobre o projeto (fases, entregáveis, o que ganha)
├── encontros/
│   ├── index.html          # Índice de encontros
│   └── registro-01-2026-09-02.html   # Encontro 01 · Kickoff
├── documentos.html         # Checklist de documentos a fornecer
└── README.md               # este arquivo
```

### 4. Manutenção (a cada atualização)

- Cada HTML tem um cabeçalho com **"Data de atualização"** — renovar ao publicar nova versão.
- **Novo encontro:** criar `encontros/registro-XX-<data>.html` a partir do `registro-01` e adicionar o link no `encontros/index.html`.
- **Novo material/entregável:** criar uma página e linkar na navegação (navbar) de todas as páginas.
- Após alterar, commitar e dar `git push`.

## Regras de conteúdo

- Linguagem **institucional** — sem links internos do vault, sem menções a `Notas Stenio`, SDL, contratos ou processos internos de trabalho.
- Rodapé e meta: **"Produzido por Stenio Diniz. Uso exclusivo do Instituto Levvo."**
- Nada de emojis decorativos; identidade visual teal (`#0e7490`) padrão.
