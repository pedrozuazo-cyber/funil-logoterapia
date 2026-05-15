# Como publicar este HTML no GitHub Pages

Este pacote contém os arquivos prontos para serem publicados como uma página estática no GitHub Pages — gratuito, com URL própria e permanente. Depois de publicado, o link pode ser compartilhado livremente com o analista (e com qualquer outra pessoa).

A URL final terá um destes formatos:

- `https://SEU_USUARIO.github.io/NOME_DO_REPO/` (usando um repositório qualquer)
- `https://SEU_USUARIO.github.io/` (se você criar um repositório especial chamado `SEU_USUARIO.github.io`)

---

## Arquivos deste pacote

- `index.html` — a página dos roteiros do funil (já com tudo inline: CSS, conteúdo).
- `.nojekyll` — arquivo vazio que evita que o GitHub processe a página com Jekyll (mantém o HTML cru).
- `README.md` — este guia.

---

## Passo a passo (caminho mais simples, via web — sem terminal)

### 1. Criar uma conta no GitHub (se ainda não tiver)
- Acesse https://github.com/signup
- Cadastre-se com email, usuário e senha
- Confirme o email
- Conta gratuita já basta para usar GitHub Pages

### 2. Criar um repositório novo
- Logado no GitHub, clique no botão **"+"** no canto superior direito → **New repository**
- Em "Repository name", coloque um nome simples (por exemplo: `funil-logoterapia`)
- Marque a opção **Public** (repositórios privados precisam de plano pago para usar Pages)
- Não marque "Add a README file" (vamos subir o nosso)
- Clique em **Create repository**

### 3. Subir os arquivos
Na tela do repositório recém-criado, você verá um link **"uploading an existing file"** (ou um botão "Add file" → "Upload files"). Clique nele.

Arraste os três arquivos desta pasta `github-pages/` para a área de upload:
- `index.html`
- `.nojekyll`
- `README.md`

Em "Commit changes", deixe a mensagem padrão e clique em **Commit changes**.

> **Dica:** o arquivo `.nojekyll` começa com ponto e é "oculto" no Finder do Mac. Se você não conseguir vê-lo na pasta, abra o Finder e pressione **Cmd + Shift + .** (ponto) para mostrar arquivos ocultos.

### 4. Ativar o GitHub Pages
- No mesmo repositório, vá em **Settings** (engrenagem no topo da página)
- No menu lateral esquerdo, clique em **Pages**
- Em "Build and deployment", seção "Source", selecione **Deploy from a branch**
- Em "Branch", selecione **main** e a pasta **/(root)**
- Clique em **Save**

### 5. Aguardar a publicação (1 a 3 minutos)
A página fica disponível em 1-3 minutos depois do Save. A URL aparece no topo da seção Pages quando estiver pronta.

URL final (exemplo): `https://SEU_USUARIO.github.io/funil-logoterapia/`

### 6. Testar e compartilhar
- Abra a URL no navegador para confirmar que carregou tudo.
- Mande a URL para o analista pelo canal que preferir (WhatsApp, email, Slack).

---

## Atualizações futuras

Sempre que você precisar atualizar os roteiros, basta:
1. Pedir para mim regerar o `index.html` atualizado.
2. No GitHub, abrir o repositório, clicar no arquivo `index.html`, depois no ícone de lápis (Edit), apagar tudo e colar o novo conteúdo. (Ou usar "Add file" → "Upload files" para sobrescrever.)
3. Fazer commit. Em 1-3 minutos a URL pública estará atualizada.

---

## Caminho alternativo (mais técnico, via terminal/Git)

Se preferir usar Git pelo terminal:

```bash
cd "/Users/MACLOC/Desktop/Funil Logoterapia/github-pages"
git init
git add .
git commit -m "Publica roteiros do funil"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/funil-logoterapia.git
git push -u origin main
```

Depois ative o Pages em Settings → Pages (passo 4 acima).

---

## Considerações de privacidade

Lembre que o GitHub Pages **publica o conteúdo de forma pública** — qualquer pessoa com o link consegue ver. Se você quiser restringir o acesso aos roteiros, melhor escolher outra forma de compartilhamento (Google Drive com link restrito a pessoas específicas, por exemplo).

Os roteiros em si não contêm dados sensíveis dos respondentes — apenas as mensagens-modelo e variáveis genéricas (`{{nome}}`, `{{link_curso}}` etc.). A base com os contatos reais (`Logoterapia - Base Clusterizada.xlsx`) **não está neste pacote** e deve ser compartilhada por outro canal.
